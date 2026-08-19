# Benchmark Methodology

## Objective

Produce comparable, reproducible measurements across AI Lab systems without overstating differences.

## Required Controls

Every comparison must hold constant:

- Model and exact tag or digest
- Quantization
- Runtime and version
- Context length
- Prompt or dataset
- Generation parameters
- Warm-up procedure
- Number of measured runs
- Power mode
- Measurement tooling

## Required Measurements

Record, when available:

- Time to first token
- Prompt-processing rate
- Generation tokens per second
- Total elapsed time
- Peak system memory
- Peak accelerator memory
- CPU, GPU, or NPU utilization
- Power and thermal observations
- Failures and anomalous runs

## Procedure

1. Pull the latest system profile.
2. Confirm the runtime and model identity.
3. Record the benchmark configuration before running.
4. Perform an unmeasured warm-up run when appropriate.
5. Run the planned number of measured repetitions.
6. Preserve individual results and calculate summary statistics.
7. Do not discard failures or outliers without a documented rule.
8. Store the completed record under `benchmarks/results/`.
9. Link the record from `models/benchmark-results.md`.

Use `../templates/benchmark-record.md` for each benchmark.
