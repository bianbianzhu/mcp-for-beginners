<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "26d41919cb423a87e067a3da8334e44a",
  "translation_date": "2025-07-14T04:29:08+00:00",
  "source_file": "07-LessonsfromEarlyAdoption/README.md",
  "language_code": "sv"
}
-->
# Lärdomar från tidiga användare

## Översikt

Den här lektionen utforskar hur tidiga användare har utnyttjat Model Context Protocol (MCP) för att lösa verkliga utmaningar och driva innovation inom olika branscher. Genom detaljerade fallstudier och praktiska projekt får du se hur MCP möjliggör standardiserad, säker och skalbar AI-integration – som kopplar samman stora språkmodeller, verktyg och företagsdata i en enhetlig ram. Du får praktisk erfarenhet av att designa och bygga lösningar baserade på MCP, lära dig av beprövade implementationsmönster och upptäcka bästa praxis för att driftsätta MCP i produktionsmiljöer. Lektionen lyfter också fram nya trender, framtida riktningar och open source-resurser för att hjälpa dig ligga i framkant inom MCP-teknologin och dess växande ekosystem.

## Lärandemål

- Analysera verkliga MCP-implementationer inom olika branscher  
- Designa och bygga kompletta applikationer baserade på MCP  
- Utforska nya trender och framtida riktningar inom MCP-teknologi  
- Tillämpa bästa praxis i faktiska utvecklingsscenarier  

## Verkliga MCP-implementationer

### Fallstudie 1: Automatisering av företagskundsupport

Ett multinationellt företag implementerade en MCP-baserad lösning för att standardisera AI-interaktioner över sina kundsupportsystem. Detta gjorde det möjligt för dem att:

- Skapa ett enhetligt gränssnitt för flera LLM-leverantörer  
- Bibehålla konsekvent prompt-hantering över avdelningar  
- Implementera robusta säkerhets- och efterlevnadskontroller  
- Enkelt växla mellan olika AI-modeller beroende på specifika behov  

**Teknisk implementation:**  
```python
# Python MCP server implementation for customer support
import logging
import asyncio
from modelcontextprotocol import create_server, ServerConfig
from modelcontextprotocol.server import MCPServer
from modelcontextprotocol.transports import create_http_transport
from modelcontextprotocol.resources import ResourceDefinition
from modelcontextprotocol.prompts import PromptDefinition
from modelcontextprotocol.tool import ToolDefinition

# Configure logging
logging.basicConfig(level=logging.INFO)

async def main():
    # Create server configuration
    config = ServerConfig(
        name="Enterprise Customer Support Server",
        version="1.0.0",
        description="MCP server for handling customer support inquiries"
    )
    
    # Initialize MCP server
    server = create_server(config)
    
    # Register knowledge base resources
    server.resources.register(
        ResourceDefinition(
            name="customer_kb",
            description="Customer knowledge base documentation"
        ),
        lambda params: get_customer_documentation(params)
    )
    
    # Register prompt templates
    server.prompts.register(
        PromptDefinition(
            name="support_template",
            description="Templates for customer support responses"
        ),
        lambda params: get_support_templates(params)
    )
    
    # Register support tools
    server.tools.register(
        ToolDefinition(
            name="ticketing",
            description="Create and update support tickets"
        ),
        handle_ticketing_operations
    )
    
    # Start server with HTTP transport
    transport = create_http_transport(port=8080)
    await server.run(transport)

if __name__ == "__main__":
    asyncio.run(main())
```

**Resultat:** 30 % minskning av modellkostnader, 45 % förbättring i svarskonsistens och förbättrad efterlevnad över globala verksamheter.

### Fallstudie 2: Diagnostisk assistent inom vården

En vårdgivare utvecklade en MCP-infrastruktur för att integrera flera specialiserade medicinska AI-modeller samtidigt som känslig patientdata skyddades:

- Sömlös växling mellan generella och specialiserade medicinska modeller  
- Strikta sekretesskontroller och revisionsspår  
- Integration med befintliga elektroniska journaler (EHR)  
- Konsekvent prompt-engineering för medicinsk terminologi  

**Teknisk implementation:**  
```csharp
// C# MCP host application implementation in healthcare application
using Microsoft.Extensions.DependencyInjection;
using ModelContextProtocol.SDK.Client;
using ModelContextProtocol.SDK.Security;
using ModelContextProtocol.SDK.Resources;

public class DiagnosticAssistant
{
    private readonly MCPHostClient _mcpClient;
    private readonly PatientContext _patientContext;
    
    public DiagnosticAssistant(PatientContext patientContext)
    {
        _patientContext = patientContext;
        
        // Configure MCP client with healthcare-specific settings
        var clientOptions = new ClientOptions
        {
            Name = "Healthcare Diagnostic Assistant",
            Version = "1.0.0",
            Security = new SecurityOptions
            {
                Encryption = EncryptionLevel.Medical,
                AuditEnabled = true
            }
        };
        
        _mcpClient = new MCPHostClientBuilder()
            .WithOptions(clientOptions)
            .WithTransport(new HttpTransport("https://healthcare-mcp.example.org"))
            .WithAuthentication(new HIPAACompliantAuthProvider())
            .Build();
    }
    
    public async Task<DiagnosticSuggestion> GetDiagnosticAssistance(
        string symptoms, string patientHistory)
    {
        // Create request with appropriate resources and tool access
        var resourceRequest = new ResourceRequest
        {
            Name = "patient_records",
            Parameters = new Dictionary<string, object>
            {
                ["patientId"] = _patientContext.PatientId,
                ["requestingProvider"] = _patientContext.ProviderId
            }
        };
        
        // Request diagnostic assistance using appropriate prompt
        var response = await _mcpClient.SendPromptRequestAsync(
            promptName: "diagnostic_assistance",
            parameters: new Dictionary<string, object>
            {
                ["symptoms"] = symptoms,
                patientHistory = patientHistory,
                relevantGuidelines = _patientContext.GetRelevantGuidelines()
            });
            
        return DiagnosticSuggestion.FromMCPResponse(response);
    }
}
```

**Resultat:** Förbättrade diagnostiska förslag för läkare samtidigt som full HIPAA-efterlevnad upprätthölls och betydande minskning av kontextväxling mellan system.

### Fallstudie 3: Riskanalys inom finanssektorn

En finansinstitution implementerade MCP för att standardisera sina riskanalyser över olika avdelningar:

- Skapade ett enhetligt gränssnitt för kreditrisk, bedrägeridetektion och investeringsriskmodeller  
- Implementerade strikta åtkomstkontroller och versionshantering av modeller  
- Säkerställde spårbarhet för alla AI-rekommendationer  
- Bibehöll konsekvent dataformat över olika system  

**Teknisk implementation:**  
```java
// Java MCP server for financial risk assessment
import org.mcp.server.*;
import org.mcp.security.*;

public class FinancialRiskMCPServer {
    public static void main(String[] args) {
        // Create MCP server with financial compliance features
        MCPServer server = new MCPServerBuilder()
            .withModelProviders(
                new ModelProvider("risk-assessment-primary", new AzureOpenAIProvider()),
                new ModelProvider("risk-assessment-audit", new LocalLlamaProvider())
            )
            .withPromptTemplateDirectory("./compliance/templates")
            .withAccessControls(new SOCCompliantAccessControl())
            .withDataEncryption(EncryptionStandard.FINANCIAL_GRADE)
            .withVersionControl(true)
            .withAuditLogging(new DatabaseAuditLogger())
            .build();
            
        server.addRequestValidator(new FinancialDataValidator());
        server.addResponseFilter(new PII_RedactionFilter());
        
        server.start(9000);
        
        System.out.println("Financial Risk MCP Server running on port 9000");
    }
}
```

**Resultat:** Förbättrad regulatorisk efterlevnad, 40 % snabbare modellutrullningscykler och förbättrad konsekvens i riskbedömningar över avdelningar.

### Fallstudie 4: Microsoft Playwright MCP-server för webbläsarautomation

Microsoft utvecklade [Playwright MCP-servern](https://github.com/microsoft/playwright-mcp) för att möjliggöra säker, standardiserad webbläsarautomation via Model Context Protocol. Denna lösning låter AI-agenter och LLMs interagera med webbläsare på ett kontrollerat, granskningsbart och utbyggbart sätt – vilket möjliggör användningsfall som automatiserad webbtillförlitlighetstestning, datautvinning och end-to-end arbetsflöden.

- Exponerar webbläsarautomationsfunktioner (navigering, formulärifyllning, skärmdumpskapning etc.) som MCP-verktyg  
- Implementerar strikta åtkomstkontroller och sandboxing för att förhindra obehöriga åtgärder  
- Tillhandahåller detaljerade revisionsloggar för alla webbläsarinteraktioner  
- Stöder integration med Azure OpenAI och andra LLM-leverantörer för agentdriven automation  

**Teknisk implementation:**  
```typescript
// TypeScript: Registering Playwright browser automation tools in an MCP server
import { createServer, ToolDefinition } from 'modelcontextprotocol';
import { launch } from 'playwright';

const server = createServer({
  name: 'Playwright MCP Server',
  version: '1.0.0',
  description: 'MCP server for browser automation using Playwright'
});

// Register a tool for navigating to a URL and capturing a screenshot
server.tools.register(
  new ToolDefinition({
    name: 'navigate_and_screenshot',
    description: 'Navigate to a URL and capture a screenshot',
    parameters: {
      url: { type: 'string', description: 'The URL to visit' }
    }
  }),
  async ({ url }) => {
    const browser = await launch();
    const page = await browser.newPage();
    await page.goto(url);
    const screenshot = await page.screenshot();
    await browser.close();
    return { screenshot };
  }
);

// Start the MCP server
server.listen(8080);
```

**Resultat:**  
- Möjliggjorde säker, programmerbar webbläsarautomation för AI-agenter och LLMs  
- Minskat manuellt testarbete och förbättrat testtäckning för webbapplikationer  
- Erbjöd en återanvändbar, utbyggbar ram för webbläsarbaserad verktygsintegration i företagsmiljöer  

**Referenser:**  
- [Playwright MCP Server GitHub Repository](https://github.com/microsoft/playwright-mcp)  
- [Microsoft AI and Automation Solutions](https://azure.microsoft.com/en-us/products/ai-services/)

### Fallstudie 5: Azure MCP – Enterprise-klass Model Context Protocol som tjänst

Azure MCP ([https://aka.ms/azmcp](https://aka.ms/azmcp)) är Microsofts hanterade, företagsklassade implementation av Model Context Protocol, designad för att erbjuda skalbara, säkra och efterlevnadssäkra MCP-serverfunktioner som molntjänst. Azure MCP gör det möjligt för organisationer att snabbt distribuera, hantera och integrera MCP-servrar med Azure AI, data och säkerhetstjänster, vilket minskar driftkostnader och påskyndar AI-adoption.

- Fullt hanterad MCP-serverhosting med inbyggd skalning, övervakning och säkerhet  
- Naturlig integration med Azure OpenAI, Azure AI Search och andra Azure-tjänster  
- Företagsautentisering och auktorisering via Microsoft Entra ID  
- Stöd för anpassade verktyg, promptmallar och resurskopplingar  
- Efterlevnad av företags säkerhets- och regulatoriska krav  

**Teknisk implementation:**  
```yaml
# Example: Azure MCP server deployment configuration (YAML)
apiVersion: mcp.microsoft.com/v1
kind: McpServer
metadata:
  name: enterprise-mcp-server
spec:
  modelProviders:
    - name: azure-openai
      type: AzureOpenAI
      endpoint: https://<your-openai-resource>.openai.azure.com/
      apiKeySecret: <your-azure-keyvault-secret>
  tools:
    - name: document_search
      type: AzureAISearch
      endpoint: https://<your-search-resource>.search.windows.net/
      apiKeySecret: <your-azure-keyvault-secret>
  authentication:
    type: EntraID
    tenantId: <your-tenant-id>
  monitoring:
    enabled: true
    logAnalyticsWorkspace: <your-log-analytics-id>
```

**Resultat:**  
- Minskat time-to-value för företags-AI-projekt genom att erbjuda en färdig, efterlevnadssäker MCP-serverplattform  
- Förenklad integration av LLMs, verktyg och företagsdatakällor  
- Förbättrad säkerhet, observabilitet och driftseffektivitet för MCP-arbetsbelastningar  

**Referenser:**  
- [Azure MCP Documentation](https://aka.ms/azmcp)  
- [Azure AI Services](https://azure.microsoft.com/en-us/products/ai-services/)

## Fallstudie 6: NLWeb  
MCP (Model Context Protocol) är ett framväxande protokoll för chatbots och AI-assistenter att interagera med verktyg. Varje NLWeb-instans är också en MCP-server som stödjer en kärnmetod, ask, som används för att ställa en fråga till en webbplats på naturligt språk. Det returnerade svaret använder schema.org, ett välanvänt vokabulär för att beskriva webdata. Förenklat kan man säga att MCP är för NLWeb vad Http är för HTML. NLWeb kombinerar protokoll, schema.org-format och exempel på kod för att hjälpa webbplatser att snabbt skapa dessa ändpunkter, vilket gynnar både människor genom konversationsgränssnitt och maskiner genom naturlig agent-till-agent-interaktion.

NLWeb består av två distinkta komponenter:  
- Ett protokoll, mycket enkelt att börja med, för att gränssnitta med en webbplats på naturligt språk och ett format som använder json och schema.org för det returnerade svaret. Se dokumentationen om REST API för mer information.  
- En enkel implementation av (1) som utnyttjar befintlig markup, för webbplatser som kan abstraheras som listor av objekt (produkter, recept, sevärdheter, recensioner etc.). Tillsammans med ett set användargränssnittskomponenter kan webbplatser enkelt erbjuda konversationsgränssnitt till sitt innehåll. Se dokumentationen om Life of a chat query för mer information om hur detta fungerar.  

**Referenser:**  
- [Azure MCP Documentation](https://aka.ms/azmcp)  
- [NLWeb](https://github.com/microsoft/NlWeb)

### Fallstudie 7: MCP för Foundry – Integrering av Azure AI-agenter

Azure AI Foundry MCP-servrar visar hur MCP kan användas för att orkestrera och hantera AI-agenter och arbetsflöden i företagsmiljöer. Genom att integrera MCP med Azure AI Foundry kan organisationer standardisera agentinteraktioner, utnyttja Foundrys arbetsflödeshantering och säkerställa säkra, skalbara distributioner. Denna metod möjliggör snabb prototypframtagning, robust övervakning och sömlös integration med Azure AI-tjänster, och stödjer avancerade scenarier som kunskapshantering och agentutvärdering. Utvecklare får ett enhetligt gränssnitt för att bygga, distribuera och övervaka agentpipelines, medan IT-team får förbättrad säkerhet, efterlevnad och driftseffektivitet. Lösningen är idealisk för företag som vill påskynda AI-adoption och behålla kontroll över komplexa agentdrivna processer.

**Referenser:**  
- [MCP Foundry GitHub Repository](https://github.com/azure-ai-foundry/mcp-foundry)  
- [Integrating Azure AI Agents with MCP (Microsoft Foundry Blog)](https://devblogs.microsoft.com/foundry/integrating-azure-ai-agents-mcp/)

### Fallstudie 8: Foundry MCP Playground – Experiment och prototypframtagning

Foundry MCP Playground erbjuder en färdig miljö för att experimentera med MCP-servrar och Azure AI Foundry-integrationer. Utvecklare kan snabbt prototypa, testa och utvärdera AI-modeller och agentarbetsflöden med resurser från Azure AI Foundry Catalog och Labs. Playgrounden förenklar uppsättning, tillhandahåller exempelprojekt och stödjer samarbetsutveckling, vilket gör det enkelt att utforska bästa praxis och nya scenarier med minimal overhead. Den är särskilt användbar för team som vill validera idéer, dela experiment och påskynda lärande utan behov av komplex infrastruktur. Genom att sänka tröskeln för inträde främjar playgrounden innovation och community-bidrag inom MCP och Azure AI Foundry-ekosystemet.

**Referenser:**  
- [Foundry MCP Playground GitHub Repository](https://github.com/azure-ai-foundry/foundry-mcp-playground)

### Fallstudie 9: Microsoft Docs MCP Server – Lärande och kompetensutveckling  
Microsoft Docs MCP Server implementerar Model Context Protocol (MCP) servern som ger AI-assistenter realtidsåtkomst till officiell Microsoft-dokumentation. Utför semantisk sökning mot Microsofts officiella tekniska dokumentation.

**Referenser:**  
- [Microsoft Learn Docs MCP Server](https://github.com/MicrosoftDocs/mcp)

## Praktiska projekt

### Projekt 1: Bygg en MCP-server med flera leverantörer

**Mål:** Skapa en MCP-server som kan dirigera förfrågningar till flera AI-modellleverantörer baserat på specifika kriterier.

**Krav:**  
- Stöd för minst tre olika modellleverantörer (t.ex. OpenAI, Anthropic, lokala modeller)  
- Implementera en routingmekanism baserad på metadata i förfrågningar  
- Skapa ett konfigurationssystem för hantering av leverantörsautentisering  
- Lägg till caching för att optimera prestanda och kostnader  
- Bygg en enkel dashboard för övervakning av användning  

**Implementeringssteg:**  
1. Sätt upp grundläggande MCP-serverinfrastruktur  
2. Implementera adapter för varje AI-modelltjänst  
3. Skapa routinglogik baserat på förfrågningsattribut  
4. Lägg till cachemekanismer för frekventa förfrågningar  
5. Utveckla övervakningsdashboard  
6. Testa med olika förfrågningsmönster  

**Teknologier:** Välj mellan Python (.NET/Java/Python beroende på preferens), Redis för caching och ett enkelt webbframework för dashboarden.

### Projekt 2: Företagsövergripande system för prompt-hantering

**Mål:** Utveckla ett MCP-baserat system för att hantera, versionera och distribuera promptmallar inom en organisation.

**Krav:**  
- Skapa ett centraliserat arkiv för promptmallar  
- Implementera versionshantering och godkännandeprocesser  
- Bygg funktioner för malltestning med exempeldata  
- Utveckla rollbaserade åtkomstkontroller  
- Skapa ett API för hämtning och distribution av mallar  

**Implementeringssteg:**  
1. Designa databasschema för malllagring  
2. Skapa kärn-API för CRUD-operationer på mallar  
3. Implementera versionshanteringssystem  
4. Bygg godkännandeprocess  
5. Utveckla testningsramverk  
6. Skapa enkel webbgränssnitt för hantering  
7. Integrera med MCP-server  

**Teknologier:** Valfritt backend-framework, SQL eller NoSQL-databas och frontend-framework för hanteringsgränssnitt.

### Projekt 3: Plattform för innehållsgenerering baserad på MCP

**Mål:** Bygg en plattform för innehållsgenerering som använder MCP för att leverera konsekventa resultat över olika innehållstyper.

**Krav:**  
- Stöd för flera innehållsformat (blogginlägg, sociala medier, marknadsföringstexter)  
- Implementera mallbaserad generering med anpassningsmöjligheter  
- Skapa system för innehållsgranskning och feedback  
- Spåra innehållsprestanda  
- Stöd för versionshantering och iteration av innehåll  

**Implementeringssteg:**  
1. Sätt upp MCP-klientinfrastruktur  
2. Skapa mallar för olika innehållstyper  
3. Bygg pipeline för innehållsgenerering  
4. Implementera granskningssystem  
5. Utveckla system för prestationsmätning  
6. Skapa användargränssnitt för mallhantering och innehållsgenerering  

**Teknologier:** Valfritt programmeringsspråk, webbframework och databassystem.

## Framtida riktningar för MCP-teknologi

### Nya trender

1. **Multi-modal MCP**  
   - Utvidgning av MCP för att standardisera interaktioner med bild-, ljud- och videomodeller  
   - Utveckling av tvärmodal resonemangsförmåga  
   - Standardiserade promptformat för olika modaliteter  

2. **Federerad MCP-infrastruktur**  
   - Distribuerade MCP-nätverk som kan dela resurser mellan organisationer  
   - Standardiserade protokoll för säker modell-delning  
   - Sekretessbevarande beräkningstekniker  

3. **MCP-marknadsplatser**  
   - Ekosystem för delning och monetisering av MCP-mallar och plugins  
   - Kvalitetssäkring och certifieringsprocesser  
   - Integration med modellmarknadsplatser  

4. **MCP för edge computing**  
   - Anpassning av MCP-standarder för resursbegränsade edge-enheter  
   - Optimerade protokoll för lågbandbreddsmiljöer  
   - Specialiserade MCP-implementationer för IoT-ekosystem  

5. **Regulatoriska ramverk**  
   - Utveckling av MCP-tillägg för regulatorisk efterlevnad  
   - Standardiserade revisionsspår och förklaringsgränssnitt  
   - Integration med framväxande AI-styrningsramverk  

### MCP-lösningar från Microsoft

Microsoft och Azure har utvecklat flera open source-repositorier för att hjälpa utvecklare implementera MCP i olika scenarier:

#### Microsoft-organisationen  
1. [playwright-mcp](https://github.com/microsoft/playwright-mcp) – En Playwright MCP-server för webbläsarautomation och testning  
2. [files-mcp-server](https://github.com/microsoft/files-mcp-server) – En OneDrive MCP-serverimplementation för lokal testning och community-bidrag  
3. [NLWeb](https://github.com/microsoft/NlWeb) – NLWeb är en samling öppna protokoll och tillhörande open source-verktyg. Huvudfokus är att etablera ett grundläggande lager för AI Web  

#### Azure-Samples-organisationen  
1. [mcp](https://github.com/Azure-Samples/mcp) – Länkar till exempel, verktyg och resurser för att bygga och integrera MCP-servrar på Azure med flera språk  
2. [mcp-auth-servers](https://github.com/Azure-Samples/mcp-auth-servers) – Referens-MCP-servrar som demonstrerar autentisering enligt den aktuella Model Context Protocol-specifikationen
3. [remote-mcp-functions](https://github.com/Azure-Samples/remote-mcp-functions) - Startsida för Remote MCP Server-implementationer i Azure Functions med länkar till språksspecifika repos  
4. [remote-mcp-functions-python](https://github.com/Azure-Samples/remote-mcp-functions-python) - Snabbstartsmall för att bygga och distribuera anpassade remote MCP-servrar med Azure Functions och Python  
5. [remote-mcp-functions-dotnet](https://github.com/Azure-Samples/remote-mcp-functions-dotnet) - Snabbstartsmall för att bygga och distribuera anpassade remote MCP-servrar med Azure Functions och .NET/C#  
6. [remote-mcp-functions-typescript](https://github.com/Azure-Samples/remote-mcp-functions-typescript) - Snabbstartsmall för att bygga och distribuera anpassade remote MCP-servrar med Azure Functions och TypeScript  
7. [remote-mcp-apim-functions-python](https://github.com/Azure-Samples/remote-mcp-apim-functions-python) - Azure API Management som AI-gateway till Remote MCP-servrar med Python  
8. [AI-Gateway](https://github.com/Azure-Samples/AI-Gateway) - APIM ❤️ AI-experiment inklusive MCP-funktioner, integrerat med Azure OpenAI och AI Foundry  

Dessa repos tillhandahåller olika implementationer, mallar och resurser för att arbeta med Model Context Protocol över flera programmeringsspråk och Azure-tjänster. De täcker en rad användningsfall från grundläggande serverimplementationer till autentisering, molndistribution och företagsintegration.  

#### MCP Resources Directory

[MCP Resources directory](https://github.com/microsoft/mcp/tree/main/Resources) i den officiella Microsoft MCP-repot innehåller en noggrant utvald samling av exempelresurser, promptmallar och verktygsdefinitioner för användning med Model Context Protocol-servrar. Denna katalog är utformad för att hjälpa utvecklare att snabbt komma igång med MCP genom att erbjuda återanvändbara byggstenar och bästa praxis-exempel för:  

- **Promptmallar:** Färdiga promptmallar för vanliga AI-uppgifter och scenarier, som kan anpassas för dina egna MCP-serverimplementationer.  
- **Verktygsdefinitioner:** Exempel på verktygsscheman och metadata för att standardisera verktygsintegration och anrop över olika MCP-servrar.  
- **Resursprover:** Exempel på resursdefinitioner för att koppla upp mot datakällor, API:er och externa tjänster inom MCP-ramverket.  
- **Referensimplementationer:** Praktiska exempel som visar hur man strukturerar och organiserar resurser, prompts och verktyg i verkliga MCP-projekt.  

Dessa resurser påskyndar utvecklingen, främjar standardisering och hjälper till att säkerställa bästa praxis vid byggande och distribution av MCP-baserade lösningar.  

#### MCP Resources Directory
- [MCP Resources (Sample Prompts, Tools, and Resource Definitions)](https://github.com/microsoft/mcp/tree/main/Resources)  

### Forskningsmöjligheter

- Effektiva tekniker för promptoptimering inom MCP-ramverk  
- Säkerhetsmodeller för multi-tenant MCP-distributioner  
- Prestandamätningar över olika MCP-implementationer  
- Formella verifieringsmetoder för MCP-servrar  

## Slutsats

Model Context Protocol (MCP) formar snabbt framtiden för standardiserad, säker och interoperabel AI-integration över olika branscher. Genom fallstudierna och de praktiska projekten i denna lektion har du sett hur tidiga användare – inklusive Microsoft och Azure – använder MCP för att lösa verkliga utmaningar, påskynda AI-antagande och säkerställa efterlevnad, säkerhet och skalbarhet. MCP:s modulära tillvägagångssätt gör det möjligt för organisationer att koppla samman stora språkmodeller, verktyg och företagsdata i en enhetlig, granskbar ram. När MCP fortsätter att utvecklas kommer det vara avgörande att hålla sig engagerad i communityn, utforska öppen källkod-resurser och tillämpa bästa praxis för att bygga robusta, framtidssäkra AI-lösningar.  

## Ytterligare resurser

- [MCP Foundry GitHub Repository](https://github.com/azure-ai-foundry/mcp-foundry)  
- [Foundry MCP Playground](https://github.com/azure-ai-foundry/foundry-mcp-playground)  
- [Integrating Azure AI Agents with MCP (Microsoft Foundry Blog)](https://devblogs.microsoft.com/foundry/integrating-azure-ai-agents-mcp/)  
- [MCP GitHub Repository (Microsoft)](https://github.com/microsoft/mcp)  
- [MCP Resources Directory (Sample Prompts, Tools, and Resource Definitions)](https://github.com/microsoft/mcp/tree/main/Resources)  
- [MCP Community & Documentation](https://modelcontextprotocol.io/introduction)  
- [Azure MCP Documentation](https://aka.ms/azmcp)  
- [Playwright MCP Server GitHub Repository](https://github.com/microsoft/playwright-mcp)  
- [Files MCP Server (OneDrive)](https://github.com/microsoft/files-mcp-server)  
- [Azure-Samples MCP](https://github.com/Azure-Samples/mcp)  
- [MCP Auth Servers (Azure-Samples)](https://github.com/Azure-Samples/mcp-auth-servers)  
- [Remote MCP Functions (Azure-Samples)](https://github.com/Azure-Samples/remote-mcp-functions)  
- [Remote MCP Functions Python (Azure-Samples)](https://github.com/Azure-Samples/remote-mcp-functions-python)  
- [Remote MCP Functions .NET (Azure-Samples)](https://github.com/Azure-Samples/remote-mcp-functions-dotnet)  
- [Remote MCP Functions TypeScript (Azure-Samples)](https://github.com/Azure-Samples/remote-mcp-functions-typescript)  
- [Remote MCP APIM Functions Python (Azure-Samples)](https://github.com/Azure-Samples/remote-mcp-apim-functions-python)  
- [AI-Gateway (Azure-Samples)](https://github.com/Azure-Samples/AI-Gateway)  
- [Microsoft AI and Automation Solutions](https://azure.microsoft.com/en-us/products/ai-services/)  

## Övningar

1. Analysera en av fallstudierna och föreslå en alternativ implementationsmetod.  
2. Välj en av projektidéerna och skapa en detaljerad teknisk specifikation.  
3. Undersök en bransch som inte täcks i fallstudierna och skissa på hur MCP kan lösa dess specifika utmaningar.  
4. Utforska en av framtidsriktningarna och skapa ett koncept för en ny MCP-extension som stödjer den.  

Nästa: [Best Practices](../08-BestPractices/README.md)

**Ansvarsfriskrivning**:  
Detta dokument har översatts med hjälp av AI-översättningstjänsten [Co-op Translator](https://github.com/Azure/co-op-translator). Även om vi strävar efter noggrannhet, vänligen observera att automatiska översättningar kan innehålla fel eller brister. Det ursprungliga dokumentet på dess modersmål bör betraktas som den auktoritativa källan. För kritisk information rekommenderas professionell mänsklig översättning. Vi ansvarar inte för några missförstånd eller feltolkningar som uppstår vid användning av denna översättning.