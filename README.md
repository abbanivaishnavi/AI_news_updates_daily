# TOP AI NEWS DAILY 🤖

An n8n workflow that gathers AI-related news, uses Google Gemini to select and summarize the five most important stories, formats the result as an HTML digest, and sends it by email through Gmail.

## Workflow overview

1. **Schedule Trigger** — starts the workflow at the configured time.
2. **RSS Read** — retrieves AI-related stories from a Google News RSS search feed.
3. **Limit** — limits the items passed downstream to 10.
4. **Aggregate** — combines the collected items for the AI step.
5. **Basic LLM Chain + Google Gemini** — selects the top five stories and creates an HTML digest with summaries, key takeaways, and source links.
6. **Gmail** — sends the generated digest by email.

## Workflow preview

![TOP AI NEWS DAILY workflow](screenshots/workflow.jpeg)

## Example email output

![Example daily AI news email](screenshots/sample-email.jpeg)

## Tools used

- **n8n** — workflow automation
- **Google News RSS** — news collection
- **Google Gemini** — AI-assisted selection and summarization
- **Gmail** — email delivery

## Import and configure

1. Download `top-ai-news-daily-workflow.json`.
2. In n8n, import the workflow JSON.
3. Configure your own Google Gemini and Gmail credentials in n8n.
4. Replace `YOUR_EMAIL_ADDRESS` in the Gmail node with your intended recipient.
5. Review the RSS feed, prompt, and schedule for your needs.
6. Test the workflow manually before enabling scheduled runs.

**Note:** Credentials are intentionally excluded from this public export. You must connect your own accounts after importing it. The workflow export does not include private API keys or passwords.

## What I learned

- Building a multi-step workflow in n8n
- Collecting news from an RSS feed
- Limiting and aggregating data
- Using an LLM to summarize and format information
- Sending automated email updates
- Testing and documenting an automation project

## Future improvements

- Add more trusted AI news sources
- Detect duplicate stories
- Include stronger error handling and failure notifications
- Improve the email layout and source attribution

## Author

**Abbani Vaishnavi**

