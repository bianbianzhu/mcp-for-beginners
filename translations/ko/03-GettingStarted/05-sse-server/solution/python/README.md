<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "d700e180ce74b2675ce51a567a36c9e4",
  "translation_date": "2025-07-13T20:14:01+00:00",
  "source_file": "03-GettingStarted/05-sse-server/solution/python/README.md",
  "language_code": "ko"
}
-->
# 이 샘플 실행하기

`uv` 설치를 권장하지만 필수는 아닙니다. 자세한 내용은 [설명](https://docs.astral.sh/uv/#highlights)을 참고하세요.

## -0- 가상 환경 만들기

```bash
python -m venv venv
```

## -1- 가상 환경 활성화하기

```bash
venv\Scrips\activate
```

## -2- 의존성 설치하기

```bash
pip install "mcp[cli]"
```

## -3- 샘플 실행하기

```bash
mcp run server.py
```

## -4- 샘플 테스트하기

한 터미널에서 서버가 실행 중일 때, 다른 터미널을 열고 다음 명령어를 실행하세요:

```bash
mcp dev server.py
```

이 명령어는 샘플을 테스트할 수 있는 시각적 인터페이스가 포함된 웹 서버를 시작합니다.

서버가 연결되면:

- 도구 목록을 확인하고 `add`를 실행해 보세요. 인수로 2와 4를 넣으면 결과로 6이 나와야 합니다.
- resources와 resource template로 이동해 get_greeting을 호출하고 이름을 입력하면, 입력한 이름이 포함된 인사말을 볼 수 있습니다.

### CLI 모드에서 테스트하기

실행한 inspector는 사실 Node.js 앱이며, `mcp dev`는 이를 감싸는 래퍼입니다.

다음 명령어로 CLI 모드에서 직접 실행할 수 있습니다:

```bash
npx @modelcontextprotocol/inspector --cli http://localhost:8000/sse --method tools/list
```

이 명령어는 서버에서 사용 가능한 모든 도구를 나열합니다. 다음과 같은 출력이 보여야 합니다:

```text
{
  "tools": [
    {
      "name": "add",
      "description": "Add two numbers",
      "inputSchema": {
        "type": "object",
        "properties": {
          "a": {
            "title": "A",
            "type": "integer"
          },
          "b": {
            "title": "B",
            "type": "integer"
          }
        },
        "required": [
          "a",
          "b"
        ],
        "title": "addArguments"
      }
    }
  ]
}
```

도구를 호출하려면 다음과 같이 입력하세요:

```bash
npx @modelcontextprotocol/inspector --cli http://localhost:8000/sse --method tools/call --tool-name add --tool-arg a=1 --tool-arg b=2
```

다음과 같은 출력이 나타납니다:

```text
{
  "content": [
    {
      "type": "text",
      "text": "3"
    }
  ],
  "isError": false
}
```

> ![!TIP]
> inspector를 브라우저 대신 CLI 모드에서 실행하는 것이 보통 훨씬 빠릅니다.
> inspector에 대해 더 알아보려면 [여기](https://github.com/modelcontextprotocol/inspector)를 참고하세요.

**면책 조항**:  
이 문서는 AI 번역 서비스 [Co-op Translator](https://github.com/Azure/co-op-translator)를 사용하여 번역되었습니다. 정확성을 위해 최선을 다하고 있으나, 자동 번역에는 오류나 부정확한 부분이 있을 수 있음을 유의하시기 바랍니다. 원문은 해당 언어의 원본 문서가 권위 있는 출처로 간주되어야 합니다. 중요한 정보의 경우 전문적인 인간 번역을 권장합니다. 본 번역 사용으로 인해 발생하는 오해나 잘못된 해석에 대해 당사는 책임을 지지 않습니다.