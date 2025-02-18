# AI Setup

## Github Copilot

[Custom Instructions for Github Copilot in VSCode](https://code.visualstudio.com/docs/copilot/copilot-customization)

### Additional Code Instruction Files

- Add this to `settings.json` with the filepath to the rule

```json
"github.copilot.chat.codeGeneration.instructions": [
  {
    "file": ".github/<filename>.md"
  }
]
```

- Add this to `settings.json` for #codebase to work in copilot edit
```json
"github.copilot.chat.edits.codesearch.enabled": true
```

### Prompt Files

- To enable prompt files add this to `settings.json`
```json
"chat.promptFiles": true
```

- Put prompt files in `.github/prompts` and label `<promptname>.prompt.md`
- To add prompt file:
  1. Inside Copilot Chat select the paperclip icon or `ctrl-/`
  2. Select `Prompt...`
  3. Select prompt from drop down

## Prompt Library

[takeoffai prompt library](https://www.jointakeoff.com/prompts)

1. [Request Prompt](./prompt-library/request-prompt.md)
2. [Spec Prompt](./prompt-library/spec-prompt.md)
3. [Planner Prompt](./prompt-library/planner-prompt.md)
4. [Codegen Prompt](./prompt-library/codegen-prompt.md) or [Codegen Prompt (XML)](./prompt-library/codegen-xml-prompt.md)
5. [Review Prompt](./prompt-library/review-prompt.md)
