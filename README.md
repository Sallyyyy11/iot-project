# IoT Course Project — [PROJECT TITLE]

> HCMUT · Internet of Things · Semester 261 (2026–2027)  
> Instructor: Dr. Nguyễn Hòa Hưng  
> Status: **Planning — topic and hardware configuration not yet decided**

## Team and contribution records

| Role slot | Member (assign later) | Main responsibility (assign later) |
| --- | --- | --- |
| Member 1 | Unassigned | To be agreed |
| Member 2 | Unassigned | To be agreed |
| Member 3 | Unassigned | To be agreed |

Each person must commit work through their own GitHub account; do not push everything using one account. Record actual contributions and technology codes in `docs/task-assignment.md`.

## 1. Project objective and features

**Problem:** [Describe the real-world problem and users.]  
**System:** Multiple interacting devices using **ESP32-S3 (YoloUNO)** and **CoreIOT**.  
**Topology:** [Direct-to-CoreIOT / Local gateway / Hybrid — choose one].

| Feature ID | Verifiable feature | Component | Technology code(s) | Status |
| --- | --- | --- | --- | --- |
| F01 | [Describe measurement, frequency, output] | [Node] | [Txx] | Planned |
| F02 | [Describe inter-device or remote control behavior] | [Node/CoreIOT] | [Txx] | Planned |
| F03 | [Describe automation and/or alert behavior] | [CoreIOT] | [Txx] | Planned |

**Important:** A single ESP32 connected to CoreIOT does **not** by itself satisfy the required multi-device integrated system. Technology grading elements are optional choices, but every claimed element requires working evidence.

## 2. Architecture

Add a diagram to `docs/diagrams/architecture.png` (or `.svg`). Indicate device nodes, CoreIOT, optional local gateway, telemetry and control directions, and link protocols (Wi-Fi, MQTT, HTTP, BLE, ESP-NOW, etc.).

## 3. Repository structure

```text
firmware/       ESP32-S3 device firmware (one subfolder per node)
gateway/        Local gateway code, if selected
ai/             Datasets, training code, exported model metadata (if selected)
coreiot/        Exported dashboards, device profiles and RuleChain configs
report/         LaTeX report, IEEE references and figures
docs/           Diagrams, evidence index, test measurements, task assignment
.github/        Pull request and issue templates
```

## 4. Requirements

### Hardware
- ESP32-S3 (YoloUNO) board(s): [quantity, inventory, role]
- [Sensor modules and interfaces]
- [Actuator(s) and power supply]
- [PC/Raspberry Pi for a local gateway, only if selected]
- **Hardware access:** boards are available only during lab sessions. Prepare code and test plans at home; flash and capture hardware evidence at the lab.

### Software
- Git and GitHub
- [Arduino IDE / PlatformIO / ESP-IDF: choose and record exact version]
- [CoreIOT account and server URL]
- [Python and version, only if gateway/AI selected]

> Keep actual board pin assignments and dependencies in each node's own README once decided. No firmware implementation is included yet because the topic and sensor hardware are not selected.

## 5. Installation and configuration

1. Clone: `git clone https://github.com/OWNER/REPOSITORY.git` and `cd REPOSITORY`.
2. Create local configuration from the applicable examples:
   - `cp firmware/node_sensor/config.example.h firmware/node_sensor/config.h`
   - `cp gateway/.env.example gateway/.env` (only when using a gateway)
3. Fill in Wi-Fi credentials, CoreIOT endpoint and device tokens **locally only**.
4. Register required devices and profiles on CoreIOT; import any exported JSON configs from `coreiot/` when available.
5. Follow `firmware/node_sensor/README.md` and `gateway/README.md` (if applicable) for actual build/flash/run commands after your toolchain is chosen.

**Do not commit passwords, access tokens, private keys, or real Wi-Fi credentials.** The `.gitignore` excludes local secret files.

## 6. How to run and verify

These steps must be completed and replaced with real instructions before submission:

1. Build and flash each device node: **[exact commands TBD]**.
2. Start local gateway if used: **[exact command TBD]**.
3. Connect to CoreIOT and confirm telemetry: **[dashboard screenshot/log link TBD]**.
4. Trigger each F0x feature and record observed behavior: **[test case IDs TBD]**.
5. Demonstrate remote control, alerts, OTA, AI or other claimed elements only when implemented and verified.

## 7. Test results and evidence

Keep test records in `docs/testing/test-results.csv` and link logs, screenshots and demo video timestamps in `docs/evidence/evidence-index.csv`. Log mean, minimum and maximum results across repeated trials as required by the report template.

## 8. Deliverables

- [ ] PDF report based on teacher template: `[ClassCode]_[GroupCode]_IoTReport.pdf`
- [ ] GitHub repository accessible to lecturer and README instructions actually tested
- [ ] Full source code and member-specific commit history
- [ ] Demo video, **5–10 minutes recommended**, showcasing all claimed features
- [ ] Report's task assignment and technology self-assessment tables
- [ ] References (at least five), test measurements and AI-use declaration

### Links
- **CoreIOT dashboard:** [link, if public]
- **Demo video:** [link]
- **Final PDF report:** [link/path]
- **Team Drive:** [link]

## 9. Reused code, sources and AI assistance

Document CoreIOT sample projects, libraries, tutorials and externally sourced code in `docs/sources-and-ai-use.md`. Explicitly distinguish what was reused from what was developed by the team. Report AI assistance and verify all generated code.

## 10. Contact

Instructor: Dr. Nguyễn Hòa Hưng · nguyenhoahung@hcmut.edu.vn
