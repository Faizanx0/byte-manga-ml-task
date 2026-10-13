# Manga Task — Experiment Notes

## Setup
- Model: Qwen/Qwen2.5-VL-3B-Instruct
- Environment: Google Colab with a Tesla T4 GPU
- Model loading: 4-bit quantization
- Data: A small pilot of 3 sequences for prompt experiments

## Preliminary experiments

I compared different prompting and output formats on 3 pilot sequences.

| Experiment | Text/order score | Balanced joint F1 | Speaker accuracy | Joint F1 | Matched token coverage |
|---|---:|---:|---:|---:|---:|
| Plain-text transcription baseline | 0.37194 | 0.06594 | 0.3910 | 0.21689 | 0.55389 |
| Three-page sequence-level JSON | 0.25095 | 0.03889 | 0.45095 | 0.13099 | 0.26166 |
| One-page JSON with speaker labels | 0.414539 | 0.063347 | 0.353569 | 0.188171 | 0.565207 |
| Tweaked speaker prompt | 0.423633 | 0.063263 | 0.369634 | 0.188104 | 0.553914 |
| Conservative one-page JSON, UNKNOWN speakers | 0.422528 | 0.062077 | 0.380148 | 0.205096 | 0.549570 |

These results are preliminary because they were measured on only 3 pilot
sequences. They should not be treated as a reliable estimate of performance
on the full test set.

## Final inference
The submitted predictions were generated using the Qwen2.5-VL model in
Google Colab. The output was checked for valid JSONL structure, 15 test
sequences, and 3 page lists per sequence. Speaker labels in the final
predictions were UNKNOWN.
