<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "873741da08dd6537858d5e14c3a386e1",
  "translation_date": "2025-07-14T05:44:42+00:00",
  "source_file": "09-CaseStudy/README.md",
  "language_code": "pa"
}
-->
# MCP ਕਾਰਜ ਵਿੱਚ: ਅਸਲੀ ਦੁਨੀਆ ਦੇ ਕੇਸ ਅਧਿਐਨ

Model Context Protocol (MCP) ਇਹ ਬਦਲ ਰਿਹਾ ਹੈ ਕਿ ਕਿਵੇਂ AI ਐਪਲੀਕੇਸ਼ਨ ਡਾਟਾ, ਟੂਲਜ਼ ਅਤੇ ਸਰਵਿਸਜ਼ ਨਾਲ ਇੰਟਰੈਕਟ ਕਰਦੇ ਹਨ। ਇਹ ਭਾਗ ਅਸਲੀ ਦੁਨੀਆ ਦੇ ਕੇਸ ਅਧਿਐਨਾਂ ਨੂੰ ਪੇਸ਼ ਕਰਦਾ ਹੈ ਜੋ ਵੱਖ-ਵੱਖ ਉਦਯੋਗਿਕ ਸਥਿਤੀਆਂ ਵਿੱਚ MCP ਦੇ ਪ੍ਰਯੋਗ ਨੂੰ ਦਰਸਾਉਂਦੇ ਹਨ।

## ਝਲਕ

ਇਸ ਭਾਗ ਵਿੱਚ MCP ਦੇ ਲਾਗੂ ਕਰਨ ਦੇ ਠੋਸ ਉਦਾਹਰਣ ਦਿੱਤੇ ਗਏ ਹਨ, ਜੋ ਦਿਖਾਉਂਦੇ ਹਨ ਕਿ ਕਿਵੇਂ ਸੰਗਠਨ ਇਸ ਪ੍ਰੋਟੋਕੋਲ ਨੂੰ ਵਰਤ ਕੇ ਜਟਿਲ ਕਾਰੋਬਾਰੀ ਸਮੱਸਿਆਵਾਂ ਦਾ ਹੱਲ ਕਰ ਰਹੇ ਹਨ। ਇਹ ਕੇਸ ਅਧਿਐਨ ਵੇਖ ਕੇ, ਤੁਸੀਂ MCP ਦੀ ਬਹੁਪੱਖੀਤਾ, ਸਕੇਲਬਿਲਟੀ ਅਤੇ ਅਸਲੀ ਦੁਨੀਆ ਵਿੱਚ ਇਸਦੇ ਲਾਭਾਂ ਬਾਰੇ ਜਾਣਕਾਰੀ ਪ੍ਰਾਪਤ ਕਰੋਗੇ।

## ਮੁੱਖ ਸਿੱਖਣ ਦੇ ਉਦੇਸ਼

ਇਹ ਕੇਸ ਅਧਿਐਨਾਂ ਦੀ ਖੋਜ ਕਰਕੇ, ਤੁਸੀਂ:

- ਸਮਝੋਗੇ ਕਿ MCP ਨੂੰ ਵਿਸ਼ੇਸ਼ ਕਾਰੋਬਾਰੀ ਸਮੱਸਿਆਵਾਂ ਦੇ ਹੱਲ ਲਈ ਕਿਵੇਂ ਲਾਗੂ ਕੀਤਾ ਜਾ ਸਕਦਾ ਹੈ
- ਵੱਖ-ਵੱਖ ਇੰਟੀਗ੍ਰੇਸ਼ਨ ਪੈਟਰਨ ਅਤੇ ਆਰਕੀਟੈਕਚਰਲ ਤਰੀਕਿਆਂ ਬਾਰੇ ਜਾਣੋਗੇ
- ਉਦਯੋਗਿਕ ਵਾਤਾਵਰਣ ਵਿੱਚ MCP ਲਾਗੂ ਕਰਨ ਲਈ ਸਰਵੋਤਮ ਅਭਿਆਸਾਂ ਨੂੰ ਪਛਾਣੋਗੇ
- ਅਸਲੀ ਦੁਨੀਆ ਵਿੱਚ ਲਾਗੂ ਕਰਨ ਸਮੇਂ ਆਉਣ ਵਾਲੀਆਂ ਚੁਣੌਤੀਆਂ ਅਤੇ ਹੱਲਾਂ ਬਾਰੇ ਜਾਣਕਾਰੀ ਪ੍ਰਾਪਤ ਕਰੋਗੇ
- ਆਪਣੇ ਪ੍ਰੋਜੈਕਟਾਂ ਵਿੱਚ ਸਮਾਨ ਪੈਟਰਨ ਲਾਗੂ ਕਰਨ ਦੇ ਮੌਕੇ ਪਛਾਣੋਗੇ

## ਪ੍ਰਮੁੱਖ ਕੇਸ ਅਧਿਐਨ

### 1. [Azure AI Travel Agents – Reference Implementation](./travelagentsample.md)

ਇਹ ਕੇਸ ਅਧਿਐਨ Microsoft ਦੇ ਵਿਸਤ੍ਰਿਤ ਰੈਫਰੈਂਸ ਹੱਲ ਦੀ ਜਾਂਚ ਕਰਦਾ ਹੈ ਜੋ ਦਿਖਾਉਂਦਾ ਹੈ ਕਿ MCP, Azure OpenAI ਅਤੇ Azure AI Search ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕਿਵੇਂ ਇੱਕ ਮਲਟੀ-ਏਜੰਟ, AI-ਚਲਿਤ ਯਾਤਰਾ ਯੋਜਨਾ ਐਪਲੀਕੇਸ਼ਨ ਬਣਾਈ ਜਾ ਸਕਦੀ ਹੈ। ਪ੍ਰੋਜੈਕਟ ਵਿੱਚ ਸ਼ਾਮਲ ਹਨ:

- MCP ਰਾਹੀਂ ਮਲਟੀ-ਏਜੰਟ ਸਹਿਯੋਗ
- Azure AI Search ਨਾਲ ਉਦਯੋਗਿਕ ਡਾਟਾ ਇੰਟੀਗ੍ਰੇਸ਼ਨ
- Azure ਸਰਵਿਸਜ਼ ਦੀ ਵਰਤੋਂ ਨਾਲ ਸੁਰੱਖਿਅਤ ਅਤੇ ਸਕੇਲਬਲ ਆਰਕੀਟੈਕਚਰ
- ਦੁਬਾਰਾ ਵਰਤਣ ਯੋਗ MCP ਕੰਪੋਨੈਂਟਸ ਨਾਲ ਵਧੀਆ ਟੂਲਿੰਗ
- Azure OpenAI ਦੁਆਰਾ ਚਲਾਇਆ ਗਿਆ ਗੱਲਬਾਤੀ ਯੂਜ਼ਰ ਅਨੁਭਵ

ਆਰਕੀਟੈਕਚਰ ਅਤੇ ਲਾਗੂ ਕਰਨ ਦੇ ਵੇਰਵੇ MCP ਨੂੰ ਕੋਆਰਡੀਨੇਸ਼ਨ ਲੇਅਰ ਵਜੋਂ ਵਰਤ ਕੇ ਜਟਿਲ, ਮਲਟੀ-ਏਜੰਟ ਸਿਸਟਮ ਬਣਾਉਣ ਵਿੱਚ ਕੀਮਤੀ ਜਾਣਕਾਰੀ ਦਿੰਦੇ ਹਨ।

### 2. [Updating Azure DevOps Items from YouTube Data](./UpdateADOItemsFromYT.md)

ਇਹ ਕੇਸ ਅਧਿਐਨ MCP ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਵਰਕਫਲੋ ਪ੍ਰਕਿਰਿਆਵਾਂ ਨੂੰ ਆਟੋਮੇਟ ਕਰਨ ਦਾ ਇੱਕ ਪ੍ਰਯੋਗ ਦਿਖਾਉਂਦਾ ਹੈ। ਇਹ ਦਿਖਾਉਂਦਾ ਹੈ ਕਿ MCP ਟੂਲਜ਼ ਕਿਵੇਂ:

- ਆਨਲਾਈਨ ਪਲੇਟਫਾਰਮਾਂ (YouTube) ਤੋਂ ਡਾਟਾ ਕੱਢ ਸਕਦੇ ਹਨ
- Azure DevOps ਸਿਸਟਮ ਵਿੱਚ ਵਰਕ ਆਈਟਮ ਅਪਡੇਟ ਕਰ ਸਕਦੇ ਹਨ
- ਦੁਹਰਾਏ ਜਾਣ ਵਾਲੇ ਆਟੋਮੇਸ਼ਨ ਵਰਕਫਲੋ ਬਣਾਉਂਦੇ ਹਨ
- ਵੱਖ-ਵੱਖ ਸਿਸਟਮਾਂ ਵਿੱਚ ਡਾਟਾ ਇੰਟੀਗ੍ਰੇਟ ਕਰਦੇ ਹਨ

ਇਹ ਉਦਾਹਰਣ ਦਰਸਾਉਂਦਾ ਹੈ ਕਿ ਸਧਾਰਣ MCP ਲਾਗੂ ਕਰਨ ਨਾਲ ਵੀ ਰੋਜ਼ਾਨਾ ਦੇ ਕੰਮਾਂ ਨੂੰ ਆਟੋਮੇਟ ਕਰਕੇ ਅਤੇ ਸਿਸਟਮਾਂ ਵਿੱਚ ਡਾਟਾ ਸਥਿਰਤਾ ਸੁਧਾਰ ਕੇ ਕਿੰਨੀ ਵੱਡੀ ਕੁਸ਼ਲਤਾ ਪ੍ਰਾਪਤ ਕੀਤੀ ਜਾ ਸਕਦੀ ਹੈ।

### 3. [Real-Time Documentation Retrieval with MCP](./docs-mcp/README.md)

ਇਹ ਕੇਸ ਅਧਿਐਨ ਤੁਹਾਨੂੰ ਦਿਖਾਉਂਦਾ ਹੈ ਕਿ ਕਿਵੇਂ Python ਕਨਸੋਲ ਕਲਾਇੰਟ ਨੂੰ MCP ਸਰਵਰ ਨਾਲ ਜੋੜ ਕੇ Microsoft ਦੀ ਰੀਅਲ-ਟਾਈਮ, ਸੰਦਰਭ-ਸੂਚਿਤ ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਪ੍ਰਾਪਤ ਅਤੇ ਲੌਗ ਕੀਤੀ ਜਾ ਸਕਦੀ ਹੈ। ਤੁਸੀਂ ਸਿੱਖੋਗੇ ਕਿ:

- Python ਕਲਾਇੰਟ ਅਤੇ ਅਧਿਕਾਰਤ MCP SDK ਦੀ ਵਰਤੋਂ ਕਰਕੇ MCP ਸਰਵਰ ਨਾਲ ਕਨੈਕਟ ਕਰਨਾ
- ਪ੍ਰਭਾਵਸ਼ਾਲੀ, ਰੀਅਲ-ਟਾਈਮ ਡਾਟਾ ਪ੍ਰਾਪਤੀ ਲਈ ਸਟ੍ਰੀਮਿੰਗ HTTP ਕਲਾਇੰਟ ਦੀ ਵਰਤੋਂ
- ਸਰਵਰ 'ਤੇ ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਟੂਲਜ਼ ਨੂੰ ਕਾਲ ਕਰਨਾ ਅਤੇ ਜਵਾਬਾਂ ਨੂੰ ਸਿੱਧਾ ਕਨਸੋਲ 'ਤੇ ਲੌਗ ਕਰਨਾ
- ਟਰਮੀਨਲ ਛੱਡੇ ਬਿਨਾਂ ਆਪਣੇ ਵਰਕਫਲੋ ਵਿੱਚ ਅਪ-ਟੂ-ਡੇਟ Microsoft ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਸ਼ਾਮਲ ਕਰਨਾ

ਇਸ ਅਧਿਆਇ ਵਿੱਚ ਇੱਕ ਹੱਥ-ਅਨੁਭਵ ਅਸਾਈਨਮੈਂਟ, ਇੱਕ ਘੱਟੋ-ਘੱਟ ਕੰਮ ਕਰਨ ਵਾਲਾ ਕੋਡ ਸੈਂਪਲ ਅਤੇ ਹੋਰ ਸਿੱਖਣ ਲਈ ਸਰੋਤਾਂ ਦੇ ਲਿੰਕ ਸ਼ਾਮਲ ਹਨ। ਪੂਰੀ ਪ੍ਰਕਿਰਿਆ ਅਤੇ ਕੋਡ ਨੂੰ ਵੇਖੋ ਤਾਂ ਜੋ ਸਮਝ ਸਕੋ ਕਿ MCP ਕਿਵੇਂ ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਪਹੁੰਚ ਅਤੇ ਡਿਵੈਲਪਰ ਉਤਪਾਦਕਤਾ ਨੂੰ ਬਦਲ ਸਕਦਾ ਹੈ।

### 4. [Interactive Study Plan Generator Web App with MCP](./docs-mcp/README.md)

ਇਹ ਕੇਸ ਅਧਿਐਨ ਦਿਖਾਉਂਦਾ ਹੈ ਕਿ ਕਿਵੇਂ Chainlit ਅਤੇ Model Context Protocol (MCP) ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕਿਸੇ ਵੀ ਵਿਸ਼ੇ ਲਈ ਨਿੱਜੀਕ੍ਰਿਤ ਅਧਿਐਨ ਯੋਜਨਾ ਬਣਾਉਣ ਵਾਲੀ ਇੰਟਰਐਕਟਿਵ ਵੈੱਬ ਐਪਲੀਕੇਸ਼ਨ ਤਿਆਰ ਕੀਤੀ ਜਾ ਸਕਦੀ ਹੈ। ਯੂਜ਼ਰ ਕਿਸੇ ਵਿਸ਼ੇ (ਜਿਵੇਂ "AI-900 ਸਰਟੀਫਿਕੇਸ਼ਨ") ਅਤੇ ਅਧਿਐਨ ਸਮੇਂ (ਜਿਵੇਂ 8 ਹਫ਼ਤੇ) ਨੂੰ ਦਰਜ ਕਰ ਸਕਦੇ ਹਨ, ਅਤੇ ਐਪ ਹਫ਼ਤੇ-ਦਰ-ਹਫ਼ਤਾ ਸਿਫਾਰਸ਼ੀ ਸਮੱਗਰੀ ਦਿੰਦੀ ਹੈ। Chainlit ਗੱਲਬਾਤੀ ਚੈਟ ਇੰਟਰਫੇਸ ਨੂੰ ਯਕੀਨੀ ਬਣਾਉਂਦਾ ਹੈ, ਜੋ ਅਨੁਭਵ ਨੂੰ ਮਨੋਰੰਜਕ ਅਤੇ ਅਨੁਕੂਲ ਬਣਾਉਂਦਾ ਹੈ।

- Chainlit ਦੁਆਰਾ ਚਲਾਇਆ ਗਿਆ ਗੱਲਬਾਤੀ ਵੈੱਬ ਐਪ
- ਵਿਸ਼ੇ ਅਤੇ ਸਮੇਂ ਲਈ ਯੂਜ਼ਰ-ਚਲਿਤ ਪ੍ਰਾਂਪਟ
- MCP ਦੀ ਵਰਤੋਂ ਨਾਲ ਹਫ਼ਤੇ-ਦਰ-ਹਫ਼ਤਾ ਸਮੱਗਰੀ ਦੀ ਸਿਫਾਰਸ਼
- ਚੈਟ ਇੰਟਰਫੇਸ ਵਿੱਚ ਰੀਅਲ-ਟਾਈਮ, ਅਨੁਕੂਲ ਜਵਾਬ

ਇਹ ਪ੍ਰੋਜੈਕਟ ਦਰਸਾਉਂਦਾ ਹੈ ਕਿ ਕਿਵੇਂ ਗੱਲਬਾਤੀ AI ਅਤੇ MCP ਨੂੰ ਮਿਲਾ ਕੇ ਆਧੁਨਿਕ ਵੈੱਬ ਵਾਤਾਵਰਣ ਵਿੱਚ ਗਤੀਸ਼ੀਲ, ਯੂਜ਼ਰ-ਚਲਿਤ ਸਿੱਖਿਆ ਟੂਲ ਬਣਾਏ ਜਾ ਸਕਦੇ ਹਨ।

### 5. [In-Editor Docs with MCP Server in VS Code](./docs-mcp/README.md)

ਇਹ ਕੇਸ ਅਧਿਐਨ ਦਿਖਾਉਂਦਾ ਹੈ ਕਿ ਕਿਵੇਂ MCP ਸਰਵਰ ਦੀ ਵਰਤੋਂ ਕਰਕੇ Microsoft Learn Docs ਨੂੰ ਸਿੱਧਾ VS Code ਵਾਤਾਵਰਣ ਵਿੱਚ ਲਿਆਇਆ ਜਾ ਸਕਦਾ ਹੈ—ਹੁਣ ਬ੍ਰਾਊਜ਼ਰ ਟੈਬ ਬਦਲਣ ਦੀ ਲੋੜ ਨਹੀਂ! ਤੁਸੀਂ ਵੇਖੋਗੇ ਕਿ ਕਿਵੇਂ:

- MCP ਪੈਨਲ ਜਾਂ ਕਮਾਂਡ ਪੈਲੇਟ ਦੀ ਵਰਤੋਂ ਕਰਕੇ VS Code ਵਿੱਚ ਤੁਰੰਤ ਡੌਕਸ ਖੋਜ ਅਤੇ ਪੜ੍ਹਾਈ ਜਾ ਸਕਦੀ ਹੈ
- ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਦਾ ਹਵਾਲਾ ਦੇਣਾ ਅਤੇ README ਜਾਂ ਕੋਰਸ ਮਾਰਕਡਾਊਨ ਫਾਈਲਾਂ ਵਿੱਚ ਲਿੰਕ ਸ਼ਾਮਲ ਕਰਨਾ
- GitHub Copilot ਅਤੇ MCP ਨੂੰ ਮਿਲਾ ਕੇ ਬਿਨਾਂ ਰੁਕਾਵਟ ਦੇ AI-ਚਲਿਤ ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਅਤੇ ਕੋਡ ਵਰਕਫਲੋ ਬਣਾਉਣਾ
- ਰੀਅਲ-ਟਾਈਮ ਫੀਡਬੈਕ ਅਤੇ Microsoft-ਸਰੋਤ ਵਾਲੀ ਸਹੀਤਾ ਨਾਲ ਆਪਣੀ ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਨੂੰ ਵੈਰੀਫਾਈ ਅਤੇ ਸੁਧਾਰਨਾ
- MCP ਨੂੰ GitHub ਵਰਕਫਲੋਜ਼ ਨਾਲ ਜੋੜ ਕੇ ਲਗਾਤਾਰ ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਵੈਰੀਫਿਕੇਸ਼ਨ ਕਰਨਾ

ਲਾਗੂ ਕਰਨ ਵਿੱਚ ਸ਼ਾਮਲ ਹਨ:
- ਆਸਾਨ ਸੈਟਅਪ ਲਈ `.vscode/mcp.json` ਕਨਫਿਗਰੇਸ਼ਨ ਉਦਾਹਰਣ
- ਇਨ-ਐਡੀਟਰ ਅਨੁਭਵ ਦੇ ਸਕ੍ਰੀਨਸ਼ਾਟ-ਆਧਾਰਿਤ ਵਾਕਥਰੂ
- ਵੱਧ ਤੋਂ ਵੱਧ ਉਤਪਾਦਕਤਾ ਲਈ Copilot ਅਤੇ MCP ਨੂੰ ਮਿਲਾਉਣ ਦੇ ਟਿਪਸ

ਇਹ ਸਥਿਤੀ ਕੋਰਸ ਲੇਖਕਾਂ, ਡੌਕਯੂਮੈਂਟੇਸ਼ਨ ਲੇਖਕਾਂ ਅਤੇ ਡਿਵੈਲਪਰਾਂ ਲਈ ਬਹੁਤ ਵਧੀਆ ਹੈ ਜੋ ਆਪਣੇ ਐਡੀਟਰ ਵਿੱਚ ਧਿਆਨ ਕੇਂਦਰਿਤ ਰੱਖਦੇ ਹੋਏ ਡੌਕਸ, Copilot ਅਤੇ ਵੈਰੀਫਿਕੇਸ਼ਨ ਟੂਲਜ਼ ਨਾਲ ਕੰਮ ਕਰਨਾ ਚਾਹੁੰਦੇ ਹਨ—ਸਭ MCP ਦੁਆਰਾ ਸੰਚਾਲਿਤ।

### 6. [APIM MCP Server Creation](./apimsample.md)

ਇਹ ਕੇਸ ਅਧਿਐਨ Azure API Management (APIM) ਦੀ ਵਰਤੋਂ ਕਰਕੇ MCP ਸਰਵਰ ਬਣਾਉਣ ਲਈ ਕਦਮ-ਦਰ-ਕਦਮ ਮਾਰਗਦਰਸ਼ਨ ਦਿੰਦਾ ਹੈ। ਇਸ ਵਿੱਚ ਸ਼ਾਮਲ ਹਨ:

- Azure API Management ਵਿੱਚ MCP ਸਰਵਰ ਸੈਟਅਪ ਕਰਨਾ
- MCP ਟੂਲਜ਼ ਵਜੋਂ API ਓਪਰੇਸ਼ਨਜ਼ ਨੂੰ ਐਕਸਪੋਜ਼ ਕਰਨਾ
- ਰੇਟ ਲਿਮਿਟਿੰਗ ਅਤੇ ਸੁਰੱਖਿਆ ਲਈ ਨੀਤੀਆਂ ਕਨਫਿਗਰ ਕਰਨਾ
- Visual Studio Code ਅਤੇ GitHub Copilot ਦੀ ਵਰਤੋਂ ਕਰਕੇ MCP ਸਰਵਰ ਦੀ ਟੈਸਟਿੰਗ

ਇਹ ਉਦਾਹਰਣ ਦਰਸਾਉਂਦਾ ਹੈ ਕਿ ਕਿਵੇਂ Azure ਦੀਆਂ ਸਮਰੱਥਾਵਾਂ ਨੂੰ ਵਰਤ ਕੇ ਇੱਕ ਮਜ਼ਬੂਤ MCP ਸਰਵਰ ਬਣਾਇਆ ਜਾ ਸਕਦਾ ਹੈ ਜੋ ਵੱਖ-ਵੱਖ ਐਪਲੀਕੇਸ਼ਨਾਂ ਵਿੱਚ ਵਰਤਿਆ ਜਾ ਸਕਦਾ ਹੈ, AI ਸਿਸਟਮਾਂ ਨੂੰ ਉਦਯੋਗਿਕ APIs ਨਾਲ ਬਿਹਤਰ ਤਰੀਕੇ ਨਾਲ ਜੋੜਦਾ ਹੈ।

## ਨਤੀਜਾ

ਇਹ ਕੇਸ ਅਧਿਐਨ Model Context Protocol ਦੀ ਬਹੁਪੱਖੀਤਾ ਅਤੇ ਅਸਲੀ ਦੁਨੀਆ ਵਿੱਚ ਇਸਦੇ ਪ੍ਰਯੋਗਾਂ ਨੂੰ ਉਜਾਗਰ ਕਰਦੇ ਹਨ। ਜਟਿਲ ਮਲਟੀ-ਏਜੰਟ ਸਿਸਟਮਾਂ ਤੋਂ ਲੈ ਕੇ ਨਿਸ਼ਾਨਾ ਬਣਾਈ ਆਟੋਮੇਸ਼ਨ ਵਰਕਫਲੋ ਤੱਕ, MCP ਇੱਕ ਮਿਆਰੀ ਤਰੀਕਾ ਪ੍ਰਦਾਨ ਕਰਦਾ ਹੈ ਜੋ AI ਸਿਸਟਮਾਂ ਨੂੰ ਉਹਨਾਂ ਦੇ ਟੂਲਜ਼ ਅਤੇ ਡਾਟਾ ਨਾਲ ਜੋੜਦਾ ਹੈ ਜਿਨ੍ਹਾਂ ਦੀ ਉਹਨਾਂ ਨੂੰ ਲੋੜ ਹੁੰਦੀ ਹੈ ਤਾਂ ਜੋ ਮੁੱਲ ਪੈਦਾ ਕੀਤਾ ਜਾ ਸਕੇ।

ਇਹ ਲਾਗੂ ਕਰਨ ਦੇ ਤਜਰਬੇ ਤੁਹਾਨੂੰ ਆਰਕੀਟੈਕਚਰਲ ਪੈਟਰਨ, ਲਾਗੂ ਕਰਨ ਦੀਆਂ ਰਣਨੀਤੀਆਂ ਅਤੇ ਸਰਵੋਤਮ ਅਭਿਆਸਾਂ ਬਾਰੇ ਜਾਣਕਾਰੀ ਦਿੰਦੇ ਹਨ ਜੋ ਤੁਹਾਡੇ ਆਪਣੇ MCP ਪ੍ਰੋਜੈਕਟਾਂ ਵਿੱਚ ਲਾਗੂ ਕੀਤੇ ਜਾ ਸਕਦੇ ਹਨ। ਇਹ ਉਦਾਹਰਣ ਦਰਸਾਉਂਦੇ ਹਨ ਕਿ MCP ਸਿਰਫ਼ ਸਿਧਾਂਤਕ ਢਾਂਚਾ ਨਹੀਂ, ਸਗੋਂ ਅਸਲੀ ਕਾਰੋਬਾਰੀ ਸਮੱਸਿਆਵਾਂ ਦਾ ਇੱਕ ਪ੍ਰਯੋਗਿਕ ਹੱਲ ਹੈ।

## ਵਾਧੂ ਸਰੋਤ

- [Azure AI Travel Agents GitHub Repository](https://github.com/Azure-Samples/azure-ai-travel-agents)
- [Azure DevOps MCP Tool](https://github.com/microsoft/azure-devops-mcp)
- [Playwright MCP Tool](https://github.com/microsoft/playwright-mcp)
- [Microsoft Docs MCP Server](https://github.com/MicrosoftDocs/mcp)
- [MCP Community Examples](https://github.com/microsoft/mcp)

ਅਗਲਾ: Hands on Lab [Streamlining AI Workflows: Building an MCP Server with AI Toolkit](../10-StreamliningAIWorkflowsBuildingAnMCPServerWithAIToolkit/README.md)

**ਅਸਵੀਕਾਰੋਪਣ**:  
ਇਹ ਦਸਤਾਵੇਜ਼ AI ਅਨੁਵਾਦ ਸੇਵਾ [Co-op Translator](https://github.com/Azure/co-op-translator) ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਅਨੁਵਾਦਿਤ ਕੀਤਾ ਗਿਆ ਹੈ। ਜਦੋਂ ਕਿ ਅਸੀਂ ਸਹੀਤਾ ਲਈ ਕੋਸ਼ਿਸ਼ ਕਰਦੇ ਹਾਂ, ਕਿਰਪਾ ਕਰਕੇ ਧਿਆਨ ਰੱਖੋ ਕਿ ਸਵੈਚਾਲਿਤ ਅਨੁਵਾਦਾਂ ਵਿੱਚ ਗਲਤੀਆਂ ਜਾਂ ਅਸਮਰਥਤਾਵਾਂ ਹੋ ਸਕਦੀਆਂ ਹਨ। ਮੂਲ ਦਸਤਾਵੇਜ਼ ਆਪਣੀ ਮੂਲ ਭਾਸ਼ਾ ਵਿੱਚ ਪ੍ਰਮਾਣਿਕ ਸਰੋਤ ਮੰਨਿਆ ਜਾਣਾ ਚਾਹੀਦਾ ਹੈ। ਮਹੱਤਵਪੂਰਨ ਜਾਣਕਾਰੀ ਲਈ, ਪੇਸ਼ੇਵਰ ਮਨੁੱਖੀ ਅਨੁਵਾਦ ਦੀ ਸਿਫਾਰਸ਼ ਕੀਤੀ ਜਾਂਦੀ ਹੈ। ਅਸੀਂ ਇਸ ਅਨੁਵਾਦ ਦੀ ਵਰਤੋਂ ਤੋਂ ਉਤਪੰਨ ਕਿਸੇ ਵੀ ਗਲਤਫਹਮੀ ਜਾਂ ਗਲਤ ਵਿਆਖਿਆ ਲਈ ਜ਼ਿੰਮੇਵਾਰ ਨਹੀਂ ਹਾਂ।