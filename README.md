# Awesome-Dynamic-Application-Security-Testing-DAST

A curated list of Dynamic Application Security Testing (DAST) tools, runtime API vulnerability scanners, DevSecOps pipeline automation tools, and security testing frameworks.

Dynamic Application Security Testing (DAST) tools test running web applications and APIs from an external attacker's perspective without requiring source code access. They detect critical vulnerabilities such as SQL injection, Cross-Site Scripting (XSS), Server-Side Request Forgery (SSRF), Broken Object Level Authorization (BOLA/IDOR), authentication bypasses, and security misconfigurations.

---

## Table of Contents

- [SaaS / Hosted Platforms](#saas--hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## SaaS / Hosted Platforms

The following commercial DAST platforms are sorted in descending order by parent company size (valuation / annual revenue).

| Product | Company Size (Revenue / Valuation) | Starting Tier Pricing | Free Tier / Free Trial Limits | Key Capabilities & Architecture |
|---|---|---|---|---|
| [Fortify WebInspect](https://www.opentext.com/products/fortify-webinspect) | **$5.17B Revenue** (~$7.53B Market Cap) | ~$25,000 / year (or ~$2,083/mo via Fortify on Demand assessment units) | No free-forever plan; 15-day assisted enterprise PoC evaluation for 1 target app | Enterprise dynamic analysis engine for complex single-page apps (SPAs), web APIs, and legacy web services with automated macro generation. |
| [Veracode Dynamic Analysis](https://www.veracode.com/products/dynamic-analysis-dast) | **$2.50B Valuation** (~$300M+ ARR) | ~$20,000 / year (DAST Essentials baseline annual subscription) | No free-forever plan; 14-day free trial of DAST Essentials (no credit card required, covers 1 designated target web application) | Cloud-scale crawler with automated authentication handling, perimeter vulnerability scanning, and unified policy compliance reporting. |
| [Black Duck Continuous Dynamic](https://www.blackduck.com/products/continuous-dynamic.html) | **$2.10B Valuation** (formerly Synopsys WhiteHat) | ~$18,000 / year (Polaris fAST Dynamic baseline annual contract) | No free-forever plan; 14-day guided enterprise Proof-of-Concept (PoC) trial (limited to 1 web application target) | Continuous production-safe web application vulnerability scanning supported by verified vulnerability analysis to filter noise. |
| [Checkmarx DAST](https://checkmarx.com/product/application-security-testing/dast/) | **$1.15B Valuation** (~$150M+ ARR) | ~$15,000 / year (Checkmarx One AppSec platform entry tier) | No free-forever plan; 14-day assisted enterprise PoC trial (requires domain verification, limited to 1 repository/app endpoint) | Integrated enterprise DAST built into Checkmarx One, correlating runtime DAST findings directly with SAST and SCA code insights. |
| [Invicti](https://www.invicti.com/) | **$1.00B+ Valuation** (~$120M+ ARR) | $7,000 / year (entry bundle covering up to 5 web targets) | No free-forever plan; 14-day guided proof-of-concept evaluation via sales demo (scoped to 1 verified FQDN) | Enterprise-grade dynamic scanner featuring Proof-Based Scanning that automatically exploits detected flaws to deliver verifiable zero-false-positive results. |
| [Acunetix](https://www.acunetix.com/) | **$1.00B+ Valuation** (part of Invicti Security) | $7,000 / year (standard 5-target FQDN annual subscription) | No free-forever plan; 14-day free trial (requires domain verification, max 1 target domain scan) | High-speed DAST scanner engineered for single-page applications (HTML5/JavaScript) with specialized deep scanning for SQLi and XSS. |
| [Rapid7 InsightAppSec](https://www.rapid7.com/products/insightappsec/) | **$859.8M Revenue** (~$1.00B Market Cap) | $175 / month per app ($2,100 / year per application, billed annually) | No free-forever plan; 30-day free trial (limited to 1 verified corporate domain or pre-configured demo test environments) | Cloud-native vulnerability management with attack replay capabilities to validate remediation without full re-scans. |
| [StackHawk](https://www.stackhawk.com/) | **$150M Valuation** ($35.3M Series B funding) | $39 / contributor per month ($468 / year per developer) for Pro/Secure; $10/mo for Wingman AI | **Free forever Developer Plan** (1 application target, 1 user environment, unlimited CI/CD scans); 14-day free trial of Pro tier | Developer-first DAST and API security platform built on top of ZAP core, designed specifically for pre-production CI/CD pipeline automation. |
| [Burp Suite Professional & Enterprise](https://portswigger.net/burp) | **~$55M Revenue** (£39M+ ARR) | $499 / user per year ($41.58/mo) for Pro; $5,999 / year for Enterprise DAST | **Free forever Community Edition** (unlimited manual proxying, Repeater, Decoder; scanner disabled); 30-day trial for Professional | De-facto industry standard pentesting proxy with automated crawl/audit engine, headless CI/CD scanning, and extensive BApp Store extensions. |
| [Intruder](https://www.intruder.io/) | **~$12M ARR** | $299 / month ($3,588 / year) for Cloud tier (includes 1 target domain + external attack surface scans) | **Free forever plan** (1 target domain, monthly basic perimeter scan); 14-day free trial of Pro tier (full authenticated web app scanning) | Cloud-based perimeter and web application scanner focused on continuous attack surface management and emerging threat notifications. |
| [AppCheck](https://appcheck-ng.com/) | **~$10M ARR** (£7M+ ARR) | £3,000 / year (~$3,850 / year, or £250/day assessment unit on G-Cloud) | No free-forever plan; 14-day free trial offering 1 complimentary full-scope web vulnerability scan report for 1 verified domain | First-principles vulnerability scanner using proprietary browser automation to test complex single-page workflows and custom APIs. |

---

## Open-Source GitHub Projects

- **OWASP ZAP (Zed Attack Proxy)** — The most widely used open-source DAST scanner, maintained by Checkmarx. Features an intercepting proxy, automated scanner, API, Docker image, and extensive add-on marketplace.
- **Nuclei** — Fast, template-driven vulnerability scanner with a massive community-maintained library of checks for known CVEs, misconfigurations, and exposed panels.
- **Nikto** — Classic web server scanner checking for dangerous files, outdated software, and misconfigurations.
- **Wapiti** — Lightweight web application vulnerability scanner that crawls pages and injects payloads to detect XSS, SQLi, and other flaws.
- **Arachni** — Feature-rich Ruby-based scanner with a unique validation methodology.
- **w3af** — Web application attack and audit framework.
- **LeakRadar** — Open-core DAST scanner designed specifically for REST APIs detecting BOLA/IDOR and privilege escalation.
- **VulnAPI** — Go-based API security vulnerability scanner supporting OpenAPI contracts.
- **gqlhunter** — GraphQL-specific recon and analysis CLI discovering endpoints and dumping schemas.
- **justdastit** — CLI-based DAST toolkit positioned as an affordable Burp alternative.
- **Moxy** — Open-source DAST tool for modern web applications with agentic pentesting capabilities.
- **OWASP PTK (PenTest Kit)** — Browser-extension-based security testing toolkit that integrates directly into browser sessions for runtime DAST.

---

## How to Contribute

Contributions are welcome! To propose additions or updates:

1. Fork the repository.
2. Edit `README.md` following the existing format.
3. Submit a Pull Request with a clear description of the tool and verification details.

---

## Disclaimer

This list is curated for educational, DevSecOps engineering, and defensive security auditing purposes. DAST tools must only be used against applications and APIs where you have explicit written authorization to perform security testing. Unauthorized testing against target infrastructure is strictly illegal.
