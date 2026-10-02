# chatbot

OpenAI GPT-3.5 기반 **Streamlit 채팅 앱**입니다. Streamlit 공식 챗봇 템플릿을 기반으로 합니다.

## 동작

- 화면에서 **OpenAI API Key**를 입력하면 활성화됩니다 (키는 서버에 저장되지 않고 세션 중에만 사용).
- `st.session_state`에 대화 기록을 유지하고, 전체 기록을 `gpt-3.5-turbo`에 전달합니다.
- 응답은 스트리밍(`st.write_stream`)으로 출력합니다.

## 파일

| 파일 | 설명 |
|---|---|
| `streamlit_app.py` | 앱 본체 |
| `requirements.txt` | `streamlit`, `openai` |
| `LICENSE` | Apache License 2.0 |

## 실행

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
```

키를 매번 입력하지 않으려면 `.streamlit/secrets.toml`에 저장하고 `st.secrets`로 읽도록 수정하세요. `secrets.toml`은 커밋하지 마세요.

## 참고

- 사용 모델은 `gpt-3.5-turbo` 고정입니다. 필요하면 `streamlit_app.py`에서 변경하세요.
