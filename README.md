# Singapore VPS: What a Usable Plan Costs, Which Tier Fits One Site, and What the "Unmetered" Asterisk Hides (Full Plan Table + Renewal Math)

A Singapore VPS that can carry a single low-traffic site starts at $2.25 per month on JustHost.asia's 12-month billing: 1 core, 1 GB RAM, 20 GB NVMe and a 300 Mbit fair-share port. The 2 GB tier costs $3.21 per month and the 4 GB tier $6.23. Those are the rates on the plan page today, with the undiscounted list rate printed beside each one.

Below is the whole lineup, which tier matches which workload, what "unmetered" means when the port is shared, and the add-ons that move the monthly number after you have picked a plan.

> **Most readers should take VPS Sirius (1 GB) at $2.25/month on annual billing.** Move up to Arcturus (2 GB, $3.21) if MySQL or a couple of Docker containers will share the box. Both come with root access and DDoS filtering, and auto-renewal can be switched off in the customer portal.
> 👉 [Check the current Sirius and Arcturus prices and pick a location](https://justhost.asia/en/vps?ref=196392)

**Confirm Singapore is in the location list before you pay.** JustHost.asia's homepage advertises 80 locations across 41 countries, and the VPS plan page names none of them. Location is chosen inside the order constructor, so open it and look for Singapore, or the nearest Asian city offered, for the exact plan you want. Everything else here holds either way; the latency argument only applies if the server really sits in Singapore.

## Does the Singapore location change anything for your users?

Yes, if your visitors are in Singapore, Malaysia, Indonesia, Vietnam or Thailand. Contabo claims ping times as low as 3 ms from its Singapore data centre to Kuala Lumpur and Jakarta, and that is roughly the scale of the improvement you are buying over a US or European host. Exabytes frames it in terms that matter for a website rather than a ping test: hosting in the region cuts load times for regional audiences and helps Core Web Vitals, which shows up in search performance and not just in how fast the page feels.

OVHcloud goes further, stating that server location and IP geolocation are among the key factors in Google ranking and that users are more likely to click a locally hosted site. That is a vendor claim with no study attached, so treat it as a marketing argument. The latency and Core Web Vitals points stand on their own.

For Australian or Japanese traffic, Singapore is a compromise rather than an ideal. If those are your main markets, price a Sydney or Tokyo location before committing to a year.

## The full JustHost VPS lineup

There are two product lines. The "Special" line is fixed-configuration NVMe. The standard line lets you pick HDD, SSD or NVMe at three RAM sizes, and the price moves with the disk type. Prices below are the 12-month rate, with the list rate in brackets.

### NVMe Special offers

| Plan | vCPU / RAM / NVMe | Port (fair-share) | 12-month price (list) | Order |
| --- | --- | --- | --- | --- |
| VPS Sirius | 1 core / 1 GB / 20 GB | 300 Mbit | $2.25 ($2.81) | [ Order Sirius](https://justhost.asia/en/vps?ref=196392) |
| VPS Arcturus | 1 core / 2 GB / 30 GB | 300 Mbit | $3.21 ($4.01) | [ Order Arcturus](https://justhost.asia/en/vps?ref=196392) |
| VPS Vega | 2 cores / 4 GB / 80 GB | 500 Mbit | $6.23 ($7.79) | [ Order Vega](https://justhost.asia/en/vps?ref=196392) |
| VPS Yildun | 4 cores / 8 GB / 200 GB | 750 Mbit | $12.96 ($16.20) | [ Order Yildun](https://justhost.asia/en/vps?ref=196392) |
| VPS Betelgeuse | 6 cores / 12 GB / 400 GB | 750 Mbit | $21.12 ($26.40) | [ Order Betelgeuse](https://justhost.asia/en/vps?ref=196392) |
| VPS Altair | 8 cores / 24 GB / 600 GB | 750 Mbit | $37.92 ($47.40) | [ Order Altair](https://justhost.asia/en/vps?ref=196392) |

### Standard KVM line (IPv4 + IPv6, choose your disk)

| Plan | vCPU / RAM | Disk | 12-month price (list) | Order |
| --- | --- | --- | --- | --- |
| HDD VPS Start | 1 core / 512 MB | 5 GB HDD | $2.60 ($3.25) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| SSD VPS Start+ | 1 core / 512 MB | 5 GB SSD | $3.12 ($3.90) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| NVMe VPS Start++ | 1 core / 512 MB | 5 GB NVMe | $3.38 ($4.22) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| HDD VPS Standard | 2 cores / 2 GB | 25 GB HDD | $8.80 ($11.00) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| SSD VPS Standard+ | 2 cores / 2 GB | 25 GB SSD | $10.56 ($13.20) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| NVMe VPS Standard++ | 2 cores / 2 GB | 25 GB NVMe | $11.44 ($14.30) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| HDD VPS Super | 4 cores / 4 GB | 50 GB HDD | $17.60 ($22.00) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| SSD VPS Super+ | 4 cores / 4 GB | 50 GB SSD | $21.12 ($26.40) | [ Order](https://justhost.asia/en/vps?ref=196392) |
| NVMe VPS Super++ | 4 cores / 4 GB | 50 GB NVMe | $22.88 ($28.60) | [ Order](https://justhost.asia/en/vps?ref=196392) |

A third line exists for IPv6-only servers, advertised from $1.60/month. Read the next section before you go near it.

Line the two tables up and the Special line wins on price at every size it covers: 2 GB is $3.21 there against $8.80 on the standard line, and 4 GB is $6.23 against $17.60. The standard line's reason to exist is disk type and raw capacity for people who need a big HDD, not value per gigabyte.

## 512 MB, 1 GB, or 4 GB?

- **512 MB (Start, Start+, Start++, from $2.60):** a secondary DNS server, a jump host, a monitoring agent, a static site sitting behind a CDN. A WordPress install with a normal plugin load will swap on this.
- **1 GB (Sirius, $2.25):** one low-traffic WordPress site with a page cache, a small API, a staging box. This is the floor for anything you would call a live website.
- **2 GB (Arcturus $3.21):** site and database on one machine, a small SaaS, two or three containers. The Special plan undercuts the standard 2 GB line by more than half, so take it unless the larger HDD is the point.
- **4 GB (Vega $6.23):** several sites, a WooCommerce store doing a few hundred orders a month, CI runners, a modded game server for a small group.
- **8 GB and up (Yildun $12.96, Betelgeuse $21.12, Altair $37.92):** heavier databases, game servers with mod packs, workloads where RAM is what runs out first.

## What "unmetered" actually limits

JustHost labels the port "UNMETERED port: 300 Mbit (fair-share)" and adds "equals to: 93+ TB monthly". Run 300 Mbit flat out for 30 days and you get roughly 97 TB, so the 93 TB figure is arithmetic, not a traffic allowance you can plan around. Fair-share means the other VPS on the same host draw from the same port. What you actually sustain depends on them.

If you need a number that holds, JustHost sells it separately: dedicated 1 Gbps bandwidth at $333.33/month, or +10 Mbps for $2.50/month. That spread tells you how they price shared versus guaranteed throughput better than any marketing line.

The asterisk after "fair-share" points to terms that were cut off in the version of the page I could read. Find that footnote before you move anything bandwidth-heavy onto a 300 Mbit plan.

Other Singapore providers show why this reading matters:

- **OVHcloud** headlines "up to 3 Gbps unmetered bandwidth" and "unlimited traffic", then footnotes that Asia-Pacific VPS get a monthly quota of 500 GB on VPS-1, 1 TB on VPS-2 and VPS-3, and 3 TB on VPS-4, after which the port drops to 10 Mbps. The 3 Gbps is a port speed, not a monthly allowance.
- **Contabo** writes "Unlimited Traffic" with an asterisk pointing to a fair usage policy, which is a different mechanism from OVHcloud's hard quota.
- **Exabytes** splits it explicitly: 80% of VPS bandwidth is allocated to local Singapore access, the remaining 20% to international. If your buyers are in Jakarta rather than Jurong, you are sizing against the smaller pool.

## The add-ons that change the monthly number

- **IPv4 address: $3.31/month.** This is the catch on the IPv6-only line from $1.60. Add IPv4 and you are at $4.91, well above the $2.60 HDD Start that already includes both. Skip the IPv6-only plans unless you genuinely have no use for IPv4.
- **+10 Mbps: $2.50/month.** Worth it only if you have measured a real ceiling on the shared port.
- **Sysadmin services: $9.16/hour.** There is no flat managed tier in the price list, so budget hourly help rather than assuming it is bundled.

👉 [See how the add-ons stack up on the plan constructor](https://justhost.asia/en/vps?ref=196392)

## The second year costs more than the first

The 20% is tied to paying 12 months up front. On monthly billing you pay the list rate, which is about 25% more: $2.81 against $2.25 for Sirius. The plan page does not say whether the discount repeats at renewal, so budget on the list rate and treat anything better as a bonus. At list, Sirius runs $33.72 a year instead of $27.

Two competitor structures show how far this can drift:

| Provider | Headline plan | Price | What to watch |
| --- | --- | --- | --- |
| JustHost.asia | VPS Sirius, 1 GB | $2.25/mo on 12-month term ($2.81 list) | Currency and tax confirmed at checkout |
| OVHcloud | VPS-1, 2 vCore / 4 GB / 40 GB NVMe | S$5.78/mo ex. GST | APAC monthly quota, 10 Mbps after |
| Contabo | CLOUD VPS 4, 4 vCPU / 8 GB / 100 GB SSD | €4.40/mo for first 24 months, €5.50 after | Minimum follow-on term equals the initial term |

Contabo's pattern is the clearest example of the trap. Over three years the CLOUD VPS 4 costs 24 × €4.40 plus 12 × €5.50, or €171.60, against €158.40 if the promotional rate held throughout. Exabytes states it plainly in its own terms: the promotion applies to new registrations only and renewals revert to the default price.

An annual term at JustHost locks the discounted rate for the term you pay. Beyond that, assume list.

## Backups, upgrades and the exit

**Backups.** The JustHost plan page does not list automatic backups among the included features, and the add-on list sells admin time by the hour instead. Ask support what snapshot or backup is included before you migrate a live database. The range across Singapore providers is wide: OVHcloud includes daily backup with seven-day rolling retention, Exabytes runs a weekly off-server backup at midnight on Saturday with two restore points, so anything changed mid-week is not covered until the next run, and Contabo provides snapshots you trigger yourself.

**Upgrades.** JustHost advertises a flexible VPS constructor, but the plan page does not document in-place RAM upgrades. Ask before you buy if you expect to grow within six months. OVHcloud allows one-click upgrades inside the same location only, and downgrades there mean buying a new plan and migrating your data.

**Cancellation.** JustHost's refund policy, revised 7 October 2026, states that turning off auto-renewal stops future renewals without ending the period you have already paid for; early termination has to be requested separately. The policy sets out how a final calculation is produced but the version I could read does not state a day count. A third-party cancellation guide lists a 15-day full refund window on international orders, then pro-rated refunds in one-month units, with IPv4 and IPv6 rentals non-refundable. If the refund window is what decides the purchase for you, get it in writing from support first.

## Who shouldn't buy a VPS here

- **A static site and a couple of mailboxes.** Shared hosting or a static host does this for less and patches itself.
- **Anyone who wants cPanel handled for them.** Exabytes charges S$50/month for its Pro Management tier, which is a fair indication of what handing over the panel costs.
- **Windows users.** Availability varies by location and it is easy to pick one that drops it. OVHcloud's Local Zone VPS, for instance, is Linux-only with no Windows, cPanel or Plesk.
- **Traffic concentrated outside Asia.** The Singapore premium buys you nothing for European or US visitors.

## FAQ

**Is 1 GB of RAM enough for WordPress in Singapore?**
For a cached site with modest plugin load and a few thousand visits a month, yes. Add a page cache and keep the database on the same box only if the site is small. WooCommerce with a real product catalogue wants the 2 GB or 4 GB tier.

**Can I add RAM later without migrating?**
Unknown from JustHost's public pages. The constructor suggests configurability and the add-on list covers bandwidth and IPs rather than memory, so ask support directly. Providers differ sharply here: OVHcloud upgrades in one click but only within the same location.

**What latency will visitors in Malaysia or Indonesia see?**
Singapore is the regional hub, and Contabo's 3 ms claim to Kuala Lumpur and Jakarta from its Singapore facility is the vendor's own figure. Expect a large improvement over US or European hosting, and expect Australia to be noticeably worse than Southeast Asia.

**Is the $2.25 price the renewal price?**
Not stated. The page shows a list rate of $2.81 and a 20% reduction for paying 12 months. Budget on $2.81.

**Which currency am I charged in, and is tax included?**
The plan page shows dollar signs without naming the currency, and does not say whether tax is added at checkout. Confirm both before you enter card details.

## How to decide

One cached site or a development box: Sirius at $2.25/month. Site plus database, or a small SaaS: Arcturus at $3.21. Several sites or a store with real orders: Vega at $6.23. RAM-bound workloads: Yildun at $12.96 and upward.

Three things to confirm at checkout: Singapore appears in the location dropdown for your chosen plan, the currency and any tax added, and whether a snapshot or backup is included. Get those three answered and the rest of the decision is arithmetic.

👉 [Open the JustHost VPS constructor and check Singapore availability for the plan you want](https://justhost.asia/en/vps?ref=196392)
