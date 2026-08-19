# MINISFORUM System

## Status

Initial sanitized profile available.

## Intended Role

Lightweight through medium local AI workloads and Windows x64 AI development.

## Hardware Profile

| Component | Verified specification |
| --- | --- |
| Manufacturer | Micro Computer (HK) Tech Limited |
| Model | AI Series |
| CPU | AMD Ryzen AI 9 HX 370 w/ Radeon 890M |
| Architecture | AMD64 / x64 |
| Memory | 64 GB class; 61.6 GiB total physical memory observed |
| GPU | AMD Radeon(TM) 890M Graphics |
| GPU memory | Pending verification |
| NPU or accelerator | Pending verification |
| Storage | C: system volume, approximately 951.6 GiB usable; approximately 757.0 GiB free at verification |

## Operating System

| Component | Verified value |
| --- | --- |
| Edition | Windows Pro |
| Version | 25H2 |
| Build | 26200.9168 |
| Architecture | x64 |

## AI Runtimes

| Runtime | Version | Status |
| --- | --- | --- |
| Ollama | 0.24.0 | Installed and available |
| Python | 3.13.13 | Installed and available |
| Container runtime | Docker 29.4.1 | Installed; config access pending verification |

## Installed Models

| Model tag | Size | Status |
| --- | --- | --- |
| deepseek-r1:8b | 5.2 GB | Installed |
| llama3.1:8b | 4.9 GB | Installed |

Model digests should be captured in benchmark records before comparing results across systems.

## Intended Workloads

- Local Ollama model experimentation
- Lightweight through medium local language-model workloads
- Retrieval, embedding, and technical-writing support
- Windows x64 development workflows
- Comparative benchmarking against the Surface ARM64, Lenovo Legion, and Surface Laptop Studio profiles
- Runtime compatibility checks for AMD Ryzen AI and Radeon integrated graphics systems

## Known Limitations

- GPU acceleration for Ollama was not verified during this profile pass.
- NPU availability and runtime support were not verified during this profile pass.
- GPU memory was not verified during this profile pass.
- CPU physical core topology was not available through the sandboxed diagnostics used for this profile.
- No inference benchmarks have been recorded yet for this system.
- Thermal and power-mode behavior are pending controlled testing.

## Verification

- Verified date: 2026-08-19
- Sanitized sources: Windows registry hardware and OS keys; .NET runtime architecture and memory APIs; PowerShell filesystem capacity query; Ollama CLI; Python CLI; Git CLI; Docker CLI.

Do not include serial numbers, product identifiers, hostnames, usernames, email addresses, network identifiers, credentials, or raw diagnostic exports.
