<div align="center">

<img src="https://images.unsplash.com/photo-1677442136019-21780ecad995?auto=format&fit=crop&w=1600&q=85" alt="Abstract generative AI neural network artwork" width="100%" />

### ✦ AI News Summarizer

  From information overload to clear insight — powered by AI.
  An AI-powered automation workflow that turns news content into concise, easy-to-understand summaries, helping you spend less time scrolling and more time learning.
<p>
  <img src="https://img.shields.io/badge/AI-Generative%20AI-7C3AED?style=for-the-badge&logo=openai&logoColor=white" alt="Generative AI" />
  <img src="https://img.shields.io/badge/Automation-n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n automation" />
  <img src="https://img.shields.io/badge/Project-AI%20Workflow-111827?style=for-the-badge" alt="AI workflow" />
</p>

</div>

### ◈ The idea

  The internet publishes more news than anyone can comfortably keep up with. AI News Summarizer is designed to make that stream easier to digest by bringing news content into an automated workflow and using AI to produce short, useful summaries.
  Less noise. More signal.
  A practical experiment in combining AI with workflow automation to make everyday information consumption smarter.

### ✧ What this workflow is designed to do

  - Collect news content from the sources configured in the workflow.
  - Process articles with AI to extract the main idea and important details.
  - Create concise summaries that are easier to scan than full-length articles.
  - Structure the results so they can be reviewed or stored consistently.
  - Reduce repetitive work involved in manually opening and summarizing multiple articles.
  The exact sources, output fields, and destination depend on the nodes configured in your exported workflow.

### 🔮 Inside the Workflow
  
   Two news feeds. One AI-powered pipeline. A curated news digest delivered to your inbox.

### ⚙️ Workflow Architecture
```
  flowchart LR
    A["⏰ Schedule Trigger"] --> B["📰 RSS: NoralTech"]
    A --> C["📰 RSS: AIBusiness"]
    B --> D["🔀 Merge"]
    C --> D
    D --> E["📦 Data Aggregator"]
    E --> F["✨ Basic LLM Chain"]
    G["🧠 Google Gemini"] -.-> F
    F --> H["📧 Gmail Delivery"]
```

### ◈ Workflow at a glance

```mermaid
  flowchart LR
      A["📰 News Source"] --> B["⚙️ n8n Workflow"]
      B --> C["✨ AI Summarization"]
      C --> D["🧩 Structured Summary"]
      D --> E["📚 Review / Store Results"]
  
      classDef source fill:#172554,stroke:#60A5FA,color:#FFFFFF
      classDef automation fill:#3B0764,stroke:#C084FC,color:#FFFFFF
      classDef ai fill:#4C1D95,stroke:#A78BFA,color:#FFFFFF
      classDef output fill:#064E3B,stroke:#34D399,color:#FFFFFF
      class A source
      class B automation
      class C ai
      class D,E output
```
### ✦ Why it matters

  <table>
    <tr>
      <td width="50%">
        <h3>⚡ Faster reading</h3>
        Get the central message without starting with every full article.
      </td>
      <td width="50%">
        <h3>🧠 AI-assisted understanding</h3>
        Turn long-form content into a more approachable first-pass summary.
      </td>
    </tr>
    <tr>
      <td width="50%">
        <h3>🔁 Repeatable process</h3>
        Use a workflow instead of repeating the same manual steps.
      </td>
      <td width="50%">
        <h3>🧱 Extendable design</h3>
        Add new sources, filters, destinations, or notification steps as the project evolves.
      </td>
    </tr>
  </table>

### 🖼️ In the world of generative AI

  <div align="center">
    <img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=1200&q=85" alt="Connected digital world representing information networks" width="49%" />
    <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=1200&q=85" alt="Electronic circuitry representing technology and AI systems" width="49%" />
  </div>

  <p align="center"><em>Visuals represent the broader AI and information-technology theme; they are illustrative, not screenshots of the workflow.</em></p>

### 🧰 Technology stack
  Component	Role
  n8n	Connects the steps into an automated workflow
  Generative AI model	Produces article summaries based on the configured prompt
  News source / feed	Supplies the content to summarize
  Output destination	Makes summaries available for review or storage

### 🚀 Run it yourself

  1. Export the workflow from your n8n workspace as a JSON file.
  2. Keep the exported file in this repository, for example at workflow/ai-news-summarizer.json.
  3. Import the JSON into your own n8n workspace.
  4. Configure the required news-source URLs and AI model.
  5. Add your credentials using n8n's credential manager.
  6. Review the prompt and adjust the summary format to your needs.
  7. Test with a small sample, verify the results, and then enable the workflow according to your setup.
  Before you run it
  - Configure your own credentials; exported workflows may not include working authentication.
  - Confirm that the news sources permit your intended use.
  - Verify summaries against the original article before relying on important claims.
  - Avoid publishing API keys, access tokens, private URLs, or personal data.
   
### 🧪 Ideas for the next version

  - [ ] Categorize stories by AI, technology, business, science, and other topics.
  - [ ] Add keyword filters to focus on specific interests.
  - [ ] Detect duplicate articles before summarizing.
  - [ ] Include the original headline, source, publication date, and article link.
  - [ ] Save summaries to Google Sheets, Notion, or a database.
  - [ ] Send a daily digest through email or a messaging platform.
  - [ ] Add a relevance score and a configurable summary length.

### 📂 Suggested repository layout
```
  ai-news-summarizer/
  ├── README.md
  ├── workflow/
     └── ai-news-summarizer.json
```

### 🔐 Security

  Never commit secrets. Store API keys and OAuth credentials in n8n's credential manager or environment variables. Before sharing the workflow JSON, inspect it for sensitive values and remove anything private.

### 🌱 What I learned

  This project is a hands-on exploration of:
  - Designing multi-step automation workflows.
  - Applying generative AI to practical information-processing tasks.
  - Writing prompts for concise, useful summaries.
  - Connecting external data sources with AI services.
  - Thinking about reliability, output structure, and credential security.

### ✨ How it works
```
  Collect: The Schedule Trigger initiates the workflow and retrieves articles from the configured RSS feeds.
  Combine: The Merge node brings together incoming items from both sources.
  Aggregate: The Data Aggregator organizes the collected news for processing.
  Summarize: Google Gemini processes the content through the Basic LLM Chain to generate concise AI-powered summaries.
  Deliver: Gmail sends the generated news digest to the configured recipient.
```
### 🪄 The bigger picture

  AI is most useful when it helps people act on information—not simply generate more of it. This project explores one small way to make a high-volume information stream easier to navigate.
  <div align="center">
  
  Built with curiosity • powered by automation • enhanced by AI
  If this project sparks an idea, feel free to ⭐ the repository or suggest an improvement.
</div>
