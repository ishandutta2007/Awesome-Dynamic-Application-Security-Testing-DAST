# Awesome-Dynamic-Application-Security-Testing-DAST

A curated list of Dynamic Application Security Testing (DAST) tools, runtime API vulnerability scanners, DevSecOps pipeline automation tools, and security testing frameworks.

Dynamic Application Security Testing (DAST) tools test running web applications and APIs from an external attacker's perspective without requiring source code access. They detect critical vulnerabilities such as SQL injection, Cross-Site Scripting (XSS), Server-Side Request Forgery (SSRF), Broken Object Level Authorization (BOLA/IDOR), authentication bypasses, and security misconfigurations.

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#saas--hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global Dynamic Application Security Testing (DAST) market is estimated between **$3.5 billion and $3.8 billion in 2025**, projected to surpass **$4.5 billion by 2026** at a compound annual growth rate (CAGR) of ~16–22%, driven by the explosion of cloud-native APIs, microservice architectures, and compliance mandates.

The sector is **moderately fragmented** rather than concentrated or winner-take-all. Established AppSec giants (OpenText Fortify, Veracode, Black Duck, Checkmarx) serve large enterprise governance needs, while high-growth developer-first challengers (PortSwigger Burp Suite, Invicti, Rapid7, StackHawk, Intruder) dominate agile development workflows. Most modern security organizations rely on a multi-layered defense-in-depth model that combines commercial DAST automation with open-source scanners and manual penetration testing toolkits.

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

Curated open-source DAST scanners, web crawlers, API fuzzers, and runtime vulnerability testing frameworks. The projects below are sorted in descending order by GitHub star count, featuring real-time star badges linking directly to their stargazers page.

1. **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** [![GitHub stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) — An interactive TLS-capable intercepting HTTP/HTTPS and WebSocket proxy for security researchers, penetration testers, and automated runtime traffic inspection.
2. **[sqlmap](https://github.com/sqlmapproject/sqlmap)** [![GitHub stars](https://img.shields.io/github/stars/sqlmapproject/sqlmap?style=social&color=white)](https://github.com/sqlmapproject/sqlmap/stargazers) — Automatic SQL injection and database takeover engine supporting fingerprinting, DB data extraction, file system access, and out-of-band connections.
3. **[Nuclei](https://github.com/projectdiscovery/nuclei)** [![GitHub stars](https://img.shields.io/github/stars/projectdiscovery/nuclei?style=social&color=white)](https://github.com/projectdiscovery/nuclei/stargazers) — Fast and customizable vulnerability scanner driven by a massive community-maintained library of YAML templates targeting web applications, APIs, DNS, network protocols, and modern CVEs.
4. **[Katana](https://github.com/projectdiscovery/katana)** [![GitHub stars](https://img.shields.io/github/stars/projectdiscovery/katana?style=social&color=white)](https://github.com/projectdiscovery/katana/stargazers) — Next-generation crawling and spidering framework supporting headless browser automation, standard web navigation, and deep endpoint discovery for DAST scanners.
5. **[ffuf](https://github.com/ffuf/ffuf)** [![GitHub stars](https://img.shields.io/github/stars/ffuf/ffuf?style=social&color=white)](https://github.com/ffuf/ffuf/stargazers) — Extremely fast web fuzzer written in Go, widely utilized in DAST workflows for parameter discovery, hidden endpoint bruteforcing, and runtime payload injection.
6. **[OWASP ZAP (Zed Attack Proxy)](https://github.com/zaproxy/zaproxy)** [![GitHub stars](https://img.shields.io/github/stars/zaproxy/zaproxy?style=social&color=white)](https://github.com/zaproxy/zaproxy/stargazers) — The world's most widely deployed open-source DAST scanner (maintained by Checkmarx). Includes an intercepting proxy, automated active/passive scanner, REST API, Docker images, and an extensive extension marketplace.
7. **[Sn1per](https://github.com/1N3/Sn1per)** [![GitHub stars](https://img.shields.io/github/stars/1N3/Sn1per?style=social&color=white)](https://github.com/1N3/Sn1per/stargazers) — Automated penetration testing and dynamic attack surface management platform aggregating recon, multi-tool DAST execution, and security reporting.
8. **[Nikto](https://github.com/sullo/nikto)** [![GitHub stars](https://img.shields.io/github/stars/sullo/nikto?style=social&color=white)](https://github.com/sullo/nikto/stargazers) — Classic web server vulnerability scanner identifying dangerous files, outdated server installations, vulnerable CGIs, and configuration defects.
9. **[feroxbuster](https://github.com/epi052/feroxbuster)** [![GitHub stars](https://img.shields.io/github/stars/epi052/feroxbuster?style=social&color=white)](https://github.com/epi052/feroxbuster/stargazers) — High-speed, recursive content discovery tool written in Rust, purpose-built for rapid web content mapping and DAST reconnaissance.
10. **[Commix](https://github.com/commixproject/commix)** [![GitHub stars](https://img.shields.io/github/stars/commixproject/commix?style=social&color=white)](https://github.com/commixproject/commix/stargazers) — Automated all-in-one OS command injection and exploitation tool capable of detecting and exploiting command execution flaws in web targets.
11. **[w3af](https://github.com/andresriancho/w3af)** [![GitHub stars](https://img.shields.io/github/stars/andresriancho/w3af?style=social&color=white)](https://github.com/andresriancho/w3af/stargazers) — Extensible Web Application Attack and Audit Framework featuring modular crawlers, audit plugins, and exploit automation.
12. **[Arachni](https://github.com/Arachni/arachni)** [![GitHub stars](https://img.shields.io/github/stars/Arachni/arachni?style=social&color=white)](https://github.com/Arachni/arachni/stargazers) — Modular, high-performance Ruby-based web application security scanner framework featuring differential analysis to eliminate false positives.
13. **[RESTler](https://github.com/microsoft/restler-fuzzer)** [![GitHub stars](https://img.shields.io/github/stars/microsoft/restler-fuzzer?style=social&color=white)](https://github.com/microsoft/restler-fuzzer/stargazers) — The first stateful REST API fuzzing tool from Microsoft Research that generates dynamic test sequences based on OpenAPI/Swagger specifications to detect deep logical vulnerabilities.
14. **[Astra](https://github.com/flipkart-incubator/Astra)** [![GitHub stars](https://img.shields.io/github/stars/flipkart-incubator/Astra?style=social&color=white)](https://github.com/flipkart-incubator/Astra/stargazers) — Automated REST API security testing framework developed by Flipkart, testing for OWASP API Top 10 vulnerabilities including BOLA, SQLi, CSRF, and authentication bypasses.
15. **[Wapiti](https://github.com/wapiti-scanner/wapiti)** [![GitHub stars](https://img.shields.io/github/stars/wapiti-scanner/wapiti?style=social&color=white)](https://github.com/wapiti-scanner/wapiti/stargazers) — Black-box web application vulnerability scanner written in Python 3 that crawls pages and injects payloads to audit for XSS, SQLi, SSRF, and file disclosure vulnerabilities.
16. **[GoTestWAF](https://github.com/wallarm/gotestwaf)** [![GitHub stars](https://img.shields.io/github/stars/wallarm/gotestwaf?style=social&color=white)](https://github.com/wallarm/gotestwaf/stargazers) — Open-source test suite in Golang to benchmark Web Application Firewalls (WAF) and API security engines against common attack payloads.
17. **[GraphQL-Cop](https://github.com/dolevf/graphql-cop)** [![GitHub stars](https://img.shields.io/github/stars/dolevf/graphql-cop?style=social&color=white)](https://github.com/dolevf/graphql-cop/stargazers) — Security auditing utility for GraphQL endpoints that detects introspection vulnerabilities, alias overloading, field duplication DOS, and batch query flaws.
18. **[Dastardly](https://github.com/PortSwigger/dastardly-github-action)** [![GitHub stars](https://img.shields.io/github/stars/PortSwigger/dastardly-github-action?style=social&color=white)](https://github.com/PortSwigger/dastardly-github-action/stargazers) — Free CI/CD security scanner from PortSwigger (makers of Burp Suite), engineered specifically for automated web application vulnerability scanning in CI/CD pipelines.
19. **[VulnAPI](https://github.com/cerberauth/vulnapi)** [![GitHub stars](https://img.shields.io/github/stars/cerberauth/vulnapi?style=social&color=white)](https://github.com/cerberauth/vulnapi/stargazers) — Open-source CLI and library written in Go for discovering and auditing vulnerabilities in REST APIs with OpenAPI specification scanning.
20. **[OWASP PTK (PenTest Kit)](https://github.com/DenisPodgurskii/pentestkit)** [![GitHub stars](https://img.shields.io/github/stars/DenisPodgurskii/pentestkit?style=social&color=white)](https://github.com/DenisPodgurskii/pentestkit/stargazers) — Browser extension for in-browser dynamic application security testing, request decoding/tampering, and automated swagger profiling.
21. **[Moxy](https://github.com/matank001/Moxy)** [![GitHub stars](https://img.shields.io/github/stars/matank001/Moxy?style=social&color=white)](https://github.com/matank001/Moxy/stargazers) — Modern open-source DAST tool featuring an agentic architecture to assist, guide, and automate complex web pentesting tasks.
22. **[justdastit](https://github.com/SnailSploit/justdastit)** [![GitHub stars](https://img.shields.io/github/stars/SnailSploit/justdastit?style=social&color=white)](https://github.com/SnailSploit/justdastit/stargazers) — Open-source CLI-driven DAST toolkit engineered as a lightweight alternative to commercial web pentest tools, featuring active/passive scanning and reporter utilities.
23. **[LeakRadar](https://github.com/Ajmax76/leakradar)** [![GitHub stars](https://img.shields.io/github/stars/Ajmax76/leakradar?style=social&color=white)](https://github.com/Ajmax76/leakradar/stargazers) — API security reconnaissance and BOLA evidence engine designed for scanning REST endpoints and identifying token privilege leaks.
24. **[gqlhunter](https://github.com/bess1lie/gqlhunter)** [![GitHub stars](https://img.shields.io/github/stars/bess1lie/gqlhunter?style=social&color=white)](https://github.com/bess1lie/gqlhunter/stargazers) — GraphQL reconnaissance and analysis CLI offering schema discovery, introspection querying, authentication analysis, and vulnerability risk classification.

---

## How to Contribute

Contributions are welcome! To propose additions or updates:

1. Fork the repository.
2. Edit `README.md` following the existing format.
3. Submit a Pull Request with a clear description of the tool and verification details.

---

## Disclaimer

This list is curated for educational, DevSecOps engineering, and defensive security auditing purposes. DAST tools must only be used against applications and APIs where you have explicit written authorization to perform security testing. Unauthorized testing against target infrastructure is strictly illegal.
