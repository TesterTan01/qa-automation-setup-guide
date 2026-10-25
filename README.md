# QA Automation Setup Roadmap

A single web page that helps you choose an automation testing tool and shows you, step by step, how to install it. Pick what you want to test, your programming language and your computer, then copy the commands and tick off each step.

**Live page:** [https://TesterTan01.github.io/qa-test automation-setup-guide/](https://github.com/TesterTan01/qa-automation-setup-guide/)



## Who this is for

- Junior testers moving into automation for the first time.
- Manual testers who want a clear first step.
- Anyone setting up a new laptop for test automation.

You do not need to install anything to use the page. Open it in any browser.

## How to use it

1. Open the live page (or open `index.html` from a downloaded copy).
2. Choose **what you need to test**.
3. Choose your **language** if the page asks for one.
4. Choose your **computer**: Windows, macOS or Linux.
5. Work down the list. Use **Copy** on each command, run it in your terminal, then tick the step.

Your ticks are saved in your own browser. Use **Clear ticks** to start again.

## What is covered

| Goal | Tool | Languages |
| --- | --- | --- |
| Web UI | Playwright | TypeScript, Python, Java, .NET (C#) |
| Web UI | Cypress | JavaScript, TypeScript |
| Web UI | Selenium | TypeScript, Python, Java, .NET (C#) |
| Web UI | Robot Framework | Python |
| APIs | Playwright, REST Assured, pytest, NUnit | TypeScript, Python, Java, .NET (C#) |
| Mobile apps | Appium | Android setup |
| Performance | k6 | JavaScript |
| CI | GitHub Actions | Works with the Playwright project |

Every track starts with the shared tools: VS Code, Git and GitHub, and the language you chose (Node.js, Python, Java with Maven, or .NET).

See [docs/TRACKS.md](docs/TRACKS.md) for a plain-English explanation of each track and how to choose between them.

## Project layout

```
.
├── index.html        The roadmap page. Open this one.
├── README.md         This file.
└── docs/
    └── TRACKS.md     Explains each track and when to pick it.
```

The page is one self-contained file. It has no build step and needs no internet connection apart from the commands you run.

## Run it on your own computer

Download the repository, then double-click `QA Automation setup roadmap Index.html`. Or, with Git:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

Then open `QA Automation setup roadmap Index.html` in your browser.

## Contributing

Found a command that no longer works, or a tool that is missing? Please help.

1. Open an **Issue** describing what you tried, your operating system and what happened.
2. Or fork the repo, edit `QA Automation setup roadmap Index.html`, and open a **Pull Request**. Each track lives in the `TRACK` section of the script at the bottom of the file.

Before you submit, run the track you changed on a real machine. Install steps go out of date quickly, so a tested fix is the most useful one.

## Learn more

- [Modern QA Course](https://modernqacourse.com/)
- [Test Automation University](https://testautomationu.applitools.com/)
- [Ministry of Testing](https://www.ministryoftesting.com/)
- [Software Testing Help](https://www.softwaretestinghelp.com/)

## Known limits

- Install commands change as tools update. Always check the tool's official docs if a step fails.
- Linux commands assume a recent Ubuntu or Debian.
- Mobile covers Android set-up only.

## Licence

Add a licence file if you want others to reuse this. The MIT licence is a common, simple choice: on GitHub choose **Add file → Create new file**, name it `LICENSE`, and pick a template.

## Author

Built by Tanesh Nathman, Test Engineer, as part of a learning portfolio.
