<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "4c4da5949611d91b06d8a5d450aae8d6",
  "translation_date": "2025-07-13T21:22:11+00:00",
  "source_file": "03-GettingStarted/06-http-streaming/solution/python/README.md",
  "language_code": "sk"
}
-->
# Spustenie tohto príkladu

Tu je návod, ako spustiť klasický HTTP streaming server a klienta, ako aj MCP streaming server a klienta pomocou Pythonu.

### Prehľad

- Nastavíte MCP server, ktorý bude klientovi streamovať notifikácie o priebehu spracovania položiek.
- Klient bude zobrazovať každú notifikáciu v reálnom čase.
- Tento návod pokrýva požiadavky, nastavenie, spustenie a riešenie problémov.

### Požiadavky

- Python 3.9 alebo novší
- Python balík `mcp` (nainštalujete pomocou `pip install mcp`)

### Inštalácia a nastavenie

1. Naklonujte repozitár alebo si stiahnite súbory riešenia.

   ```pwsh
   git clone https://github.com/microsoft/mcp-for-beginners
   ```

1. **Vytvorte a aktivujte virtuálne prostredie (odporúčané):**

   ```pwsh
   python -m venv venv
   .\venv\Scripts\Activate.ps1  # On Windows
   # or
   source venv/bin/activate      # On Linux/macOS
   ```

1. **Nainštalujte potrebné závislosti:**

   ```pwsh
   pip install "mcp[cli]"
   ```

### Súbory

- **Server:** [server.py](../../../../../../03-GettingStarted/06-http-streaming/solution/python/server.py)
- **Klient:** [client.py](../../../../../../03-GettingStarted/06-http-streaming/solution/python/client.py)

### Spustenie klasického HTTP streaming servera

1. Prejdite do adresára riešenia:

   ```pwsh
   cd 03-GettingStarted/06-http-streaming/solution
   ```

2. Spustite klasický HTTP streaming server:

   ```pwsh
   python server.py
   ```

3. Server sa spustí a zobrazí:

   ```
   Starting FastAPI server for classic HTTP streaming...
   INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
   ```

### Spustenie klasického HTTP streaming klienta

1. Otvorte nový terminál (aktivujte rovnaké virtuálne prostredie a adresár):

   ```pwsh
   cd 03-GettingStarted/06-http-streaming/solution
   python client.py
   ```

2. Mali by ste vidieť postupne vypisované streamované správy:

   ```text
   Running classic HTTP streaming client...
   Connecting to http://localhost:8000/stream with message: hello
   --- Streaming Progress ---
   Processing file 1/3...
   Processing file 2/3...
   Processing file 3/3...
   Here's the file content: hello
   --- Stream Ended ---
   ```

### Spustenie MCP streaming servera

1. Prejdite do adresára riešenia:
   ```pwsh
   cd 03-GettingStarted/06-http-streaming/solution
   ```
2. Spustite MCP server s transportom streamable-http:
   ```pwsh
   python server.py mcp
   ```
3. Server sa spustí a zobrazí:
   ```
   Starting MCP server with streamable-http transport...
   INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
   ```

### Spustenie MCP streaming klienta

1. Otvorte nový terminál (aktivujte rovnaké virtuálne prostredie a adresár):
   ```pwsh
   cd 03-GettingStarted/06-http-streaming/solution
   python client.py mcp
   ```
2. Mali by ste vidieť notifikácie vypisované v reálnom čase, ako server spracováva jednotlivé položky:
   ```
   Running MCP client...
   Starting client...
   Session ID before init: None
   Session ID after init: a30ab7fca9c84f5fa8f5c54fe56c9612
   Session initialized, ready to call tools.
   Received message: root=LoggingMessageNotification(...)
   NOTIFICATION: root=LoggingMessageNotification(...)
   ...
   Tool result: meta=None content=[TextContent(type='text', text='Processed files: file_1.txt, file_2.txt, file_3.txt | Message: hello from client')]
   ```

### Kľúčové kroky implementácie

1. **Vytvorte MCP server pomocou FastMCP.**
2. **Definujte nástroj, ktorý spracuje zoznam a posiela notifikácie pomocou `ctx.info()` alebo `ctx.log()`.**
3. **Spustite server s `transport="streamable-http"`.**
4. **Implementujte klienta s handlerom správ, ktorý zobrazuje notifikácie hneď, ako prídu.**

### Prehľad kódu
- Server používa asynchrónne funkcie a MCP kontext na odosielanie aktualizácií priebehu.
- Klient implementuje asynchrónny handler správ na vypisovanie notifikácií a konečného výsledku.

### Tipy a riešenie problémov

- Používajte `async/await` pre neblokujúce operácie.
- Vždy ošetrujte výnimky na strane servera aj klienta pre väčšiu spoľahlivosť.
- Testujte s viacerými klientmi, aby ste videli aktualizácie v reálnom čase.
- Ak narazíte na chyby, skontrolujte verziu Pythonu a či sú všetky závislosti nainštalované.

**Vyhlásenie o zodpovednosti**:  
Tento dokument bol preložený pomocou AI prekladateľskej služby [Co-op Translator](https://github.com/Azure/co-op-translator). Aj keď sa snažíme o presnosť, prosím, majte na pamäti, že automatizované preklady môžu obsahovať chyby alebo nepresnosti. Originálny dokument v jeho pôvodnom jazyku by mal byť považovaný za autoritatívny zdroj. Pre kritické informácie sa odporúča profesionálny ľudský preklad. Nie sme zodpovední za akékoľvek nedorozumenia alebo nesprávne interpretácie vyplývajúce z použitia tohto prekladu.