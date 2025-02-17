# Github Copilot

[Custom Instructions for Github Copilot in VSCode](https://code.visualstudio.com/docs/copilot/copilot-customization)

## Additional Code Instruction Files

- Add this to `settings.json` with the filepath to the rule

```json
"github.copilot.chat.codeGeneration.instructions": [
  {
    "file": ".github/<filename>.md"
  }
]
```

## Prompt Files

- Add `"chat.promptFiles": true` to `settings.json`
- Put prompt files in `.github/prompts` and label `<promptname>.prompt.md`