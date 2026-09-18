# Enterprise Compromise Hunting Atlas

An offline, self-contained investigation atlas for connecting enterprise technologies, attack patterns, evidence sources, historical vulnerabilities, and defensive hunting actions.

![Enterprise Compromise Hunting Atlas demonstration](assets/compromise-hunting-atlas-preview-zh-CN.gif)

[中文说明](#中文说明)

## What it does

The atlas helps incident responders and threat hunters answer four practical questions:

1. Which evidence should be preserved for this type of system?
2. Which traces are relevant to the suspected compromise pattern?
3. Which historical vulnerabilities and product-specific logs deserve review?
4. What can the available evidence support—and what can it not prove?

The current snapshot includes:

- 16 target-system categories;
- 38 concrete product identities;
- 375 product-level minimum log and evidence entries;
- 13 compromise patterns;
- 21 representative historical vulnerabilities;
- 44 generic evidence artifacts;
- 29 defensive hunt recipes;
- relationship-level detection methods and historical fingerprint guidance.

## Quick start

1. Download `Enterprise-Compromise-Hunting-Atlas.html`.
2. Open it with a current version of Chrome, Chromium, Edge, or Firefox.
3. No installation, local server, administrator privilege, account, or network connection is required.
4. Start from a target-system card, or open the **Attack & evidence matrix**.
5. Use **Hunt plan** to select targets, products, and suspected scenarios, then mark the evidence currently available.

The default interface is Chinese. Select **English** in the upper-right language control for the complete English interface and knowledge view. You can also open:

```text
Enterprise-Compromise-Hunting-Atlas.html?lang=en
```

## Main views

- **Overview** — Browse operating systems, databases, middleware, web stacks, containers, cloud platforms, network devices, and firmware domains.
- **Attack & evidence matrix** — Explore target × compromise-pattern relationships, relevant evidence, hunt strategies, detections, fingerprints, vulnerabilities, and conclusion boundaries.
- **Hunt plan** — Build a case-specific collection and investigation checklist, track evidence readiness, and export the result as Markdown.
- **Method & sources** — Review evidence levels, confidence language, operating boundaries, and primary references.

## Evidence semantics

Evidence readiness is not a risk score or a probability of compromise. Missing, unavailable, or uncollected evidence must not be interpreted as proof that an attack did not occur.

Historical CVEs, protocol fingerprints, file signatures, URIs, and individual rule hits are leads—not conclusions. Confirm product identity, version, deployment conditions, time windows, and independent side effects before escalating a finding.

Hunt recipes are defensive templates. Review placeholders, scope, authorization, dependencies, privileges, side effects, and collection limits before running any command.

## Privacy and security

- Runs entirely in the browser from a local HTML file.
- Does not upload evidence or telemetry.
- Does not require a backend or cloud service.
- Does not automatically scan hosts, execute exploits, or run hunting commands.
- Does not fetch remote runtime scripts, fonts, styles, images, or data.
- External references open only when the user explicitly selects them.

## Limitations

This project is an investigation-planning and evidence-interpretation aid. It does not replace vendor advisories, product documentation, forensic acquisition, specialist parsers, memory analysis, or human review. The included knowledge is a reviewed snapshot, not a complete CVE, detection-rule, or threat-intelligence database.

The primary tested environment is Chromium on Linux. Firefox is expected to work, but Safari, managed enterprise browsers, mobile devices, assistive technologies, and all local-file security policies have not been exhaustively validated.

## Repository contents

```text
Enterprise-Compromise-Hunting-Atlas.html  Offline application
README.md                                 Project and usage guide
assets/compromise-hunting-atlas-preview-zh-CN.gif
LICENSE                                   MIT License for software and documentation
LICENSE-MEDIA.md                          CC BY 4.0 terms for the demonstration GIF
```

## License

The HTML application and project documentation are released under the [MIT License](LICENSE). The demonstration GIF is released under [CC BY 4.0](LICENSE-MEDIA.md).

---

## 中文说明

Enterprise Compromise Hunting Atlas（企业关键系统失陷狩猎图谱）是一款完全离线、单 HTML、自包含的调查规划与失陷痕迹狩猎工具。它把目标系统、具体产品、攻击与失陷形态、历史漏洞、日志和证据工件、检测方法以及结论边界组织成一张可交互的调查地图。

### 能解决什么问题

- 面对某类操作系统、数据库、中间件、Web、容器、云或网络设备时，应该优先保全哪些证据；
- 怀疑 RCE、WebShell、内存驻留、Rootkit、身份后门、横向移动、C2 或反取证时，应检查哪些痕迹；
- 某个历史漏洞是否真正适用于当前产品、版本和部署条件；
- 当前证据能够支持什么结论，还缺少哪些独立证据进行互证。

### 快速使用

1. 下载 `Enterprise-Compromise-Hunting-Atlas.html`。
2. 使用最新版 Chrome、Chromium、Edge 或 Firefox 双击打开。
3. 无需安装、管理员权限、账户、网络或本地服务器。
4. 从首页的目标系统卡片开始，或者进入“攻击与痕迹矩阵”。
5. 在“狩猎计划”中选择目标、具体产品和怀疑场景，标记已有证据，然后生成并导出调查计划。
6. 右上角可在中文和 English 之间切换，切换不会清除当前选择。

### 重要边界

“证据掌握度”不是风险分数，也不是失陷概率。没有采集、证据缺失或工具无输出，不能解释为没有发生攻击。

历史 CVE、JA3/JA4/JARM、文件签名、URI 或单条规则命中都只是调查线索。形成失陷结论前，仍需核验产品身份、版本、暴露条件、时间相关性和独立副作用。

应用本身不会上传证据、扫描目标、执行漏洞利用或自动运行命令。所有配方均面向获得授权的防御性调查，执行前必须检查占位符、权限、范围、依赖、副作用和结论限制。

### 许可证

HTML 应用和项目文档使用 [MIT License](LICENSE)。演示 GIF 使用 [CC BY 4.0](LICENSE-MEDIA.md)。
