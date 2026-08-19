# AI Lab Systems

## Purpose

This repository documents the systems used in Dennis Mercer's personal AI lab, including hardware capabilities, intended workload roles, local AI runtimes, compatible models, and reproducible benchmark results.

It supports:

- Selecting the appropriate system for each workload
- Tracking local AI runtime and model compatibility
- Recording sanitized hardware and software configurations
- Comparing inference performance across systems
- Preserving reproducible setup and benchmark procedures
- Planning upgrades and workload placement

## Lab Systems

| System | Intended role | Status |
| --- | --- | --- |
| MINISFORUM system | Lightweight through medium local AI workloads and Windows x64 AI development | Initial profile available |
| Lenovo Legion | Heavyweight local AI workloads | Specifications pending |
| Microsoft Surface Laptop Studio | Windows mobile AI and development workstation | Specifications pending |
| Microsoft Surface Laptop, 7th Edition | Heavy-work mobile system and ARM64 local AI experimentation | Initial profile available |

## Microsoft Surface Laptop, 7th Edition

### Sanitized hardware profile

| Component | Specification |
| --- | --- |
| Processor | Snapdragon X Elite X1E80100 |
| CPU | 12 cores, up to approximately 3.4 GHz |
| Architecture | ARM64 |
| Memory | 64 GB |
| Graphics | Qualcomm Adreno X1-85 |
| Display | 2496 x 1664, up to 120 Hz |
| Storage | Samsung 1 TB-class SSD |
| Usable system volume | Approximately 951.6 GB |
| Operating system | Windows 11 Pro 25H2 |
| Local AI runtime | Ollama client 0.32.5 |

### Intended use

- Research and technical writing
- Software development
- Local retrieval and embedding workloads
- Lightweight through medium local language models
- ARM64 compatibility testing
- X-CTIF development and controlled experimentation

### Current limitation

Ollama on Windows ARM64 does not currently provide the same GPU or NPU acceleration options available on supported NVIDIA and AMD systems. Local inference should therefore be evaluated as primarily CPU-bound unless runtime diagnostics demonstrate otherwise.

## Repository Structure

```text
AI-Lab-Systems/
|-- README.md
|-- AGENTS.md
|-- systems/
|   |-- minisforum.md
|   |-- lenovo-legion.md
|   |-- surface-laptop-studio.md
|   `-- surface-laptop-snapdragon.md
|-- models/
|   |-- compatibility-matrix.md
|   `-- benchmark-results.md
|-- software/
|   |-- ollama.md
|   |-- python-environments.md
|   `-- development-tools.md
|-- benchmarks/
|   |-- methodology.md
|   `-- results/
`-- templates/
    |-- system-profile.md
    `-- benchmark-record.md
```

This structure is implemented and will be populated incrementally as verified system information and benchmark results become available.

## Adding or Updating a System

Each computer should update its own dedicated profile rather than placing complete diagnostic output directly in this README.

1. Clone or pull the latest version of this repository on the system being documented.
2. Read this README, especially the Privacy and Security requirements.
3. Collect current hardware, operating-system, storage, accelerator, and AI-runtime information.
4. Review and sanitize all diagnostic output before adding it to the repository.
5. Create or update the matching profile under `systems/`:
   - `systems/minisforum.md`
   - `systems/lenovo-legion.md`
   - `systems/surface-laptop-studio.md`
   - `systems/surface-laptop-snapdragon.md`
6. Update the Lab Systems summary table in this README only when the system role or profile status changes.
7. Commit the profile and summary-table update together with a clear message identifying the system.
8. Pull the latest changes before pushing. If another system is being updated concurrently, use a separate branch and pull request to avoid conflicting README edits.
9. Verify the rendered files on GitHub after the push.

Do not commit raw `Get-ComputerInfo`, CIM, storage, driver, or network exports. Preserve only sanitized, inventory-relevant values. When a value cannot be verified safely, mark it as pending rather than guessing.

## System Profile Requirements

Each system profile should record:

- Manufacturer and model
- Intended workload role
- CPU and architecture
- GPU and available VRAM
- NPU or other AI accelerator
- Installed memory
- Storage type and usable capacity
- Operating system and architecture
- AI runtimes and exact versions
- Installed local models
- Supported quantization formats
- Recommended context limits
- Observed performance
- Thermal or power considerations
- Known compatibility limitations
- Date the profile was verified

## Benchmarking Principles

Benchmark results should record:

- System profile revision
- Runtime and model versions
- Exact model tag or digest
- Quantization and context length
- Prompt or test-set identifier
- Generation parameters
- Tokens per second and time to first token
- Peak memory use
- CPU, GPU, or NPU utilization
- Power mode and thermal conditions
- Run count and summary statistics
- Failures, limitations, and anomalies

Results from different systems should not be compared unless the workload, model, quantization, context, and measurement procedure are equivalent.

## Privacy and Security

This repository must not contain:

- Device, BIOS, or storage serial numbers
- Windows product identifiers
- Account names or email addresses
- Computer or DNS host names
- IP or MAC addresses
- Credentials, keys, tokens, or certificates
- Private network topology
- Unsanitized diagnostic exports
- Employer-confidential, customer, or proprietary information

Raw diagnostic outputs must be reviewed and sanitized before publication.

## Data Quality

System specifications should be treated as verified only when supported by current diagnostic output or manufacturer documentation. Unknown values should remain marked as pending rather than inferred.

Hardware, drivers, operating systems, runtimes, and model support change over time. Material updates should include a verification date and source.

## Current Status

- Repository structure implemented
- Root Codex instructions added
- MINISFORUM system profile documented
- Surface Laptop ARM64 profile documented
- Placeholder profiles created for the remaining systems
- Model compatibility, software inventory, benchmark methodology, and reusable templates initialized
- Remaining Lenovo Legion and Surface Laptop Studio specifications and verified benchmark results pending
