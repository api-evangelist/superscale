---
name: Superscale
description: Use Superscale when building, testing, and scaling performance advertising campaigns. Reach for this skill when you need to research competitor ads, generate static or video creative, publish to ad platforms, monitor campaign performance, or automate recurring marketing workflows. Agents should use Superscale for end-to-end ad production: from research and creative generation through publishing and performance analysis.
metadata:
    mintlify-proj: superscale
    version: "1.0"
---

# Superscale Skill

## Product summary

Superscale is an autonomous AI marketing agent that researches, creates, and runs paid ads. It takes a product link, brand context, and a brief, then produces research insights, static ads, video ads, scripts, and campaign recommendations—all grounded in your brand and market data. The agent works through a research → creation → media-buying loop: it analyzes competitor ads and your account performance, generates creative variations, and publishes to Meta, TikTok, Google, and other platforms with your approval. Key files and concepts: **context** (brand, product, audience, and reference assets), **projects** (organize work by campaign or client), **integrations** (connect ad platforms and data sources), **custom skills** (repeatable workflows), and **scheduled runs** (recurring agent jobs). Primary docs: https://docs.superscale.ai

## When to use

Use Superscale when:
- **Generating ads**: You need static images, UGC videos, or scripts for a product or campaign.
- **Researching competitors**: You want to find live competitor ads, identify winning hooks, and score likely performers.
- **Publishing campaigns**: You're ready to launch ads to Meta, TikTok, Google, or other connected platforms.
- **Monitoring performance**: You need to identify winners, waste, fatigue, and patterns in live campaigns.
- **Automating workflows**: You want recurring research, creative refreshes, or health checks on a schedule.
- **Managing creative at scale**: You're producing ads for multiple products, campaigns, or clients in one workspace.

Do not use Superscale for: account setup, billing, authentication, or platform-specific targeting rules (Superscale keeps targeting broad by design).

## Quick reference

### Core workflow steps
1. **Set up context**: Add brand, products, audiences, and reference assets so the agent reuses them.
2. **Brief the agent**: Describe the ad (audience, angle, format, references).
3. **Generate a batch**: Ask for multiple variations; let performance pick the winner.
4. **Iterate**: Refine one element at a time (hook, visual, layout).
5. **Export or publish**: Download files or publish directly to connected ad accounts.
6. **Monitor**: Track winners, waste, and fatigue; feed findings back into context.

### Context levels (cascade from workspace → brand → product)
| Level | Holds | Reused across |
| --- | --- | --- |
| **Workspace** | Shared settings, integrations, team access | All brands and products |
| **Brand** | Identity, guidelines, voice, competitors, ad accounts | All products under that brand |
| **Product** | Specific offer, pricing, imagery, audience segment | All creatives for that product |

### Generation types and costs
| Type | Best for | Cost | Time |
| --- | --- | --- | --- |
| **Static ads** | Fast testing, multiple hooks, feed/story placements | Lower | Minutes |
| **UGC video** | Testimonial-style, direct-response, creator talking to camera | Higher | 5-15 min |
| **B-roll video** | Product demo, app screens, real footage with voiceover | Higher | 5-15 min |
| **Seedance formats** | 9:16 vertical, multiple styles (lifestyle, POV, before/after, etc.) | Higher | 5-15 min |

### Integration capabilities at a glance
| Platform | Read | Publish | Manage | Notes |
| --- | --- | --- | --- | --- |
| **Meta Ads** | ✅ | ✅ | ✅ | Campaign, ad set, ad creation; pause/resume; budget changes; approval-gated |
| **TikTok Ads** | ✅ | ✅ (video only) | ✅ | Campaign and ad group setup; approval-gated ad creation |
| **Google Ads** | ✅ | ✅ (Search only) | ✅ | Search campaign creation; responsive search ads; approval-gated |
| **Shopify** | ✅ | — | — | Product catalog, inventory, sales analytics |
| **Google Analytics** | ✅ | — | — | Acquisition, audience, landing page, event signals |
| **Meta/TikTok organic** | — | ✅ | — | Instagram Reels, TikTok organic posts (not ads) |

### Custom skills vs. context files
| Use context files for | Use skills for |
| --- | --- |
| Brand voice, ICPs, claims, testimonials, legal rules, competitor lists, past learnings | Step-by-step workflows, recurring analyses, report formats, creative formulas, approval rules, playbooks |

## Decision guidance

### When to generate statics vs. video
| Choose statics when | Choose video when |
| --- | --- |
| Testing multiple hooks quickly | You have a clear script or story to tell |
| Budget is tight (lower credit cost) | You need a testimonial or creator presence |
| You need many aspect ratios fast | The product demo or transformation matters |
| Feed/story placements are primary | TikTok/YouTube/Reels are primary channels |

### When to iterate vs. start fresh
| Iterate when | Start fresh when |
| --- | --- |
| Direction is right, one element needs fixing | Product, audience, or strategy is wrong |
| You want to refine hook, copy, or layout | The asset is built on the wrong foundation |
| You're testing one variable | Multiple elements need to change |

### When to use read-only vs. write access for integrations
| Read-only | Write access |
| --- | --- |
| You want analysis and recommendations only | You want Superscale to publish or manage campaigns |
| You have strict review processes | You trust approval cards to gate platform actions |
| You upload creatives manually to platforms | You want direct publishing from Superscale |

### When to schedule a run vs. chat manually
| Schedule when | Chat manually when |
| --- | --- |
| The task repeats (weekly, daily, monthly) | You're exploring or need immediate feedback |
| The objective is self-contained (no follow-ups needed) | You need to ask clarifying questions mid-task |
| You want consistent cadence (Monday health check) | You're testing a one-off idea |

## Workflow

### Typical ad production workflow

1. **Set up context once**
   - Add brand (website, identity, guidelines, voice).
   - Add products (links, pricing, imagery, descriptions).
   - Add audiences (ICPs, customer language, pain points).
   - Add reference assets (winning ads, brand examples, competitor ads).

2. **Research before creating**
   - Run competitor research to find live ads, hooks, and formats.
   - Analyze your own account performance (if connected) to identify winners and patterns.
   - Save findings as context or references for the next brief.

3. **Brief the agent clearly**
   - Audience: who the ad is for.
   - Angle: pain, desire, value prop, or objection.
   - Format: static, UGC, B-roll, or Seedance style.
   - References: attach winning ads, product shots, or brand examples.
   - Guardrails: what must stay fixed (product, layout, tone).

4. **Generate a batch**
   - Ask for 3–5 variations around the same hypothesis.
   - Attach exact assets (product images, logos, screenshots) if they must be accurate.
   - Let the agent use your context instead of re-explaining brand basics.

5. **Iterate surgically**
   - Lock what works (product, layout, hook structure).
   - Change one variable (headline, visual direction, CTA).
   - Generate 1–4 variants to compare.

6. **Export or publish**
   - Export files for manual upload, or use direct publishing if connected.
   - Review approval cards before platform actions run.
   - Everything starts paused; you control when it goes live.

7. **Monitor and learn**
   - Track winners (high CTR, CPA, ROAS), waste (low signal), and fatigue (frequency decay).
   - Save winning ads as references for the next batch.
   - Feed performance patterns back into context or briefs.

8. **Automate recurring tasks**
   - Schedule weekly competitor scans, Monday health checks, or Friday creative refreshes.
   - Attach skills for repeatable methods (e.g., "run our weekly Meta audit").
   - Scheduled runs still wait for approval before platform actions execute.

### Typical research workflow

1. **Find competitors**: Superscale discovers competitors from your website; you confirm or correct the list.
2. **Pull live ads**: The agent surfaces ads from ad libraries, scored by likelihood of performance.
3. **Filter and save**: Narrow by format, platform, or status; favorite or save useful ads.
4. **Analyze patterns**: Look for repeated hooks, proof points, offers, and visual styles.
5. **Brief from research**: Use competitor structure as a reference: "Keep this hook pattern, replace the product."

## Common gotchas

- **Relying on prompts alone**: Context is the foundation. Set up durable brand, product, and audience context once; reuse it across all briefs instead of re-explaining in every prompt.
- **Not attaching exact assets**: If a logo, product image, UI, or price must be exact, attach the source file. Do not rely on the model to reconstruct commercial details from memory.
- **Generating too much at once**: Start with small batches (3–5 variations) to compare before scaling volume. Large batches waste credits if the direction is wrong.
- **Iterating broadly instead of surgically**: "Make it better" wastes credits. Lock what works and change one variable: "Keep the product and layout; only rewrite the headline."
- **Ignoring approval cards**: Approval cards appear before ad-platform actions that affect delivery, spend, or live creative. Review them carefully; they are your control gate.
- **Connecting write access without understanding scope**: Read-only is fine for analysis. Write access lets Superscale publish or manage campaigns. Understand what each permission does before granting it.
- **Scheduling without a self-contained objective**: Scheduled runs cannot ask follow-up questions. Make the objective detailed enough to run autonomously (e.g., "Find five new competitor ads and explain which format to test").
- **Forgetting to save winners**: When an ad performs well, save it as a reference. The best brief for the next ad is a previous winner.
- **Treating video like statics**: Video is expensive. Write or approve the script first, attach exact product visuals, and use small test batches before scaling.
- **Assuming broad targeting is a limitation**: Superscale keeps targeting broad by design (country, age, gender). The angle and creative do the work; let the platform's delivery system find the audience.

## Verification checklist

Before submitting work or publishing:

- [ ] **Context is complete**: Brand, product, and audience context are set up and current.
- [ ] **References are attached**: Exact assets (product images, logos, winning ads) are attached if they must be accurate.
- [ ] **Brief is specific**: Audience, angle, format, and test variable are clear (not "make an ad").
- [ ] **Batch size is reasonable**: Asking for 3–5 variations, not 20.
- [ ] **Iteration is surgical**: Only one variable is changing; everything else is locked.
- [ ] **Approval cards are reviewed**: Before publishing, check the approval card for platform, action, and fields.
- [ ] **Integrations are connected**: If using performance data or publishing, the right platforms are linked.
- [ ] **Scheduled runs are self-contained**: If scheduling, the objective does not require follow-up questions.
- [ ] **Winners are saved**: High-performing ads are saved as references for the next batch.

## Resources

- **Comprehensive navigation**: https://docs.superscale.ai/llms.txt — Full page-by-page index for agent reference.
- **Getting started**: https://docs.superscale.ai/getting-started/quickstart — Set up your first brand and generate your first ads in 10 minutes.
- **Context setup**: https://docs.superscale.ai/context/overview — Understand how to build durable brand, product, and audience context.
- **Integration capabilities**: https://docs.superscale.ai/integrations/capabilities — Platform-by-platform matrix of what each integration can read, publish, and manage.

---

> For additional documentation and navigation, see: https://docs.superscale.ai/llms.txt