# tidylog-kit

Keep your log directories small without thinking about it

Started as a weekend hack, grew on me.

## Installation

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Examples

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## Highlights

- Filter by age (--older-than) or size (--larger-than)
- Dry-run mode shows what would happen, touches nothing
- Archive matched logs into a timestamped .tar.gz
- Exit codes friendly for cron and CI
- Scan directories for log files by glob pattern

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── roadmap.md
│   └── usage.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   └── cli.py
├── tests/
│   └── test_cli.py
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── pyproject.toml
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## 说明

个人练习项目, 谨慎用于生产环境。
