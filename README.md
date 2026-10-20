# AI Workflow Notes

Practical templates for planning, recording and reviewing AI-assisted experiments.
The aim is to make a result inspectable: what was supplied, what changed, how it
was checked, and what remains unknown.

This is a starter collection, not a benchmark or a claim of validated model performance.

## Start here

1. Copy the [experiment template](templates/experiment.md) and define the acceptance criteria before running a model.
2. Freeze the input and record the model/version and settings that are actually available.
3. Save the original output before editing it. Record any manual changes separately.
4. Apply the [review checklist](checklists/review.md), keeping factual, technical and visual checks separate.
5. Record a pass, fail, partial result or unknown, with evidence and limitations.

| Resource | Use |
| --- | --- |
| [Experiment template](templates/experiment.md) | One task, fixed inputs, explicit success criteria |
| [Comparison template](templates/comparison.md) | Compare candidates using the same inputs and rubric |
| [Evidence log](templates/evidence-log.md) | Separate source-backed facts from inference |
| [Review checklist](checklists/review.md) | Check correctness, usability and disclosure before publishing |
| [Reference-first visual workflow](workflows/reference-first.md) | Preserve a supplied design and label reconstructed areas |
| [Research workflow](workflows/research.md) | Turn a question into claims that can be verified |
| [Illustrative experiment](examples/csv-summary-experiment.md) | A worked specification using fictional data; no model run is claimed |

## Recording rules

- Use `unknown` when a UI or API does not expose a model version or setting.
- Include timestamps with timezone, and distinguish source dates from retrieval dates.
- Record failures and retries; do not select a winner using only its best output.
- A deterministic validator checks encoded rules; it does not prove the rules are correct.
- Prompt and model settings alone do not guarantee an identical rerun.
- Keep raw private inputs, credentials and internal URLs out of public examples.

## Scope

The collection covers text research, structured summaries and visual asset
review. It does not contain provider-specific API integrations or automated agents.
Templates can be used manually with any tool that lets you save inputs and outputs.

## По-русски

Набор шаблонов для ИИ-экспериментов: постановка задачи, одинаковые условия
сравнения, журнал источников и проверка результата. Заполняйте только реально
известные параметры. Примеры учебные и не выдают вымышленные прогоны за проведённые.

## Contributing

Suggest changes with a small, reproducible example and explain which failure the
change prevents. Use synthetic or explicitly public input. Keep templates short
enough to use in a real experiment.

## License

[MIT](LICENSE).
