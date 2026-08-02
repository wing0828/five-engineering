# Five Engineering

Five Engineering is a portable Agent Skill for making complex AI work more reliable in Codex and Claude Code through five nested layers:

1. Prompt engineering
2. Context engineering
3. Harness engineering
4. Loop engineering
5. Graph engineering

It helps an agent turn an ambiguous request into a testable contract, gather bounded context, build verification into execution, iterate without repeating failed attempts, and coordinate independent work safely.

## What you gain

- **Clearer requirements** - turn an ambiguous request into observable completion criteria before execution starts.
- **Focused context** - keep only the files, decisions, constraints, and evidence needed for the next decision.
- **Verification-first execution** - connect every meaningful change to tests, diagnostics, or manual checks.
- **Controlled iteration** - change the hypothesis or method after failure instead of repeating the same attempt.
- **Explicit stop conditions** - finish when the criteria pass and report precise evidence when progress is blocked.
- **Safer multi-agent coordination** - define ownership, dependencies, merge points, and review gates for independent work.
- **Auditable handoffs** - report outcomes together with verification evidence, assumptions, limitations, and remaining risks.

Five Engineering does not add new tools or guarantee a better answer by itself. It gives Codex and Claude Code a reusable operating method for making complex work more explicit, testable, and reviewable.

## What you can build

- **Verified implementation workflows** for features, bug fixes, refactors, and migrations
- **Research pipelines** that preserve source quality, decisions, open questions, and evidence
- **Test-and-repair loops** that continue until checks pass or a defined stop condition is reached
- **Long-running automations** with bounded context, progress evidence, retry rules, and clear failure reports
- **Multi-agent delivery systems** with separate ownership for implementation, review, QA, and integration
- **Release and quality gates** that connect changes to tests, diagnostics, manual observation, and approval
- **Reusable project playbooks** that apply the same execution discipline across Codex and Claude Code

Examples include implementing a feature until its tests pass, diagnosing a regression without repeating failed guesses, migrating multiple modules with independent verification, producing a source-backed technical report, or coordinating several agents into one reviewed result.

## 설치하면 얻는 것

- 모호한 요청을 관찰 가능한 완료 조건으로 구체화합니다.
- 다음 판단에 필요한 파일과 근거만 유지해 컨텍스트 노이즈를 줄입니다.
- 구현 전에 테스트, 진단 또는 수동 확인 방법을 연결합니다.
- 실패 원인을 바꾸지 않은 반복 시도를 방지합니다.
- 완료 조건과 중단 조건을 명확히 하고, 막혔을 때 누적된 근거를 보고합니다.
- 멀티에이전트 작업의 담당 범위, 의존성, 병합 지점과 검토 게이트를 설계합니다.

## 만들어볼 수 있는 것

- 테스트 통과까지 이어지는 기능 구현·버그 수정 워크플로
- 출처와 판단 근거가 남는 리서치 파이프라인
- 실패 전략을 갱신하며 동작하는 테스트·수정 반복 루프
- 중단 조건과 진행 증거를 갖춘 장기 자동화
- 구현, 리뷰, QA와 통합 역할이 분리된 멀티에이전트 시스템
- 리팩터링, 마이그레이션과 릴리스를 위한 검증 게이트
- Codex와 Claude Code에서 공통으로 사용하는 프로젝트 실행 플레이북

## Install in Codex

Ask Codex:

```text
Install the five-engineering skill from https://github.com/wing0828/five-engineering/tree/main/skills/five-engineering
```

Codex can install it from the public GitHub path using its built-in skill installer. The skill becomes available on the next turn after installation.

## Manual installation

Clone this repository, then copy `skills/five-engineering` into your Codex skills directory as `five-engineering`:

- Windows: `%USERPROFILE%\.codex\skills\five-engineering`
- macOS/Linux: `~/.codex/skills/five-engineering`

The installed directory must contain `SKILL.md` directly.

## Use

Invoke it explicitly:

```text
Use $five-engineering to plan and implement this feature with clear success criteria and verification.
```

It can also be selected automatically for complex implementation, research, automation, debugging, and multi-agent work.

## Install in Claude Code

### Plugin installation

Run these commands inside Claude Code:

```text
/plugin marketplace add wing0828/five-engineering
/plugin install five-engineering@five-engineering-marketplace
/reload-plugins
```

Invoke the plugin skill explicitly:

```text
/five-engineering:five-engineering
```

Claude can also invoke it automatically when the request matches its description.

### Personal skill installation

Alternatively, clone this repository and copy `skills/five-engineering` into your personal Claude Code skills directory:

- Windows: `%USERPROFILE%\.claude\skills\five-engineering`
- macOS/Linux: `~/.claude/skills/five-engineering`

Then invoke it without a plugin namespace:

```text
/five-engineering
```

## Repository layout

```text
.claude-plugin/
  marketplace.json
  plugin.json
skills/
  five-engineering/
    SKILL.md
    agents/
      openai.yaml
```

## License

MIT License. See [LICENSE](LICENSE).
