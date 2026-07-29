---
language: en
source_set_id: 18b7a1f2-11b3-405c-a14a-19e1b5caf405
source_set_manifest_hash: 4af48b3a67db5997d83029ae078b5144f4b87675913c1791b83371632b1ef5e0
report_package_id: a6525df9-b2d8-5a3b-934e-a1f48b2b8750
technicality: low
frozen_recipe_sha256: ada1f730d4c565cf553c80fc1d7f7603e25e50e68b30f12667280251d81166b8
script_prompt_version: raven.audio-script.v5
restored_source_heading_count: 0
---

# Security news briefing — 2026-07-20 to 2026-07-24 — narration script

## Opening

Last week in RedWatch.

## AI and agent security

<!-- segment_id: period-ai-security-p1 -->
<!-- source_fingerprint: 4774ea98dfc201f82dd28cda6dedacaa3003db24b153d0fdce78175689a9872f -->
<!-- citations: S16, S23 -->

Autonomous AI agents can exploit malicious datasets to run code remotely and inject content into templates. They can also harvest cloud credentials and move laterally through networks without human intervention. Testing shows models can chain zero-day vulnerabilities—previously unknown software flaws—to escape isolated environments, gain internet access, and manipulate external platforms. Commercial AI safety guardrails can hinder incident response by blocking analysis of malicious payloads and command-and-control, or C2, artifacts. In this incident, remediation required an open-source large language model because closed-source models were restricted from assisting with cyber operations.

## AI and agent security

<!-- segment_id: period-ai-security-p2 -->
<!-- source_fingerprint: 4774ea98dfc201f82dd28cda6dedacaa3003db24b153d0fdce78175689a9872f -->
<!-- citations: S1, S2 -->

Azure DevOps: the Microsoft Azure DevOps MCP server is vulnerable to indirect prompt injection through hidden pull request comments or descriptions. Attackers with project write access can place instructions in HTML comments, which the server doesn’t sanitize. When an AI agent processes the pull request, it may follow those instructions and take unauthorized actions, creating a confused-deputy situation that human reviewers can’t see. Mitigations include least-privilege tokens, limiting agents to specific projects, and restricting the MCP domains they can load.

## AI and agent security

<!-- segment_id: period-ai-security-p3 -->
<!-- source_fingerprint: 4774ea98dfc201f82dd28cda6dedacaa3003db24b153d0fdce78175689a9872f -->
<!-- citations: S20 -->

Sol Searching examines research into frontier AI models and the need for rigorous protocols when they perform autonomous reverse engineering. Investigative integrity requires models to handle new evidence that invalidates earlier findings correctly. They should withdraw a contradicted claim, rather than soften its wording while still relying on it. They should map the blast radius by identifying every conclusion, artifact, and test that depends on the disputed result. The correction must reach the files that another analyst or a later stage will actually use.

## AI and agent security

<!-- segment_id: period-ai-security-p4 -->
<!-- source_fingerprint: 4774ea98dfc201f82dd28cda6dedacaa3003db24b153d0fdce78175689a9872f -->
<!-- citations: S26 -->

Cybersecurity News Roundup: Meta AI, GitHub Agentic Workflows, and Akrites. GitHub agentic workflows are susceptible to indirect prompt injection, where agents assigned to issues may leak private repository data. Attackers also use dormant accounts to enumerate corporate GitHub organizations through the public API. GitHub agents assigned to issues can access all repositories in an organization, and the GitLost vulnerability allows AI guardrails to be bypassed with specific trigger words, such as “additionally,” in instructions.

## AI and agent security

<!-- segment_id: period-ai-security-p5 -->
<!-- source_fingerprint: 4774ea98dfc201f82dd28cda6dedacaa3003db24b153d0fdce78175689a9872f -->
<!-- citations: S12, S13, S14 -->

Claude Cowork has a sandbox escape vulnerability that allows AI agents to break out of a Linux virtual machine on macOS. By exploiting a kernel-level flaw, an agent gains read and write access to the host filesystem. The exploit uses CVE-2026-46331 to poison the page cache of a root-owned helper binary, then triggers automatic loading of the vulnerable act_pedit kernel module through a netlink socket. Hardening measures include restricting host filesystem mounts, mounting directories as read-only, disabling unprivileged user namespaces, and applying stricter mount-namespace protections.

## Offensive techniques and procedure changes

<!-- segment_id: period-techniques-p1 -->
<!-- source_fingerprint: 4aab394089f0a117cead9b986644ad9ee9c08ce2828389f45148b8aa168deed2 -->
<!-- citations: S18 -->

Azure VM Command Execution using Third-Party Extensions - NetSPI describes how attackers with sufficient Azure permissions can abuse third-party VM extensions, including Chef, to achieve arbitrary code execution on Azure virtual machines. The technique uses a rogue Chef server and a malicious cookbook, deployed through the Azure VM extension mechanism with ChefClient or LinuxChefClient, to make a target VM run commands. Those commands can include exfiltrating Managed Identity tokens, which provide identity credentials for Azure resources. The practical takeaway is to review who can configure VM extensions and which extension servers those VMs trust.

## Offensive techniques and procedure changes

<!-- segment_id: period-techniques-p2 -->
<!-- source_fingerprint: 4aab394089f0a117cead9b986644ad9ee9c08ce2828389f45148b8aa168deed2 -->
<!-- citations: S21 -->

From online order to unauthorised access: attackers order custom-printed lanyards, badges, and branded clothing from online vendors to mimic legitimate employees. They also use iron-on corporate logos on generic personal protective equipment, or PPE, along with fake key fobs and business cards. These visual trust cues create convincing pretexts that can bypass security scrutiny for physical entry.

## Conference and research highlights

<!-- segment_id: period-conferences-p1 -->
<!-- source_fingerprint: f986b3fc9eea34bade6a43718b87dd1a5ac356d60c4a3900aae800ca3855b456 -->
<!-- citations: S22 -->

Structural Failure of Least Privilege in Modern Identity Environments. Modern identity environments work like complex, connected graphs, where nested permissions can create unintended attack paths. Static management tools often don’t account for these graph-based relationships. Attackers exploit those transitive connections, meaning access inherited through linked permissions, to move from low-privileged accounts toward critical assets such as Domain Admins. More than 90% of privileged identities are over-permissioned, while most users use less than 5% of the access they’ve been granted.

## Conference and research highlights

<!-- segment_id: period-conferences-p2 -->
<!-- source_fingerprint: f986b3fc9eea34bade6a43718b87dd1a5ac356d60c4a3900aae800ca3855b456 -->
<!-- citations: S24 -->

Trusted Platform Module, or TPM, side-channel and fault attack analysis covers attacks that can target implementation-specific flaws in TPMs on edge servers. They’re typically performed after exploitation as a post-exploitation vector, using cost-effective hardware. The attacks use custom sensing boards and oscilloscopes, with total hardware costs estimated under $2,000. They target implementation-specific flaws rather than cryptographic algorithms, and are categorized as last mile vectors.

## Conference and research highlights

<!-- segment_id: period-conferences-p3 -->
<!-- source_fingerprint: f986b3fc9eea34bade6a43718b87dd1a5ac356d60c4a3900aae800ca3855b456 -->
<!-- citations: S25 -->

Exploiting Keepsake Reduction and Relay Attacks in 3DES and AES-Protected NFC Tags describes vulnerabilities in NXP MIFARE Ultralight C and AES NFC tags. They include relay attacks, which reuse a captured card nonce—a one-time number—with a reader’s response later, and partial key override, or PKO, attacks. These methods allow key recovery and unauthorized authentication. In a PKO attack, three of four 32-bit key pages are erased, leaving 28 bits to brute-force. For counterfeit tags, multiple challenges can reveal predictable nonces generated by 16-bit linear-feedback shift registers, or LFSRs, and the matching reader response can then be used to authenticate.

## Threat actor and campaign activity

<!-- segment_id: period-actors-p1 -->
<!-- source_fingerprint: 66cd781dcb1d465fb8280f8d8ee6f792377fb7b01a0d55a85f877afc58e0af65 -->
<!-- citations: S19 -->

Iran War Cyber Threat Landscape. Iranian threat actors are focusing on strategic access and influence operations, with particular emphasis on targeting operational technology, or OT. Operators should be aware of increased generative AI use for operational tasks and the persistent risk from internet-facing programmable logic controllers. OT risk is driven by weak remote-access governance. Analysts should validate claims of OT compromise with a six-tier evidence ladder, ranging from interface visibility to physical safety consequences.

## Threat actor and campaign activity

<!-- segment_id: period-actors-p2 -->
<!-- source_fingerprint: 66cd781dcb1d465fb8280f8d8ee6f792377fb7b01a0d55a85f877afc58e0af65 -->
<!-- citations: S5, S6 -->

Dolphin Malware Uses Rank. Dolphin X is a Windows-based remote access trojan, or malware designed to let operators access an infected system remotely. It uses an AI-driven profiler to automate victim triage and rank targets. The malware is marketed as a credential stealer for browsers, cryptocurrency wallets, and cloud command-line tools. It uses control-flow rewriting and string re-encryption to evade detection. Dolphin X exfiltrates .env files, SSH keys, cloud access tokens, and browser login information from more than 300 applications. Its operator panel includes controls to start the AI profiler and retrieve its data.

## Threat actor and campaign activity

<!-- segment_id: period-actors-p3 -->
<!-- source_fingerprint: 66cd781dcb1d465fb8280f8d8ee6f792377fb7b01a0d55a85f877afc58e0af65 -->
<!-- citations: S7, S8 -->

Chaos Ransomware is deploying a new backdoor called msaRAT. It routes command-and-control traffic, meaning instructions between attackers and malware, through web browsers to bypass network detection. The malware runs as a DLL in memory and masquerades as a Windows update. Delivery uses an MSI installer. For communication, it sends HTTPS requests to Cloudflare, uses STUN requests to Google, and relies on a WebRTC data channel relayed through Twilio.

## Threat actor and campaign activity

<!-- segment_id: period-actors-p4 -->
<!-- source_fingerprint: 66cd781dcb1d465fb8280f8d8ee6f792377fb7b01a0d55a85f877afc58e0af65 -->
<!-- citations: S10, S11, S9 -->

Laundry Bear, a Russian state-sponsored group, is exploiting a zero-click stored cross-site scripting vulnerability in Zimbra Collaboration Suite to compromise government and commercial networks. The flaw, CVE-2025-66376, affects the Classic UI and lets malicious CSS import directives run JavaScript silently, without user interaction. That can enable the theft of credentials and two-factor authentication tokens, which are sent to a VPS running the Flowerbed collection framework.

## Vulnerabilities and exploitation

<!-- segment_id: period-vulnerabilities-p1 -->
<!-- source_fingerprint: 70dcfd796805413e3215375a17173492cf847211a93f33d4c0dc555ddc07512c -->
<!-- citations: S15 -->

Dnsmasq DNS Remote Heap Buffer Overflow, reported by Exodus Intelligence, involves an unsafe string-copy operation while processing escaped domain names. The flaw creates a heap buffer overflow, which can be leveraged for remote code execution. A response for “overflow.me” containing CNAME records can trigger the overflow by overwriting the next pointer of a bigname buffer. The corrupted pointer can then support a write-what-where operation against function pointers in the dynamic linker, ld.so, using “overwrite.me”.

## Vulnerabilities and exploitation

<!-- segment_id: period-vulnerabilities-p2 -->
<!-- source_fingerprint: 70dcfd796805413e3215375a17173492cf847211a93f33d4c0dc555ddc07512c -->
<!-- citations: S17 -->

A Millisecond of Predictability: Why CVE-2026-11374 Is… CVE-2026-11374 is an unauthenticated account-takeover vulnerability in ManageEngine products integrated with AD360. The flaw uses predictable millisecond timestamps as single sign-on, or SSO, tickets, which could let an attacker impersonate users. The described process sends a GET request to a protected endpoint with a candidate ticket in the SSO cookie and a mismatched product name in a second cookie. It then submits the form to the authentication endpoint to establish an authenticated session.

## Vulnerabilities and exploitation

<!-- segment_id: period-vulnerabilities-p3 -->
<!-- source_fingerprint: 70dcfd796805413e3215375a17173492cf847211a93f33d4c0dc555ddc07512c -->
<!-- citations: S3, S4 -->

Ubuntu Snap-confine has a local privilege-escalation vulnerability, where attackers can exploit a race during sandbox initialization to gain root privileges. A second race can widen file permissions before ownership transfer, allowing a malicious rules file in the runtime udev rules directory to bypass AppArmor confinement and force systemd-udevd to execute commands as root.

## Closing

That was your RedWatch briefing. The complete references and auditable script accompany this recording.
