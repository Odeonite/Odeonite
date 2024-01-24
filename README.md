### Hi there 👋

<!--
**Odeonite/Odeonite** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

name: Waka Readme Stats

on:
  schedule:
    # Runs at 12am IST
    - cron: '30 18 * * *'
  workflow_dispatch:
jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: Odeonite/waka-readme-stats@main
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
           SHOW_OS: "False"
           SHOW_PROJECTS: "False"
           SHOW_LINES_OF_CODE: "True"
           SHOW_TOTAL_CODE_TIME: "True"
           SHOW_COMMIT: "True"
           SHOW_DAYS_OF_WEEK: "True"
           SHOW_LANGUAGE: "True"
           SHOW_OS: "True"
           SHOW_EDITORS: "True"
           SHOW_LANGUAGE_PER_REPO: "True"
