# WGU D322 - Introduction to IT Quiz

A study tool for Western Governors University's Introduction to IT course (D322).

## Features

- **244 quiz questions** covering all course topics
- **138 lessons** of course content for reference
- **Progress tracking** synced across devices via cloud storage
- **Practice mode** with spaced repetition - master questions by answering correctly
- **Final exam mode** requiring 100% to pass
- **Exam persistence** - resume exams after closing browser
- **Study materials** accessible via ? button during quizzes

## Live Demo

https://fullstackkevinvandriel.github.io/quizlet/quiz.html

## Topics Covered

| Category | Questions |
|----------|-----------|
| IT Roles & Functions | 20 |
| Data & Information | 14 |
| Hardware | 28 |
| Networking | 25 |
| Internet | 13 |
| Security | 17 |
| Operating Systems | 17 |
| Programming | 8 |
| Licensing | 10 |
| Databases | 16 |
| Project Management | 8 |
| SDLC | 8 |
| Testing | 6 |
| IT Governance | 11 |
| Software | 7 |
| Ethics | 6 |

## How It Works

### Progress Sync

Enter a keyword when you start - your progress saves to the cloud under that keyword. Use the same keyword on any device to continue where you left off.

### Practice Mode

- Questions appear randomly from your unmastered pool
- Answer correctly 3 times to master a question
- Mastered questions are removed from rotation
- Track your accuracy and remaining questions

### Final Exam

- All 244 questions in random order
- Must score 100% to pass
- Progress saves after each answer - resume if interrupted
- Review correct answers after each question

## Architecture

```
quizlet/
├── index.html          # Course content (138 lessons)
├── quiz.html           # Interactive quiz application
├── README.md           # This file
├── PLAN.md             # Development roadmap
├── worker/
│   ├── worker.js       # Cloudflare Worker for progress sync
│   └── wrangler.toml   # Worker configuration
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Pages deployment
```

## Tech Stack

- **Frontend**: Vanilla HTML/CSS/JavaScript
- **Storage**: Cloudflare Workers KV
- **Hosting**: GitHub Pages
- **CI/CD**: GitHub Actions

## Local Development

1. Clone the repository
2. Open `quiz.html` in a browser
3. Progress sync requires the Cloudflare Worker (or use without sync)

### Deploy Worker (optional)

```bash
cd worker
npm install -g wrangler
wrangler login
wrangler deploy
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make changes
4. Submit a pull request

## License

MIT
