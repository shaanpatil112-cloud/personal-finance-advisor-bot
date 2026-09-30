# Personal Finance Advisor Bot

An AI-powered personal finance assistant that helps individuals record income, track expenses by category, get personalized budget plans, and follow their savings progress.

**Live demo:** <your-demo-link>

## Features

- Record monthly income from one or more sources
- Log daily and weekly expenses by category (rent, food, transport, entertainment, etc.)
- AI-generated budget plans with category limits
- Overspending detection and saving suggestions
- Monthly financial report: income vs. expenses, savings achieved, goals for next month
- Savings goal tracking

## Use cases

| User | How the bot helps |
|------|-------------------|
| Salaried professional | Finds overspending areas and builds a monthly budget with saving tips |
| College student | Sets realistic limits on a fixed allowance and flags unnecessary spending |
| Freelancer | Adapts budgets to variable income and suggests an emergency fund |
| Household manager | Consolidates family income and expenses and highlights budget overruns |

## Tech stack

- **Backend:** Python, Flask
- **Database:** SQLAlchemy (SQLite for development)
- **AI engine:** <your AI provider or model>
- **Frontend:** HTML, CSS, JavaScript

## Project structure

```
personal-finance-advisor-bot/
├── app.py
├── models.py
├── routes/
├── services/
│   └── ai_advisor.py
├── templates/
├── static/
├── requirements.txt
└── README.md
```

## Getting started

```bash
# 1. Clone the repository
git clone https://github.com/shaanpatil112-cloud/personal-finance-advisor-bot.git
cd personal-finance-advisor-bot

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set environment variables
cp .env.example .env            # then add your AI API key

# 5. Run the app
flask run
```

Open http://127.0.0.1:5000 in your browser.

## Configuration

Create a `.env` file in the project root:

```
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///finance.db
AI_API_KEY=your-api-key
```

Never commit `.env` to GitHub. Add it to `.gitignore`.

## API endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/income` | Add income |
| POST | `/expenses` | Log an expense |
| GET | `/expenses?month=YYYY-MM` | List expenses for a month |
| POST | `/budget/generate` | Generate an AI budget plan |
| GET | `/insights` | Overspending areas and saving tips |
| GET | `/report/<month>` | Monthly financial report |
| POST | `/goals` | Create a savings goal |

## Future enhancements

- Predictive spending analytics
- Investment suggestions
- Goal-based savings tracking
- AI-driven financial health monitoring

## Disclaimer

This project provides general budgeting guidance and is not professional financial advice.

## Author

Shaan Patil – https://github.com/shaanpatil112-cloud
