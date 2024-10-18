# ai-commit

Conv2
```text
Using the diff provided below, create a concise commit message following the Conventional Commits format (e.g., "🐛 fix(types): corrected imports in types"). Begin the message with an appropriate emoji to highlight the nature of the changes. Use the past tense and first person for articulation. Ensure the line does not exceed 74 characters. Write in {locale}. If uncertain about the precise wording, offer several commit message options. If the diff does not provide enough information to determine the commit's purpose, focus on the specific changes made rather than attempting to guess the intent. Utilize single-line code blocks to denote variable names, file paths, or any code-related elements.

## Internal Terminology List:
<put your terminology here, if needed>

## Emoji Usage Guide:
- 🐛 fix: For bug fixes.
- ✨ feat: For new features.
- 📄 docs: For documentation changes.
- ♻️ refactor: For code refactoring without changing functionality.
- 🚀 perf: For performance improvements.
- 🔒 security: For security-related fixes.
- 🚧 chore: For maintenance tasks.
- 🧪 test: For tests

{Author's notes: "$hint"}

Your response should consist solely of the commit message, without additional descriptions or formatting. Avoid verbosity, here is an output of `git diff --staged` command:
{diff}
```

Detailed2

```text
Write a commit message that accurately summarizes the changes made in the given `git diff` output, following the best practices and conventional commit convention as described below. Your response should look like this (no codeblock), the response must be use the language {locale} :

<type>(<optional scope>): <subject>

<BODY (bullet points)>

Example:
chore(deps): update library versions

- Update Kotlin version from `0.1.0` to `0.2.0`

Here are some best practices for writing commit messages:
- Write clear, concise, and descriptive messages that explain the changes made in the commit
- Use the present tense and active voice in the message, for example, "fix bug" instead of "fixed bug"
- Use the imperative mood, which gives the message a sense of command, e.g. "add feature" instead of "added feature"
- Limit the subject line to 72 characters or less
- Don't capitalize the first letter
- Do not end the subject line with a period
- Any numbers or file names should be enclosed in backticks, e.g. "`0.1`" instead of "0.1", "`README.md`" instead of "README.md"
- Limit the body of the message to 256 characters or less
- Use a blank line between the subject and the body of the message
- Use the body of the message to provide additional context or explain the reasoning behind the changes
- Avoid using general terms like "update" or "change" in the subject line, be specific about what was updated or changed
- Explain, What was done at a glance in the subject line, and provide additional context in the body of the message
- Why the change was necessary in the body of the message
- The details about what was done in the body of the message
- Any useful details concerning the change in the body of the message
- Use a hyphen (-) for the bullet points in the body of the message

Here are the commit types you can choose from:
- build: Changes that affect the build system or external dependencies (Usually associated with changes to build scripts, e.g. Gradle, NPM, Cargo)
- chore: Miscellaneous commits, updating dependencies, copyrights or other repo configs (example scopes: project, deps)
- ci: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, GitHub Actions)
- docs: Non-code changes, such as fixing typos or adding new documentation (example scopes: Markdown file)
- feat: A commit of the type feat introduces a new feature to the codebase
- fix: A commit of the type fix patches a bug in your codebase
- perf: A code change that improves performance
- refactor: A code change that neither fixes a bug nor adds a feature
- style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- test: Adding missing tests or correcting existing tests

Here is the output of the `git diff`:
--
{diff}
```

Detailed3
```text
Write a concise, clear, and informative commit message based on the conventional commit specification.

- Format: `<type>(<scope>): <description>`
- Accurately classify the commit type (see below). If uncertain, provide the best guess:
    - 🐛 fix: For bug fixes.
    - ✨ feat: For new features.
    - 📄 docs: For documentation changes.
    - ♻️ refactor: For code refactoring without changing functionality.
    - 🚀 perf: For performance improvements.
    - 🔒 security: For security-related fixes.
    - 🚧 chore: For maintenance tasks.
    - 🧪 test: For tests
- Accurately classify the commit scope (see below). If uncertain, provide the best guess:
    - Noun describing a section of the codebase.
    - E.g.:
      areas, contacts, containers, orders, prices, settings, statistics, core, ui, config, yarn, gradle, deps,
      github-actions, release.
- Use present tense and active voice.
- Subject
    - Start with a lowercase letter and avoid ending with a period.
    - Encapsulate any code, numbers, or filenames in backticks.
- Body
    - Only add really relevant information, that are not already covered by the subject.
    - If it really matters. provide a detailed explanation of what was changed, why it was changed, and its impact.

Each line, MUST NOT exceed **72** characters; Wrap in the body if necessary!

Do not embed the response in a code block.

`git diff --staged`:

{diff}
```