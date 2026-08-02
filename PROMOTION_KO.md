# Five Engineering 홍보문

아래 문구는 필요한 부분만 복사해서 사용할 수 있습니다.

## 한 줄 소개

AI에게 일을 시키는 프롬프트를 넘어, 성공 기준부터 검증과 반복, 멀티에이전트 협업까지 설계하는 오픈소스 Agent Skill입니다.

## 짧은 SNS 게시물

AI가 그럴듯한 답만 내놓고 끝나는 것이 아쉬웠다면?

`Five Engineering`을 공개했습니다.

프롬프트, 컨텍스트, 하네스, 루프, 그래프의 5개 계층으로 AI 작업을 설계합니다.

- 모호한 요청을 검증 가능한 성공 기준으로 전환
- 필요한 컨텍스트만 선별
- 실행 전에 검증 방법 정의
- 같은 실패를 반복하지 않는 개선 루프
- 멀티에이전트 작업의 역할과 병합 지점 관리

Codex와 Claude Code에서 모두 사용할 수 있습니다.

https://github.com/wing0828/five-engineering

## 커뮤니티 소개 게시물

### Five Engineering을 공개합니다

AI 코딩 에이전트를 사용하다 보면 프롬프트 하나만 잘 쓰는 것으로 해결되지 않는 작업을 만나게 됩니다. 관련 파일을 어디까지 읽을지, 성공 여부를 어떻게 검증할지, 실패했을 때 무엇을 바꿔 다시 시도할지, 여러 에이전트의 결과를 어떻게 합칠지까지 함께 설계해야 합니다.

Five Engineering은 이 문제를 다섯 계층으로 정리한 오픈소스 Agent Skill입니다.

1. **Prompt Engineering** - 요청을 역할, 목표, 제약, 결과물과 성공 기준으로 구체화합니다.
2. **Context Engineering** - 다음 판단에 필요한 정보만 모으고 오래되거나 중복된 정보는 제거합니다.
3. **Harness Engineering** - 작업을 작은 결과 단위로 나누고 각 변경의 검증 방법을 미리 정의합니다.
4. **Loop Engineering** - 실행과 검증을 반복하되 같은 실패를 그대로 반복하지 않도록 통제합니다.
5. **Graph Engineering** - 독립 작업의 담당, 의존성, 병합 지점과 승인 게이트를 명확히 합니다.

설치하면 AI가 무조건 더 똑똑해지는 것은 아닙니다. 대신 복잡한 작업을 시작하기 전에 성공 기준을 세우고, 필요한 근거를 모으고, 변경을 검증하고, 실패와 협업을 관리하는 공통 작업 방식을 적용할 수 있습니다.

Codex와 Claude Code를 모두 지원하며 MIT 라이선스로 공개했습니다.

GitHub: https://github.com/wing0828/five-engineering

## 상세 출시 게시물

### 프롬프트 엔지니어링 다음에는 무엇이 필요할까?

좋은 프롬프트는 중요하지만, 실제 프로젝트에서는 그것만으로 충분하지 않았습니다.

AI가 관련 없는 파일까지 읽어 컨텍스트가 흐려지거나, 구현은 했지만 검증하지 않거나, 같은 실패를 표현만 바꿔 반복하거나, 여러 에이전트가 비슷한 작업을 중복하는 문제가 생깁니다.

Five Engineering은 AI 작업을 다음의 다섯 계층으로 운영하도록 돕습니다.

- **Prompt**: 무엇을 완료로 볼지 먼저 정의합니다.
- **Context**: 현재 판단에 필요한 근거만 유지합니다.
- **Harness**: 작업 단위와 검증 방법을 연결합니다.
- **Loop**: 실행, 검증, 가정 갱신을 통제된 방식으로 반복합니다.
- **Graph**: 병렬 작업의 소유권과 합류 지점을 관리합니다.

설치 후 기대할 수 있는 변화는 분명합니다.

- 모호한 요청이 관찰 가능한 성공 기준으로 바뀝니다.
- 구현 전에 테스트와 확인 방법을 함께 생각하게 됩니다.
- 실패 원인을 바꾸지 않은 재시도를 줄입니다.
- 작업이 막혔을 때 추측 대신 누적된 증거를 보고합니다.
- 멀티에이전트 작업에서 담당 범위와 검토 지점이 선명해집니다.
- Codex와 Claude Code에서 같은 작업 원칙을 재사용할 수 있습니다.

복잡한 구현, 디버깅, 리서치, 자동화와 멀티에이전트 작업을 더 명시적이고 검증 가능하게 운영하고 싶은 분들에게 유용합니다.

오픈소스로 공개했으며 설치 방법과 전체 지침은 GitHub에서 확인할 수 있습니다.

https://github.com/wing0828/five-engineering

## Claude Code 설치 안내용 문구

Claude Code에서 다음 명령으로 설치할 수 있습니다.

```text
/plugin marketplace add wing0828/five-engineering
/plugin install five-engineering@five-engineering-marketplace
/reload-plugins
```

설치 후 다음 명령으로 직접 호출합니다.

```text
/five-engineering:five-engineering
```

## Codex 설치 안내용 문구

Codex에 다음과 같이 요청합니다.

```text
Install the five-engineering skill from https://github.com/wing0828/five-engineering/tree/main/skills/five-engineering
```

설치 후 다음과 같이 명시적으로 적용할 수 있습니다.

```text
Use $five-engineering to plan and execute this task with explicit success criteria and verification.
```

## 핵심 표현 모음

- 프롬프트를 넘어 작업 시스템을 설계합니다.
- 완료 기준이 없는 실행을 검증 가능한 작업으로 바꿉니다.
- 같은 실패를 반복하지 않는 AI 작업 루프를 만듭니다.
- 멀티에이전트 협업에 소유권과 병합 지점을 부여합니다.
- 복잡한 AI 작업을 더 명시적이고 검토 가능하게 만듭니다.

## 해시태그 예시

`#FiveEngineering #AgentSkills #Codex #ClaudeCode #AIAgent #오픈소스 #개발자동화 #멀티에이전트`
