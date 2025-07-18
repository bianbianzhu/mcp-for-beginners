<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "748c61250d4a326206b72b28f6154615",
  "translation_date": "2025-07-13T23:46:48+00:00",
  "source_file": "05-AdvancedTopics/README.md",
  "language_code": "tl"
}
-->
# Advanced Topics in MCP 

Ang kabanatang ito ay naglalayong talakayin ang mga serye ng advanced na paksa sa implementasyon ng Model Context Protocol (MCP), kabilang ang multi-modal integration, scalability, mga pinakamahusay na kasanayan sa seguridad, at enterprise integration. Mahalaga ang mga paksang ito para makabuo ng matibay at handang gamitin sa produksyon na mga aplikasyon ng MCP na kayang tugunan ang mga pangangailangan ng makabagong AI systems.

## Overview

Tinutuklas ng araling ito ang mga advanced na konsepto sa implementasyon ng Model Context Protocol, na nakatuon sa multi-modal integration, scalability, mga pinakamahusay na kasanayan sa seguridad, at enterprise integration. Mahalaga ang mga paksang ito para makabuo ng mga production-grade na aplikasyon ng MCP na kayang humawak ng mga kumplikadong pangangailangan sa mga enterprise environment.

## Learning Objectives

Sa pagtatapos ng araling ito, magagawa mong:

- Ipatupad ang multi-modal na kakayahan sa loob ng MCP frameworks
- Magdisenyo ng scalable na MCP architectures para sa mga sitwasyong mataas ang demand
- Ilapat ang mga pinakamahusay na kasanayan sa seguridad na naaayon sa mga prinsipyo ng seguridad ng MCP
- Isama ang MCP sa mga enterprise AI systems at frameworks
- I-optimize ang performance at pagiging maaasahan sa mga production environment

## Lessons and sample Projects

| Link | Title | Description |
|------|-------|-------------|
| [5.1 Integration with Azure](./mcp-integration/README.md) | Integrate with Azure | Matutunan kung paano isama ang iyong MCP Server sa Azure |
| [5.2 Multi modal sample](./mcp-multi-modality/README.md) | MCP Multi modal samples  | Mga halimbawa para sa audio, imahe, at multi-modal na tugon |
| [5.3 MCP OAuth2 sample](../../../05-AdvancedTopics/mcp-oauth2-demo) | MCP OAuth2 Demo | Minimal na Spring Boot app na nagpapakita ng OAuth2 gamit ang MCP, bilang Authorization at Resource Server. Ipinapakita ang secure na pag-isyu ng token, protektadong mga endpoint, deployment sa Azure Container Apps, at integrasyon sa API Management. |
| [5.4 Root Contexts](./mcp-root-contexts/README.md) | Root contexts  | Alamin pa ang tungkol sa root context at kung paano ito ipinatutupad |
| [5.5 Routing](./mcp-routing/README.md) | Routing | Matutunan ang iba't ibang uri ng routing |
| [5.6 Sampling](./mcp-sampling/README.md) | Sampling | Matutunan kung paano gamitin ang sampling |
| [5.7 Scaling](./mcp-scaling/README.md) | Scaling  | Matutunan ang tungkol sa scaling |
| [5.8 Security](./mcp-security/README.md) | Security  | Siguraduhin ang seguridad ng iyong MCP Server |
| [5.9 Web Search sample](./web-search-mcp/README.md) | Web Search MCP | Python MCP server at client na nagsasama ng SerpAPI para sa real-time na web, balita, paghahanap ng produkto, at Q&A. Ipinapakita ang multi-tool orchestration, integrasyon ng external API, at matibay na paghawak ng error. |
| [5.10 Realtime Streaming](./mcp-realtimestreaming/README.md) | Streaming  | Ang real-time data streaming ay naging mahalaga sa mundo ngayon na pinapatakbo ng data, kung saan kailangan ng mga negosyo at aplikasyon ng agarang access sa impormasyon para makagawa ng napapanahong desisyon.|
| [5.11 Realtime Web Search](./mcp-realtimesearch/README.md) | Web Search | Paano binabago ng MCP ang real-time web search sa pamamagitan ng pagbibigay ng standardized na paraan sa pamamahala ng konteksto sa pagitan ng AI models, search engines, at mga aplikasyon.| 
| [5.12  Entra ID Authentication for Model Context Protocol Servers](./mcp-security-entra/README.md) | Entra ID Authentication | Nagbibigay ang Microsoft Entra ID ng matibay na cloud-based identity at access management solution, na tumutulong tiyakin na tanging mga awtorisadong user at aplikasyon lamang ang makakagamit ng iyong MCP server.|
| [5.13 Azure AI Foundry Agent Integration](./mcp-foundry-agent-integration/README.md) | Azure AI Foundry Integration | Matutunan kung paano isama ang Model Context Protocol servers sa Azure AI Foundry agents, na nagpapahintulot ng makapangyarihang tool orchestration at enterprise AI capabilities gamit ang standardized na koneksyon sa mga external data source.|

## Additional References

Para sa pinakabagong impormasyon tungkol sa mga advanced na paksa sa MCP, tingnan ang:
- [MCP Documentation](https://modelcontextprotocol.io/)
- [MCP Specification](https://spec.modelcontextprotocol.io/)
- [GitHub Repository](https://github.com/modelcontextprotocol)

## Key Takeaways

- Pinalalawak ng multi-modal MCP implementations ang kakayahan ng AI lampas sa text processing
- Mahalaga ang scalability para sa mga enterprise deployment at maaaring tugunan sa pamamagitan ng horizontal at vertical scaling
- Pinoprotektahan ng komprehensibong mga hakbang sa seguridad ang data at tinitiyak ang tamang access control
- Pinapalakas ng enterprise integration sa mga platform tulad ng Azure OpenAI at Microsoft AI Foundry ang kakayahan ng MCP
- Nakikinabang ang advanced MCP implementations mula sa optimized na mga arkitektura at maingat na pamamahala ng mga resources

## Exercise

Magdisenyo ng enterprise-grade na implementasyon ng MCP para sa isang partikular na kaso ng paggamit:

1. Tukuyin ang mga multi-modal na pangangailangan para sa iyong kaso ng paggamit
2. Ilahad ang mga kontrol sa seguridad na kailangan para protektahan ang sensitibong data
3. Magdisenyo ng scalable na arkitektura na kayang humawak ng nagbabagong load
4. Planuhin ang mga integration point sa mga enterprise AI system
5. Idokumento ang mga posibleng bottleneck sa performance at mga estratehiya para malutas ito

## Additional Resources

- [Azure OpenAI Documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Microsoft AI Foundry Documentation](https://learn.microsoft.com/en-us/ai-services/)

---

## What's next

- [5.1 MCP Integration](./mcp-integration/README.md)

**Paalala**:  
Ang dokumentong ito ay isinalin gamit ang AI translation service na [Co-op Translator](https://github.com/Azure/co-op-translator). Bagamat nagsusumikap kami para sa katumpakan, pakatandaan na ang mga awtomatikong pagsasalin ay maaaring maglaman ng mga pagkakamali o di-tumpak na impormasyon. Ang orihinal na dokumento sa orihinal nitong wika ang dapat ituring na pangunahing sanggunian. Para sa mahahalagang impormasyon, inirerekomenda ang propesyonal na pagsasalin ng tao. Hindi kami mananagot sa anumang hindi pagkakaunawaan o maling interpretasyon na maaaring magmula sa paggamit ng pagsasaling ito.