# VPS remote desktop: Windows license or Linux with xrdp, how much RAM you need, and what the bill becomes after the promo (full plan table)

A remote desktop VPS costs $7 a month at one provider and $88 at another for what looks like the same product, and most of that gap is Windows Server licensing, not hardware. Contabo's own pricing page lists an Ubuntu VPS 6 at $7.20/month and a Windows Server VPS 12 at $87.60/month, and states plainly that the Windows option "Requires Windows Server (additional licensing cost)". The second thing to settle before you compare any prices is what you are actually buying: a self-managed VPS where you get root on the operating system, or a hosted RDP account where you get a desktop and, in most cases, no admin rights. Those two products share a keyword and little else.

> **Quick pick:** For one always-on desktop that you set up yourself, the **KVM 6 vCPU / 8 GB** plan at **$39.00/month** is the realistic entry point in Spin Servers' current KVM line. The $12.00/month 2 GB plan is fine for a single light session or a Linux desktop, and the 16 GB tier at $74.00/month is what you want if a trading terminal or several browser profiles will be running around the clock. 👉 [Check the current KVM plan prices and billing terms](https://bit.ly/Spinservers)

## The KVM plans Spin Servers lists right now

Every plan below includes a 1 Gbps network port, one IPv4 and one IPv6 address, and RAID-10 SSD storage. Prices are USD and shown as monthly "starting from" figures on the plan cards.

| Plan | vCPU / RAM | Storage / bandwidth | Price (USD) | Order |
| --- | --- | --- | --- | --- |
| KVM 2 vCPU 2 GB (40 GB SSD) | 2 / 2 GB DDR4 | 40 GB SSD, 4 TB/mo | from $12.00/mo | [ View plan](https://bit.ly/Spinservers) |
| KVM 4 vCPU 4 GB (80 GB SSD) | 4 / 4 GB DDR4 | 80 GB SSD, 8 TB/mo | not listed on the card | [ View plan](https://bit.ly/Spinservers) |
| KVM 6 vCPU 8 GB (120 GB SSD) | 6 / 8 GB DDR4 | 120 GB SSD, 8 TB/mo | from $39.00/mo | [ View plan](https://bit.ly/Spinservers) |
| KVM 8 vCPU 8 GB (160 GB SSD) | 8 / 8 GB DDR4 | 160 GB SSD, 10 TB/mo | from $45.00/mo | [ View plan](https://bit.ly/Spinservers) |
| KVM 12 vCPU 12 GB (160 GB SSD) | 12 / 12 GB DDR4 | 160 GB SSD, 10 TB/mo | not listed on the card | [ View plan](https://bit.ly/Spinservers) |
| KVM 16 vCPU 16 GB (320 GB SSD) | 16 / 16 GB DDR4 | 320 GB SSD, 15 TB/mo | from $74.00/mo | [ View plan](https://bit.ly/Spinservers) |
| Advanced 32 vCPU 32 GB (500 GB SSD) | 32 / 32 GB | 500 GB SSD, 20 TB/mo | not listed on the card | [ View plan](https://bit.ly/Spinservers) |

Three of the seven cards publish a starting price and four do not, so those fields read "not listed" rather than a number I invented. A fourth row item worth knowing before you order: **port 25 is closed by default on every Spin Servers VPS**, and opening it requires a ticket with a justification that the company can refuse. If your desktop workload sends mail, plan around that.

The KVM line is sold as application servers, and the plan pages do not advertise a Windows Server add-on or an RDP-ready image. If Windows is a hard requirement rather than a preference, ask support what license and image they can provide before you pay, because the answer changes the total cost far more than the plan tier does.

## Windows or Linux: pick the desktop before you pick the plan

Windows gives you RDP built in, a desktop layout that most people already know, and the shortest path from "server delivered" to "I can see a screen". It also requires a Windows Server license, which Contabo flags as an additional cost on its own product page, and that line item is why a Windows desktop VPS can land near $90/month while an equivalent Linux machine sits near $7.

Linux takes the other route. You run a desktop environment such as XFCE, GNOME or KDE and connect over RDP through xrdp, or over VNC, or through X11 forwarding. It is free, it runs in less memory, and it is more efficient for anything that lives on a server. It also assumes you can configure it yourself, and you will be applying security updates on your own schedule.

The practical rule: if the thing you need to run only exists on Windows, buy Windows and accept the license line. If the thing you need is a graphical desktop, a browser and a handful of Linux-native tools, xrdp on a cheaper Linux plan will do the job, and you can move the saved $70 into more RAM.

Neither path changes what the provider owes you. On a hosted RDP account, you usually get a desktop and no root access, which limits how deeply you can install or configure software. On a self-managed VPS, you get the machine and the root password, and you own the consequences.

## What the bill becomes after the promo ends

Headline prices in this category are frequently 24-month prepayments, and the renewal figure is printed in smaller text. Hostinger's KVM 1 is the clearest example: $6.49/month for the first term, which works out to $155.76 paid up front for 24 months, then renews at $11.99/month, so the second 24 months cost 24 × $11.99 = $287.76. That is roughly 1.85 times the first term, on the same hardware. Contabo's prices on the same page carry the qualifier "for the first 24 months" for the same reason.

Spin Servers advertises its KVM tiers as monthly prices with no multi-year prepayment attached to the number on the card. That does not automatically make it cheaper than a discounted two-year deal, but it does mean the price you see is not a one-time entry fee you have to renegotiate in two years.

👉 [See how Spin Servers prices 8 GB and 16 GB of RAM on a monthly basis](https://bit.ly/Spinservers)

## Limits that only turn up after you have paid

- **Regional traffic quotas hide in footnotes.** OVHcloud's Asia-Pacific VPS locations (Mumbai, Singapore, Sydney) carry monthly allowances of 1 TB on VPS-1 and VPS-2, 3 TB on VPS-3 and VPS-4, and 4 TB on VPS-5 and VPS-6. Go over and the connection is throttled to 10 Mbps, which is enough to make a desktop session feel broken.
- **Not every plan can be upgraded later.** OVHcloud states that VPS ordered in data centers outside the United States cannot be modified or upgraded after delivery. Pick the size you will need in year two, not year one.
- **Managed servers can block RDP entirely.** GoDaddy's own help documentation warns that on Managed or Fully Managed servers you may need to enable administrator access before Remote Desktop will connect at all. Buyers lose hours to this one.
- **No admin rights is a product category, not a bug.** Hosted RDP products typically withhold root or administrative access so you cannot manage software at a deep level. Self-managed VPS products hand over full root access instead. Both are legitimate; buying one while expecting the other is the expensive mistake.
- **Refund terms are not universal.** A 2026 third-party review of Spin Servers' dedicated server line notes that month-to-month services generally carry no refund policy, and scores the provider 6.6/10 overall. Read the cancellation terms at checkout rather than assuming a grace period.

👉 [Open the Spin Servers plan page and confirm the terms before you order](https://bit.ly/Spinservers)

## Connecting to it the first time

On Windows, the client is already installed. Launch Remote Desktop Connection, type the server's IP address, select Connect, then enter the username and password and select OK. macOS users get Microsoft's Remote Desktop app from the App Store; on Linux the usual choices are Remmina, FreeRDP or KRDC; iOS and Android have official Microsoft clients.

Expect a certificate warning on the first connection. A freshly installed server presents a self-signed certificate, so the client has nothing to verify it against. Spin Servers documents the same pattern inside its browser-based noVNC KVM console, where you click Continue on the certificate warning, accept the risk and run the session, with no Java installation required. That console is the fallback when the machine will not boot or the network configuration locks you out: it gives you keyboard, monitor and mouse access before the operating system starts.

If the connection times out instead of warning you, check that the OS actually has remote access enabled and that the firewall allows port 3389. A server that pings but refuses RDP is almost always a firewall rule, not a broken VPS.

## How Spin Servers' prices compare

| Provider | Plan | Specs | Price and terms |
| --- | --- | --- | --- |
| Spin Servers | KVM 6 vCPU 8 GB | 8 GB RAM, 120 GB SSD, 8 TB/mo, 1 Gbps | $39.00/mo, USD |
| Contabo | CLOUD VPS 6 (Ubuntu) | 6 vCPU, 12 GB RAM, 200 GB SSD / 100 GB NVMe | $7.20/mo for the first 24 months, USD |
| Contabo | CLOUD VPS 12 (Windows Server) | 12 vCPU, 48 GB RAM, 400 GB SSD / 200 GB NVMe | $87.60/mo for the first 24 months, USD |
| Hostinger | KVM 2 | 2 vCPU, 8 GB RAM, 100 GB NVMe, 8 TB | $8.79/mo on a 24-month prepay, renews at $14.99/mo, USD |
| HOSTKEY | tiny | 1 vCPU, 0.5 GB RAM, 15 GB SSD | €1.27/mo, EUR, VAT excluded, Windows license status not stated |

The currencies are not interchangeable and the billing models are not either, so treat this as a shape rather than a ranking. Two notes on the cheap end: HOSTKEY markets its VPS line around Windows Server 2022 and 2025, but the plan cards do not say whether a Windows license is included, and a €1.27/month machine with 0.5 GB of RAM cannot be carrying a full Windows Server license at that price. Contabo's sub-$10 entry price applies to the Ubuntu configuration and is tied to a 24-month term.

## FAQ

**How much RAM does a remote desktop VPS need?**
For a single user running a desktop and a browser, 8 GB is the comfortable floor and 2 GB is tight enough that you will notice it. Move to 16 GB if you keep a trading terminal, several browser profiles or a build process running alongside the desktop. RAM runs out before CPU does in desktop workloads.

**Can several people connect at the same time?**
On Windows, concurrent sessions depend on your Windows Server license and how the server is set up, which is why providers phrase it as "may be enabled by your license". On Linux with xrdp you can run multiple sessions, but they all draw from the same RAM and CPU.

**Can I install any software I want?**
Only if you have administrator or root access. Hosted RDP accounts generally do not give it to you. Self-managed VPS plans generally do.

**Does Linux support RDP at all?**
Yes, through xrdp, which lets the standard Windows Remote Desktop client connect to a Linux desktop. VNC and X11 forwarding are the other common routes.

**Why does my client show a certificate warning?**
Because the server's certificate is self-signed and your client has no authority to check it against. Accept it on a server you just provisioned.

**Can I move to a bigger plan later?**
Ask before ordering. Upgrade policies differ by provider and, in OVHcloud's case, by data center region, and a plan you cannot resize is a plan you have to migrate off.

## Which tier to buy

One desktop, email and a browser for a single user: the 8 GB tier at $39.00/month, and the 4 GB tier if you are running a lean Linux desktop instead. A trading terminal, an automation script or anything that must stay up around the clock: 16 GB at $74.00/month, because memory is the constraint that shows up first at 3 a.m. Testing a single Windows-only application a few times a month: a hosted RDP account may cost less per month, provided you accept that you will not have admin rights and may not be able to install what you need.

Before you pay, confirm four things: the currency and whether the price is monthly or a prepaid term, what the renewal costs, whether a Windows Server license is included in the price you are looking at, and whether the plan can be upgraded without a migration. If the desktop matters more than the logo on the invoice, the 8 GB KVM tier is where most people should start.

👉 [Pick a KVM tier and check the monthly price on Spin Servers](https://bit.ly/Spinservers)
