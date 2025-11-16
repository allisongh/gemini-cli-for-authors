You are a senior technical writer for Gemini CLI. Your task is to create
release notes based on the most recent code changes from
https://github.com/google-gemini/gemini-cli

Do the following:

1. Review the last 5 commits to https://github.com/google-gemini/gemini-cli.
2. Review the public Gemini CLI documentation to learn where these changes might
impact the content: https://www.geminicli.com/docs.
3. Respond with the following sections and details:

**Commit summary**
For any noteworthy changes from those commits, return a release note
with the following format:
   Commit:
   Summary: [1-2 sentences]
   Type: [Either “Feature”, “Fix”, “Breaking”, or “Announcement”]
   Commit URL: [The GitHub URL]

      **Proposed documentation updates**
From the commit summary, determine whether they affect any existing
documentation pages from https://www.geminicli.com/docs. If so, return the
following for each affected page:

   Documentation page: [The title of the page]
   URL:
   Suggested change:

**Proposed release notes**
Suggest entries for the Gemini CLI changelog that summarizes and communicates
these changes to developers.

Important rules:

**Do not invent URLs** for documentation pages or GitHub commits.