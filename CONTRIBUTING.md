# Contributing

This project welcomes contributions and suggestions. Most contributions require you to
agree to a Contributor License Agreement (CLA) declaring that you have the right to,
and actually do, grant us the rights to use your contribution. For details, visit
<https://cla.microsoft.com>.

When you submit a pull request, a CLA-bot will automatically determine whether you need
to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the
instructions provided by the bot. You will only need to do this once across all repositories using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)
or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Documentation checks

Run both checks from the repository root:

```shell
npx --yes markdownlint-cli2@0.22.1 "**/*.md"
npx --yes cspell@10.4.1 lint
```

The Markdown configuration preserves long paragraphs, tables, and copy/paste blocks, and permits the HTML used by the README banner and owner table. Scoped directives preserve the README's HTML preamble and Skillable's `+++URL+++` autotype links. Other rules, including MD028, remain enabled. Separate adjacent alert blocks with a normal paragraph rather than an unmarked blank line.

Correct spelling mistakes in the source text. Add only legitimate product names, technical terms, and identifiers to `cspell.json`. The original LAB665 screenshot filename containing a spelling error is preserved for attribution and exempted only in that attribution file.
