# Capstone project documentation

Store the project's implementation steps, design decisions, verification results, and final-report material in this folder.

## Document index

| Document | Purpose | Status |
| --- | --- | --- |
| [Architecture](architecture.md) | Architecture overview, diagram creation approach, complete connection register, implementation sequence, and evidence checklist | Design documented; deployment evidence pending |

The editable diagram and its exported image remain in [Architecture](../Architecture/). Link to these files from documents rather than maintaining duplicate copies.

## Adding future documents

Use descriptive Markdown filenames, for example `infrastructure.md`, `jenkins-pipeline.md`, `kubernetes-deployment.md`, `monitoring.md`, `security.md`, and `testing-and-recovery.md`. These are suggested future documents; they have not been created yet.

For each implementation step, record:

1. Date, objective, and prerequisites.
2. Configuration or commands used, including the relevant source-file paths and commit.
3. Expected outcome and observed result.
4. Evidence such as a screenshot, test output, or pipeline-run link.
5. Issues encountered, resolution, and any remaining work.

Mark work as **planned**, **implemented**, or **verified**. Keep credentials, access tokens, Terraform state, and unredacted secret values out of documentation and screenshots. Add evidence under this folder when it becomes available and link it from the relevant document.
