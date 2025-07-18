<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "748c61250d4a326206b72b28f6154615",
  "translation_date": "2025-07-13T23:48:26+00:00",
  "source_file": "05-AdvancedTopics/README.md",
  "language_code": "sr"
}
-->
# Напредне теме у MCP

Ово поглавље покрива низ напредних тема у имплементацији Model Context Protocol (MCP), укључујући мултимодалну интеграцију, скалабилност, најбоље безбедносне праксе и интеграцију у предузећима. Ове теме су кључне за изградњу робусних и спремних за производ MCP апликација које могу да задовоље захтеве савремених AI система.

## Преглед

Ова лекција истражује напредне концепте у имплементацији Model Context Protocol-а, са фокусом на мултимодалну интеграцију, скалабилност, најбоље безбедносне праксе и интеграцију у предузећима. Ове теме су неопходне за изградњу MCP апликација за производњу које могу да поднесу сложене захтеве у пословним окружењима.

## Циљеви учења

До краја ове лекције, моћи ћете да:

- Имплементирате мултимодалне могућности у оквиру MCP фрејмворка
- Дизајнирате скалабилне MCP архитектуре за сценарије са великим оптерећењем
- Примените најбоље безбедносне праксе у складу са безбедносним принципима MCP-а
- Интегришете MCP са AI системима и фрејмворцима у предузећима
- Оптимизујете перформансе и поузданост у производним окружењима

## Лекције и пример пројеката

| Линк | Наслов | Опис |
|------|--------|-------|
| [5.1 Integration with Azure](./mcp-integration/README.md) | Интеграција са Azure | Научите како да интегришете свој MCP сервер на Azure |
| [5.2 Multi modal sample](./mcp-multi-modality/README.md) | MCP мултимодални примери | Примери за аудио, слике и мултимодалне одговоре |
| [5.3 MCP OAuth2 sample](../../../05-AdvancedTopics/mcp-oauth2-demo) | MCP OAuth2 демо | Минимална Spring Boot апликација која показује OAuth2 са MCP-ом, као Authorization и Resource Server. Демонстрира безбедно издавање токена, заштићене крајње тачке, деплојмент на Azure Container Apps и интеграцију са API Management-ом. |
| [5.4 Root Contexts](./mcp-root-contexts/README.md) | Root контексти | Сазнајте више о root контексту и како их имплементирати |
| [5.5 Routing](./mcp-routing/README.md) | Роутинг | Упознајте различите типове рутирања |
| [5.6 Sampling](./mcp-sampling/README.md) | Узорковање | Научите како да радите са узорковањем |
| [5.7 Scaling](./mcp-scaling/README.md) | Скалабилност | Сазнајте више о скалабилности |
| [5.8 Security](./mcp-security/README.md) | Безбедност | Осигурајте свој MCP сервер |
| [5.9 Web Search sample](./web-search-mcp/README.md) | Веб претрага MCP | Python MCP сервер и клијент који интегришу SerpAPI за претрагу веба, вести, производа и Q&A у реалном времену. Демонстрира мулти-алатску оркестрацију, интеграцију спољних API-ја и робусно руковање грешкама. |
| [5.10 Realtime Streaming](./mcp-realtimestreaming/README.md) | Стриминг | Стриминг података у реалном времену постао је неопходан у данашњем свету вођеном подацима, где послови и апликације захтевају тренутни приступ информацијама за правовремене одлуке. |
| [5.11 Realtime Web Search](./mcp-realtimesearch/README.md) | Веб претрага | Како MCP трансформише претрагу веба у реалном времену пружајући стандардизован приступ управљању контекстом између AI модела, претраживача и апликација. |
| [5.12  Entra ID Authentication for Model Context Protocol Servers](./mcp-security-entra/README.md) | Entra ID аутентификација | Microsoft Entra ID пружа робусно решење за управљање идентитетом и приступом у облаку, помажући да само овлашћени корисници и апликације могу да комуницирају са вашим MCP сервером. |
| [5.13 Azure AI Foundry Agent Integration](./mcp-foundry-agent-integration/README.md) | Интеграција Azure AI Foundry | Научите како да интегришете Model Context Protocol сервере са Azure AI Foundry агентима, омогућавајући моћну оркестрацију алата и AI могућности у предузећима са стандардизованим везама ка спољним изворима података. |

## Додатне референце

За најсвежије информације о напредним MCP темама, погледајте:
- [MCP документација](https://modelcontextprotocol.io/)
- [MCP спецификација](https://spec.modelcontextprotocol.io/)
- [GitHub репозиторијум](https://github.com/modelcontextprotocol)

## Кључне поуке

- Мултимодалне MCP имплементације проширују AI могућности изван обраде текста
- Скалабилност је неопходна за примене у предузећима и може се постићи хоризонталним и вертикалним скалирањем
- Комплетне безбедносне мере штите податке и обезбеђују правилну контролу приступа
- Интеграција у предузећима са платформама као што су Azure OpenAI и Microsoft AI Foundry побољшава MCP могућности
- Напредне MCP имплементације имају користи од оптимизованих архитектура и пажљивог управљања ресурсима

## Вежба

Дизајнирајте MCP имплементацију за предузеће за конкретан случај употребе:

1. Идентификујте мултимодалне захтеве за ваш случај употребе
2. Нагласите безбедносне контроле потребне за заштиту осетљивих података
3. Дизајнирајте скалабилну архитектуру која може да поднесе променљиво оптерећење
4. Испланирајте тачке интеграције са AI системима у предузећима
5. Документујте потенцијалне уске грла у перформансама и стратегије за њихово отклањање

## Додатни ресурси

- [Azure OpenAI документација](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Microsoft AI Foundry документација](https://learn.microsoft.com/en-us/ai-services/)

---

## Шта следи

- [5.1 MCP Integration](./mcp-integration/README.md)

**Одрицање од одговорности**:  
Овај документ је преведен коришћењем AI преводилачке услуге [Co-op Translator](https://github.com/Azure/co-op-translator). Иако се трудимо да превод буде тачан, молимо вас да имате у виду да аутоматски преводи могу садржати грешке или нетачности. Оригинални документ на његовом изворном језику треба сматрати ауторитетним извором. За критичне информације препоручује се професионални људски превод. Нисмо одговорни за било каква неспоразума или погрешна тумачења која произилазе из коришћења овог превода.