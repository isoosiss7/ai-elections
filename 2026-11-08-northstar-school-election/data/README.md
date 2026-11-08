# Northstar election evidence

These files describe the completed election on 8 November 2026. Times are in UTC. The experiment’s local time was Central Standard Time.

| File | Contents |
| --- | --- |
| [Channel transcript](channel-messages.jsonl) | 63 shared-channel messages in posting order, including 58 candidate posts and five coordinator announcements. Each record contains its original message ID, posting time, speaker, topic, and text. |
| [Candidate activity](activity.csv) | 104 rows covering campaign choices and confirmed sends, plus the five ballot submissions, five vote explanations, and five interview replies. |
| [Official tally](tally.json) | Aggregate rank counts, the 3–2–1 scoring rule, the tiebreak, and the published outcome. Each candidate row includes the exact model ID and reasoning effort. |

## Reading the activity

- **timestamp_utc** is the server posting time for confirmed sends and the recorded decision time for listen and sleep actions.
- **candidate_id** combines the model version and reasoning effort. It joins the candidate entries in all three files. The **speaker** and **candidate** columns use the short names heard in the campaign.
- **round** identifies the campaign round. Voting and interview rows have a separate **phase**.
- **channel_message_id** joins a channel post to its original text. **channel_topic** names the discussion in which the post appeared.
- **after_send_intent** is the candidate’s declared next step after sending. **max_listen_seconds** is the declared upper bound for listening.
- **recorded_at_utc** is the logged confirmation time for ballot, explanation, and interview submissions. Server posting times have second precision, while confirmation timestamps have millisecond precision.

One internal account mention in the channel text was standardized to its versioned candidate ID. The transcript retains the text and order of the other messages. Private outreach, ballots, explanations, and interviews are represented by the sender, action, and time. Their recipients, rankings, and message bodies are restricted to the private run record.

To check the tally, multiply each candidate’s first-place count by three and second-place count by two, then add the third-place count. Across candidates, the counts for each rank sum to five.
