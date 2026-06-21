# Link Building Strategy — Topical Alignment of the Network

> Brain dump captured 2026-06-21, ~10pm. Nothing actioned yet. This is the
> thinking to pick up in the morning.

## The premise (from the masterclass)

If you boil "what makes a stronger-than-average backlink" down to two things:

1. **Page-level traffic.** Not domain traffic — traffic to the *specific page*
   the link sits on. A link from a page that actually pulls organic visitors
   passes something a link from a dead page never will.
2. **Topical alignment.** The linking domain (and ideally the linking page)
   should already rank for the target keyword or related keywords. The link is
   "endorsed" by a source Google already trusts on that topic.

Underneath both sits the **cosine-similarity** idea: Google represents pages and
topics as vectors (embeddings), and a link from a page whose vector sits close
to the target page's vector carries more relevance weight. The "narrow crawler"
point is the practical version of this — alongside the broad web crawl, there are
crawl/ranking passes that operate on a *tightly clustered* topical neighborhood.
If you're chasing "dentist California," the relevant graph is the dentist-topic
sub-graph, not the whole web. Links from inside that neighborhood count for more.

Old-but-still-relevant names for this same instinct: **Topic-Sensitive PageRank**
(rank computed per-topic, not globally) and **Hilltop** (links from recognized
"expert" pages on a topic are worth disproportionately more).

## The five canonical takeaways (from the slide)

1. **The Binary Traffic Rule** — Only secure backlinks from pages that have their
   own organic traffic. If a page doesn't rank, Google treats the link as low
   value (Reasonable Surfer Patent: weight follows the links a real user would
   plausibly click, and dead pages have no clickers).
2. **Topical Triangulation** — Use content strategy to match related *entities*.
   Authority is identified by how connected your subject matter is to the core
   intent of the query.
3. **Cosine Similarity and Vectors** — If the angle between your site's vector and
   the link source's vector is too wide, authority isn't passed.
4. **Quality over Volume** — Vendor guest-post lists are mostly wasted budget.
   High-relevance link insertions on pages *already ranking for your keywords*
   produce results significantly faster.
5. **The Time Decay Factor** — Low-quality links often cause a temporary rise
   followed by a sharp drop. Only high-relevance links from tight topical
   clusters give sustainable, long-term growth.

> Small technical caveat so we're not caught out: "the web in three dimensions"
> is a teaching simplification — embeddings are high-dimensional, and the crawler
> doesn't literally "stop" at a wide angle. But the operative point is exactly
> right: **relevance gates how much authority flows**, so directionally treat it
> as gospel.

## Where this lands for us

We own ~150 domains. Core business is iGaming. The question on the table:

> Should we be actively reshaping these assets so they're more *topically
> aligned* with our money targets — i.e. making the network's vectors sit
> closer to the iGaming/casino/betting cluster?

Short answer: **yes on relevance, but carefully**, because the same move that
raises topical relevance also raises the network's *footprint*, and those two
pull in opposite directions. The whole game is buying the relevance without
buying the fingerprint.

### The two levers, made concrete

**Lever 1 — Page traffic (your idea here).**
The only traffic that helps is *real organic* traffic to the linking page.
Synthetic/bot traffic is both detectable and worthless for this. So engineering
this means: build pages on the network that genuinely rank and pull visitors,
then point the link from *those* pages. The linking page has to earn its own
keystone before it can pass anything.

**Lever 2 — Topical alignment via long-tail informational content (your idea).**
This is the right instinct. You won't get links from pages ranking for the exact
commercial money term — those are competitors. What you *can* manufacture is
pages ranking for **related, long-tail, informational** terms in the same
cluster. Those pages:
- are realistic to rank (low competition),
- pull their own traffic (feeds Lever 1),
- sit close to the money page in vector space (feeds Lever 2),
- let you use natural, varied, non-spammy anchors and surrounding co-text.

So the two ideas aren't separate — long-tail informational content is the single
mechanism that satisfies *both* levers at once. That's the key realization.

## The tension to respect: relevance vs. footprint

A private network where all 150 domains converge on the same niche, interlink,
and point at the same money sites is the **textbook detectable footprint**.
Homogenizing everything toward iGaming maximizes relevance *and* maximizes
fingerprintability. Don't optimize one into a penalty for the other.

Ways to keep relevance high while keeping the footprint low:

- **Cluster, don't clone.** Group domains into topical clusters (casino, sports
  betting, poker, slots, payments/responsible-gaming adjacency) rather than
  making every domain a carbon copy of the same keyword set.
- **Adjacent, not identical.** Aligned ≠ identical. Vectors should be *near* the
  target, not stacked on it. Adjacency (gambling-adjacent finance, entertainment,
  sports) still raises cosine similarity without making every site a mirror.
- **Tier the network.** Not every domain should link to money pages. Some should
  link to each other / to informational hubs to build the cluster's internal
  authority first.
- **Vary the surface.** Registrars, hosting, CMS, templates, publishing cadence,
  outbound link patterns. Relevance is a content-vector property; footprint is a
  metadata property. You can max the first and minimize the second.

## What "aligned" actually means (so we measure the right thing)

Cosine similarity is about the **semantic content** of the linking page vs. the
target page — not just shared keyword strings. So alignment work is really:

- the linking page's body content sits in the target's topic cluster,
- the anchor text + the sentence around it co-occur with the target topic,
- the linking domain has a track record of ranking for related terms,
- the link sits on a page that's part of a coherent topical hub, not an orphan.

## Proposed link-source scoring (the "chart")

A rubric to grade any candidate linking page on the network. Score each 0–2,
prioritize the high totals.

| Factor                                  | 0 (weak)            | 1 (ok)                  | 2 (strong)                          |
|-----------------------------------------|---------------------|-------------------------|-------------------------------------|
| Organic traffic to the *page*           | none                | some impressions        | ranks + steady clicks               |
| Page ranks for related keywords         | unrelated           | loosely related         | ranks for cluster terms             |
| Content–target vector proximity         | off-topic           | adjacent topic          | same cluster                        |
| Anchor + surrounding co-text relevance  | generic/forced      | brand/URL               | natural topical phrase              |
| Outbound link dilution on the page      | link farm           | several links           | few, editorial-feeling              |
| Footprint hygiene (host/registrar/CMS)  | matches rest of PBN | partially varied        | clean / independent-looking         |

Decision shorthand, traffic × relevance:

```
                 LOW relevance        HIGH relevance
HIGH traffic  |  okay link, but    |  *** prime link ***
              |  build relevance   |  (point money pages here)
--------------+--------------------+----------------------
LOW traffic   |  skip / repurpose  |  build traffic first,
              |                    |  then promote to prime
```

The strategy is to manufacture cells from the bottom-right upward: create
relevant long-tail informational pages (high relevance, low traffic), let them
earn traffic, *then* graduate them into prime linking sources.

## Open questions for the morning

1. **Audit first.** Where do the 150 domains actually sit today — topic clusters,
   per-page traffic, what they already rank for? We can pull this from Ahrefs
   (Site Explorer top pages / organic keywords / traffic per page) before
   deciding what to reshape.
2. **Cluster map.** Which domains naturally belong to which iGaming sub-cluster,
   and where are the footprint risks (shared hosting/registrar/interlink)?
3. **Long-tail backlog.** Build a keyword list of related informational
   long-tails per cluster — these become the content briefs for the linking pages.
4. **Tiering rules.** Which domains link to money pages vs. which only build
   internal cluster authority.

## My bottom line

Your instinct is right and the long-tail informational play is the smart unlock —
it satisfies both the traffic lever (Binary Traffic Rule) and the relevance lever
(Cosine Similarity / Topical Triangulation) with one mechanism. The thing to add
to your thinking is the **footprint counterweight**: pursue *adjacency and
clustering*, not *homogenization*. Align the vectors, vary the metadata.

The slide's **Time Decay Factor** is the clincher for doing this properly: half-
measures don't just under-perform, they actively *reverse* — a spike then a slump.
That means a half-aligned network is arguably worse than no campaign, so this is
worth doing as a deliberate cluster build rather than a quick interlink pass.

Next concrete step is an Ahrefs audit of where the network sits today so we're
reshaping from data, not guesses — happy to run that when you're back.
