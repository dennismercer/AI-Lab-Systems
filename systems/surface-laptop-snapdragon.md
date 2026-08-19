# Microsoft Surface Laptop, 7th Edition

## Status

Initial sanitized profile verified on 2026-08-16.

## Intended Role

Heavy-work mobile system and ARM64 local AI experimentation.

## Hardware Profile

| Component | Verified specification |
| --- | --- |
| Manufacturer | Microsoft |
| Model | Surface Laptop, 7th Edition |
| Processor | Snapdragon X Elite X1E80100 |
| CPU | 12 cores, up to approximately 3.4 GHz |
| Architecture | ARM64 |
| Memory | 64 GB |
| GPU | Qualcomm Adreno X1-85 |
| GPU memory | Shared system memory; dedicated capacity not reported |
| NPU | Pending verification |
| Display | 2496 x 1664, up to 120 Hz |
| Storage | Samsung 1 TB-class SSD |
| Usable system volume | Approximately 951.6 GB |
| Firmware | UEFI |
| Virtualization | Hypervisor present |

## Operating System

| Component | Verified value |
| --- | --- |
| Edition | Windows 11 Pro |
| Display version | 25H2 |
| Build | 26200 |
| Architecture | ARM64 |

## AI Runtimes

| Runtime | Version | Status |
| --- | --- | --- |
| Ollama client | 0.32.5 | Reported installed |
| Python | Pending verification | Not yet inventoried |
| Container runtime | Pending verification | Not yet inventoried |

## Installed Models

Pending verification. Model names, exact tags, digests, quantization, and storage requirements should be recorded after running `ollama list` and sanitizing the output.

## Intended Workloads

- Research and technical writing
- Software development
- Local retrieval and embedding workloads
- Lightweight through medium local language models
- ARM64 compatibility testing
- X-CTIF development and controlled experimentation

## Known Limitations

- Windows ARM64 currently has fewer Ollama acceleration options than supported NVIDIA and AMD systems.
- Inference should be treated as CPU-bound unless runtime diagnostics demonstrate active accelerator use.
- GPU memory is shared and was not reported as dedicated VRAM by the collected Windows diagnostic.
- NPU availability to the selected AI runtime has not been verified.

## Verification Sources

This profile was derived from sanitized local outputs for:

- `Get-ComputerInfo`
- `Win32_ComputerSystem`
- `Win32_Processor`
- `Win32_VideoController`
- `Get-PhysicalDisk`
- `Get-Volume`
- User-reported Ollama client version

Serial numbers, product identifiers, hostnames, account information, driver paths, and transient utilization values were intentionally excluded.
