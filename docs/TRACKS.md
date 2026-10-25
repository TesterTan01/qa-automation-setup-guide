# Track guide

This guide explains each track on the roadmap page in plain English: what the tool is, when to pick it, what you will have at the end, and what to watch out for.

If you are new to automation and unsure where to start, jump to [Which track should I pick?](#which-track-should-i-pick).

## Tools every track shares

Every track begins with the same foundations.

| Tool | What it does for you |
| --- | --- |
| **VS Code** | The editor where you write and run your tests. The page also installs helpful extensions. |
| **Git** | Records every change to your work, so you can go back and share it. |
| **GitHub account** | Hosts your projects online. This is your portfolio. |
| **A language runtime** | Node.js (TypeScript or JavaScript), Python, Java with Maven, or the .NET SDK. Your tests are written in this language. |

Check each install worked by running the version command shown on the page, for example `node -v` or `git --version`.

## Web UI tracks

These tools open a real browser, click and type like a user, and check what appears on screen.

### Playwright

**What it is:** A modern browser automation tool from Microsoft. It tests Chrome, Firefox and Safari's engine from one set of tests, waits for pages automatically, and produces an HTML report.

**Languages:** TypeScript, Python, Java, .NET (C#).

**Pick it when:** You want the quickest way to a working, reliable test, or you are starting fresh with no existing framework.

**You will end up with:** A project that runs example tests, an HTML report, and a repo you can push to GitHub.

**Watch out for:**
- The first run downloads browsers, which can take a few minutes.
- The TypeScript setup is the smoothest. Java and .NET need one extra step to download browsers.

### Cypress

**What it is:** A tool that runs tests inside the browser and shows each step as it happens. Very friendly for beginners because failures are easy to see.

**Languages:** JavaScript or TypeScript only.

**Pick it when:** You work on a JavaScript web app, or you want the clearest visual feedback while learning.

**You will end up with:** A project with an interactive test window and a headless command for CI.

**Watch out for:**
- It tests one browser tab at a time, so it suits some workflows less well.
- On Linux you may need extra system libraries. The page links to the official list.

### Selenium

**What it is:** The long-standing industry standard for browser testing. Many companies already have Selenium tests, so knowing it helps in interviews.

**Languages:** TypeScript, Python, Java, .NET (C#).

**Pick it when:** A job advert mentions Selenium, or you want to match what a larger company already uses.

**You will end up with:** A first test that opens Chrome, visits a page and checks its title.

**Watch out for:**
- Chrome or Firefox must already be installed. Selenium 4 downloads the matching browser driver for you.
- You add your own waits and reporting. Playwright and Cypress give you more out of the box.
- The TypeScript setup has the most moving parts. If you see a module error, set `"module": "commonjs"` in `tsconfig.json`.

### Robot Framework

**What it is:** A keyword-driven framework. Tests read almost like plain sentences, so non-programmers can follow them.

**Languages:** Python (it is built on Python).

**Pick it when:** You prefer readable, low-code tests, or your team mixes testers with different coding experience.

**You will end up with:** A `.robot` test file, a VS Code extension for syntax help, and an HTML report.

**Watch out for:**
- Spacing matters. Use four spaces between columns in a `.robot` file.
- The page uses SeleniumLibrary to drive the browser. Robot Framework also has a Playwright-based library you can try later.

## API track

### API testing

**What it is:** Tests that call a service directly, with no browser. They run fast and catch problems early.

**Tools by language:**

| Language | Tools |
| --- | --- |
| TypeScript | Playwright's built-in request tool |
| Python | pytest and the requests library |
| Java | Maven, JUnit and REST Assured |
| .NET (C#) | NUnit and HttpClient |

All four also install **Postman**, so you can explore an API by hand before you automate it.

**Pick it when:** You want fast, stable tests, or you want to learn how the front end and back end talk to each other.

**You will end up with:** A test that calls a public practice API and checks the status code and response.

**Watch out for:** Use a free practice API such as jsonplaceholder.typicode.com, not a real company's service.

## Mobile track

### Appium

**What it is:** A tool that controls apps on a phone or emulator, using the same ideas as browser testing.

**Pick it when:** You need to test an Android app.

**You will end up with:** Java, Android Studio, an emulator, and an Appium server ready for a test client.

**Watch out for:**
- This is the biggest install on the page. Allow time for the downloads.
- The page covers Android set-up only. You then write tests in the language of your choice.
- If the doctor command reports a missing path, set the `ANDROID_HOME` environment variable to your Android SDK folder.

## Performance track

### k6

**What it is:** A load testing tool. You write a short script, and k6 sends many virtual users to your site and reports how it copes.

**Languages:** JavaScript.

**Pick it when:** You want to learn how fast and how stable a system is under pressure.

**You will end up with:** A script that runs ten virtual users for thirty seconds against a practice site.

**Watch out for:** Only run load tests against sites you own or that explicitly allow it. Test.k6.io is made for practice.

## Continuous integration track

### GitHub Actions

**What it is:** A service that runs your tests automatically every time you push code to GitHub. A green tick appears when they pass.

**Pick it when:** You have a working Playwright project and want to show employers a repo that tests itself.

**You will end up with:** A workflow file at `.github/workflows/playwright.yml`, a test run you can open from the **Actions** tab, and a status badge for your README.

**Watch out for:** Finish a Web UI Playwright track first. The workflow is generated when you answer yes during setup.

## Which track should I pick?

| If you... | Start with |
| --- | --- |
| Have never automated anything | Playwright with TypeScript or Python |
| Mostly know JavaScript | Playwright (TypeScript) or Cypress |
| Know Python | Playwright (Python), or Robot Framework for readable tests |
| Work in a Java or .NET company | Playwright or Selenium in that language |
| See Selenium in job adverts | Selenium |
| Want something quick that looks good in a portfolio | Playwright plus the CI track |
| Want to test an Android app | Appium |
| Want to test how a site copes with traffic | k6 |

## A good portfolio plan

1. Build the same three small tests in two tools, for example Playwright and Cypress, against a public practice site.
2. Add a short README to each repo with what you test, how to run it, and a screenshot of the report.
3. Add the CI track so each repo shows a green build.
4. Write a short comparison of what you liked and disliked about each tool. Employers enjoy this kind of reflection.

## If something does not work

- Read the error message. The last few lines usually point to the cause.
- Check the tool's official documentation, since commands change between versions.
- Close and reopen your terminal after installing a tool.
- Search the exact error text, or ask in the Ministry of Testing community.
- If a command on the roadmap page is out of date, please open an issue or pull request on the repository.
