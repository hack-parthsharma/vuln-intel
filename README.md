# 🛡️ VULN INTEL — 24h Vulnerability Intelligence Dashboard

Real-time vulnerability scanner that checks **82+ enterprise products** against the NVD (National Vulnerability Database) and displays prioritized results with CVSS scoring, tier classification, and executive briefings.

![Dashboard Preview](https://img.shields.io/badge/CVEs-Real--Time-00e5ff?style=for-the-badge&logo=shield&logoColor=white)
![NVD API](https://img.shields.io/badge/NVD-API%202.0-1e40af?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-69f0ae?style=for-the-badge)

## 🚀 Live Demo

**[https://YOUR_USERNAME.github.io/vuln-intel/](https://YOUR_USERNAME.github.io/vuln-intel/)**

## Features

- **Real-time NVD scanning** — Queries NIST NVD 2.0 API for CVEs published in the last 24 hours
- **82+ product matching** — Keyword + CPE pattern matching against your full inventory
- **4-tier priority classification** — Emergency / High / Medium / Low based on CVSS + exploit signals
- **Executive briefing** — Auto-generated situational summary with action items
- **Outlook integration** — Auto-opens Outlook with pre-filled report after each scan
- **Rich report export** — Copy HTML report to clipboard or download as .html file
- **Zero dependencies** — Single HTML file, no frameworks, no build tools, no backend

## Monitored Products

| Category | Products |
|----------|----------|
| Network & Firewall | Cisco Nexus, UCS, SonicWall, Fortigate, UniFi, Cato |
| OS & Virtualization | Windows 10, Windows Server 2012 R2, VMware ESXi/vCenter, Samba |
| Browsers | Chrome, Firefox, Edge |
| Databases | PostgreSQL, MySQL, MSSQL, MongoDB, Redis, Elasticsearch, RabbitMQ |
| Web Servers | Apache HTTP, Tomcat, Node.js, WordPress, cPanel, OpenSSL |
| Dev & Monitoring | Grafana, Prometheus, Kibana, Graylog, SolarWinds, Notepad++ |
| Security | ESET, Cortex XDR, Imperva, KnowBe4, Jamf Protect |
| SaaS | Microsoft Office 365, Zoom, Slack, Zendesk, JumpCloud |
| Adobe & PDF | Photoshop CC, Acrobat Reader DC, Nitro PDF |
| And more... | Oracle Java, ManageEngine, Hikvision, SonarQube, Fluentd, etc. |

## Setup

### Option 1: GitHub Pages (Recommended)
1. Fork this repo
2. Go to **Settings → Pages → Source → Deploy from branch → main**
3. Your dashboard is live at `https://YOUR_USERNAME.github.io/vuln-intel/`

### Option 2: Local
Just download `index.html` and open it in any browser.

## NVD API Key

The dashboard includes an NVD API key for faster scanning. To use your own:
1. Register at [https://nvd.nist.gov/developers/request-an-api-key](https://nvd.nist.gov/developers/request-an-api-key)
2. Replace the `NVD_API_KEY` value in `index.html`

## How It Works

1. **Scan** — Fetches all CVEs published in the last 24h from NVD API 2.0
2. **Match** — Checks each CVE description + CPE data against 82+ product keywords
3. **Classify** — Assigns priority tiers based on CVSS score + exploit indicators
4. **Report** — Displays interactive dashboard + opens Outlook with the full report

## Tier Classification

| Tier | Label | Criteria |
|------|-------|----------|
| 🔴 0 | Emergency | Active exploitation, unauth RCE, or CVSS ≥ 9.5 |
| 🟠 1 | High | Remote code execution or CVSS ≥ 8.0 |
| 🟡 2 | Medium | CVSS ≥ 5.0 |
| 🟢 3 | Low | Info leak, DoS, local-only |

## License

MIT
