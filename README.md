# Aphoric

A focused tool for crawling daily news articles and generating concise summaries. Extract key insights from top stories automatically.

![Aphoric News Crawling Demo](demo.gif) *<!-- Replace with your demo GIF/image -->*

## Features
### **News Crawling**
- Scrape top daily news articles from trusted sources
- Filter by topic/category (e.g., technology, politics)
- Limit results by date range and number of articles

### **Summarization**
- Generate bullet-point summaries from crawled articles
- Export to TXT/JSON/Excel formats
- Preserve source links and metadata

## Installation
```bash
git clone https://github.com/1666sapple/aphoric.git
cd aphoric
pip install -r requirements.txt
```

### File Directories
```bash
news_agent_project/
├── backend/                       # Django backend
│   ├── news_agent/                # Main Django project
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   ├── api/                       # Django API app
│   │   ├── __init__.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── migrations/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── news_scraper/              # Django app for scraping
│   │   ├── __init__.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── migrations/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── tasks.py               # Celery tasks for scraping
│   │   ├── tests.py
│   │   └── views.py
│   ├── ai_agents/                 # AI agent system
│   │   ├── __init__.py
│   │   ├── agents/
│   │   │   ├── __init__.py
│   │   │   ├── scraper_agent.py   # Agent for web scraping
│   │   │   ├── summary_agent.py   # Agent for summarization 
│   │   │   ├── chat_agent.py      # Agent for chatbot
│   │   │   └── search_agent.py    # Agent for web search
│   │   ├── graphs/
│   │   │   ├── __init__.py
│   │   │   ├── scraper_graph.py   # LangGraph for scraper
│   │   │   ├── summary_graph.py   # LangGraph for summary
│   │   │   └── search_graph.py    # LangGraph for search
│   │   ├── tools/
│   │   │   ├── __init__.py
│   │   │   ├── scraper_tools.py   # Scraping tools
│   │   │   └── search_tools.py    # Search tools
│   │   └── utils.py               # Utility functions
│   ├── celery.py                  # Celery configuration
│   ├── manage.py
│   ├── Dockerfile
│   ├── requirements.txt
│   └── .env.example
├── frontend/                      # Next.js frontend
│   ├── public/
│   ├── src/
│   │   ├── app/
│   │   │   ├── layout.tsx
│   │   │   ├── page.tsx
│   │   │   ├── news/
│   │   │   │   └── page.tsx       # News listing page
│   │   │   ├── category/
│   │   │   │   └── [slug]/page.tsx # Category page
│   │   │   ├── summary/
│   │   │   │   └── page.tsx       # Summary page
│   │   │   ├── chat/
│   │   │   │   └── page.tsx       # Chat page
│   │   │   └── search/
│   │   │       └── page.tsx       # Search page
│   │   ├── components/
│   │   │   ├── ui/                # UI components
│   │   │   ├── news/              # News components
│   │   │   ├── summary/           # Summary components
│   │   │   ├── chat/              # Chat components
│   │   │   └── search/            # Search components
│   │   ├── lib/
│   │   │   ├── api.ts             # API client
│   │   │   └── utils.ts           # Utility functions
│   │   └── types/
│   │       └── index.ts           # TypeScript types
│   ├── package.json
│   ├── tsconfig.json
│   ├── .env.local.example
│   └── Dockerfile
├── docker-compose.yml             # Docker Compose configuration
├── .gitignore
├── README.md
└── scripts/
    └── deploy.sh                  # Deployment script

```