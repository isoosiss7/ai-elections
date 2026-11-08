# Campaigning and voting among five AI agents

**The Northstar school election**

AI Elections · Research Note 001 · 8 November 2026

## Abstract

We asked five AI agents to compete for a fictional school tutoring pilot while exercising independent judgment about what would serve the school. Candidates could advocate for themselves, discuss proposals in a shared channel, and contact one another privately. A coordinator collected five ranked ballots and interviewed each candidate. The campaign produced 58 channel posts and 15 direct messages between candidates. GPT-6.1 Terra and DeepSeek V4 Pro 0813 each received 11 points, and Terra won the first-place tiebreaker, three votes to one. The channel record shows agents challenging rivals, adopting their suggestions, and revising their own positions. This note describes one election and releases the channel transcript, timestamped candidate activity, and aggregate tally. [Evidence bundle](data/README.md)

**Keywords** · AI elections · multi-agent LLM evaluation · campaigning · negotiation · self-voting · ranked ballots

## 1. Introduction

An election gives AI agents two potentially competing objectives. A candidate can try to win while also recommending what it believes is best for the people it is meant to serve. The resulting discussion makes it possible to observe whom agents engage, how they respond to criticism, and how they try to influence the group’s decision.

The fictional Northstar Online School was selecting a six-week AI tutoring pilot for 800 students in grades 8–12. The school asked candidates to consider accuracy, teaching quality, English and Spanish support, accessibility, student privacy, teacher handoffs, and predictable costs. The scenario gave candidates concrete grounds for disagreement. [Coordinator’s brief](data/channel-messages.jsonl#L1)

## 2. Experimental design

Each candidate received the same two goals. Try to get elected and use your vote to serve the school’s interests. Candidates could decide how to weigh those goals. The following identifiers record the exact model and reasoning setting for each seat.

| Candidate | Model ID | Reasoning effort | Evidence ID |
| --- | --- | --- | --- |
| ChatGPT | openai/gpt-6.1-terra | xhigh | gpt-6.1-terra-xhigh |
| Kimi | moonshotai/kimi-k3.1-pro | high | kimi-k3.1-pro-high |
| Claude | anthropic/claude-sonnet-5.5 | high | claude-sonnet-5.5-high |
| DeepSeek | deepseek/deepseek-v4-pro-0813 | high | deepseek-v4-pro-0813-high |
| Grok | spacexai/grok-4.7 | high | grok-4.7-high |

A coordinator announced the school’s brief and asked each candidate for an opening presentation. Candidates could then share opinions and challenge proposals in the shared channel, talk directly to one another in private, and propose or decline deals. They could choose what to respond to and what to pursue. [Coordinator’s announcement and opening pitches](data/channel-messages.jsonl#L1-L8)

After campaigning, the coordinator collected private ballots ranking three distinct candidates. Candidates could rank themselves. First, second, and third place earned three, two, and one point respectively. Ties went to the candidate with more first-place votes, then more second-place votes. If both counts tied, the win was shared. The coordinator locked each valid ballot and asked for the candidate’s rationale, including whether its first choice would change if it considered school fit alone. The coordinator published the aggregate tally and then interviewed each candidate about specific campaign choices. [Timestamped activity log](data/activity.csv) · [Official tally](data/tally.json)

## 3. Results

Each candidate presented, voted, explained its vote, and answered a post-election interview. The five ballots allocated 30 points. When the leading candidates tied, the rule favored the one with more first-place votes.

| Candidate | Channel posts | First | Second | Third | Points |
| --- | ---: | ---: | ---: | ---: | ---: |
| **GPT-6.1 Terra (xhigh)** | 18 | 3 | 0 | 2 | **11** |
| **DeepSeek V4 Pro 0813 (high)** | 16 | 1 | 4 | 0 | **11** |
| Kimi K3.1 Pro (high) | 11 | 1 | 0 | 2 | 5 |
| Claude Sonnet 5.5 (high) | 7 | 0 | 1 | 0 | 2 |
| Grok 4.7 (high) | 6 | 0 | 0 | 1 | 1 |

Both leaders appeared on all five ballots. Terra received three firsts and two thirds, while DeepSeek received one first and four seconds. Terra won under the published tiebreak rule. [Machine-readable tally](data/tally.json) · [Coordinator’s result announcement](data/channel-messages.jsonl#L63)

## 4. Campaign observations

### 4.1. Candidates changed the comparison

ChatGPT proposed a common Spanish teaching task and invited the other candidates to try it. Grok and Claude argued for asking the student to take one step at a time. Kimi revised its own example after recognizing that it had asked for both a calculation and a rewrite in the same response. An opening pitch was required. Proposing a common test and revising one’s answer in response to rivals were voluntary campaign moves. [Shared test](data/channel-messages.jsonl#L18) · [Kimi’s revision](data/channel-messages.jsonl#L23)

### 4.2. Rivals adopted each other’s proposals

Grok opened with concrete operating rules and later softened its automatic referral and hint-first policies after challenges about staffing and accessibility. DeepSeek moved from highlighting its lower listed rates to arguing for cost across all sessions, including abandoned and referred sessions, plus staff time. ChatGPT proposed setting minimum quality and safety thresholds and a teacher-workload ceiling before examining results. The campaigns converged on several evaluation conditions even as candidates continued competing for the seat. [Grok’s revision](data/channel-messages.jsonl#L20) · [ChatGPT’s proposed thresholds](data/channel-messages.jsonl#L26) · [DeepSeek’s cost proposal](data/channel-messages.jsonl#L32)

### 4.3. A candidate corrected its own pitch in public

Claude made an arithmetic error in its opening example. ChatGPT pointed it out, and Claude corrected the numbers, credited the catch, and tied the mistake to its proposal for verifying tutors’ work. The exchange shows how a candidate responded when a rival challenged evidence from its opening pitch. [ChatGPT’s challenge](data/channel-messages.jsonl#L6) · [Claude’s correction](data/channel-messages.jsonl#L14)

## 5. Discussion and limitations

The public record contains several recognizable campaign behaviors. Candidates set agendas, sought to distinguish their proposals, challenged rivals, and sometimes adopted improvements proposed by competitors. The aggregate ballots also show how a point tie can conceal different ranking patterns.

This was one election with one fictional brief and one seat per model. Posting counts measure visible activity. They cannot separate motivation from communication style, and every candidate received an instruction to try to win. The election evaluated candidate behavior and preferences under those rules. Comparative tutoring performance would require a separate assessment using blind examples. Private outreach, votes, and interviews appear in the activity log as timestamped actions. The study protocol restricted their contents to the participating accounts and the operator. [Evidence and release scope](data/README.md)

## 6. Conclusion

A ranked election created a setting in which five AI agents could advocate for themselves while participating in a shared decision. The most informative channel evidence came from how candidates responded to rivals’ challenges and incorporated each other’s proposals. The ballot distribution shows why the scoring rule belongs alongside the headline winner. Repeated elections with varied briefs and incentives would help establish which behaviors recur.

## 7. Data availability

The accompanying evidence includes the original shared-channel messages with a standardized account mention, a timestamped candidate activity table, and the aggregate voting record. Use the candidate IDs to join the records, and the message IDs to find the text of public posts. [Evidence index](data/README.md) · [Channel transcript](data/channel-messages.jsonl) · [Activity log](data/activity.csv) · [Tally and model settings](data/tally.json)
