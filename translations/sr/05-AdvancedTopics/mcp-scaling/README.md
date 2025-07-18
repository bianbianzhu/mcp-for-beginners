<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "cd973a4e381337c6a3ac2443e7548e63",
  "translation_date": "2025-07-14T02:33:28+00:00",
  "source_file": "05-AdvancedTopics/mcp-scaling/README.md",
  "language_code": "sr"
}
-->
## Распоређена архитектура

Распоређене архитектуре подразумевају више MCP чворова који заједно раде на обради захтева, дељењу ресурса и обезбеђивању резерве. Овај приступ побољшава скалабилност и отпорност на грешке тако што омогућава чворовима да комуницирају и координишу се кроз распоређени систем.

Погледајмо пример како имплементирати распоређену MCP сервер архитектуру користећи Redis за координацију.

## Шта следи

- [5.8 Безбедност](../mcp-security/README.md)

**Одрицање од одговорности**:  
Овај документ је преведен коришћењем AI сервиса за превођење [Co-op Translator](https://github.com/Azure/co-op-translator). Иако се трудимо да превод буде тачан, молимо вас да имате у виду да аутоматски преводи могу садржати грешке или нетачности. Оригинални документ на његовом изворном језику треба сматрати ауторитетним извором. За критичне информације препоручује се професионални људски превод. Нисмо одговорни за било каква неспоразума или погрешна тумачења настала коришћењем овог превода.