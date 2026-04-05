<h1 align="center">AI-Powered GitHub PR Reviewer (n8n)</h1>

<p align="center">
  Automated Pull Request review system using AI Agent and n8n workflows
</p>

<hr/>

<h2>Overview</h2>

<p>
This project automates GitHub Pull Request reviews by integrating workflow automation with an AI Agent.
It retrieves PR data files, analyzes code diffs, generates insights, and posts structured feedback directly to the Pull Request.
</p>

<hr/>

<h2>Features</h2>

<ul>
  <li>Automated Pull Request detection</li>
  <li>AI-based code diff analysis</li>
  <li>Structured feedback generation:
    <ul>
      <li>Code quality assessment</li>
      <li>Improvement suggestions</li>
      <li>Approval recommendation</li>
    </ul>
  </li>
  <li>Automatic label assignment</li>
  <li>Comment posting on Pull Requests</li>
  <li>End-to-end workflow automation</li>
</ul>

<hr/>

<h2>Workflow</h2>

<img src="https://github.com/YajithVishwa/n8n.workflows/blob/master/pr_review/images/workflow.png" />

<ol>
  <li>Trigger on Pull Request events (opened, updated)</li>
  <li>Fetch PR metadata and file changes</li>
  <li>Send code diffs to AI model</li>
  <li>Process AI response into structured format</li>
  <li>Post review comments and apply labels</li>
</ol>

<hr/>

<h2>Tech Stack</h2>

<ul>
  <li>Workflow Automation: n8n</li>
  <li>Version Control: GitHub</li>
  <li>AI Integration: OpenAI GPT LLM API</li>
</ul>

<hr/>

<h2>Example Review Comment</h2>

<pre><code>Comments By AI Agent

Quality Score - 2

S͟u͟m͟m͟a͟r͟y͟
Adds a new src/main.py with a main() function that defines two variables and attempts to print their sum, then runs main when executed as a script.

S͟t͟r͟e͟n͟g͟t͟h͟s͟
1 - Includes a standard Python entry point guard (if __name__ == '__main__':).
2 - Simple, readable structure for a small script.

C͟o͟n͟c͟e͟r͟n͟s͟
1 - Bug: print(a + c) references c, which is undefined; this will raise a NameError at runtime. Likely meant b.
2 - Trailing whitespace on the line b = 5 .
3 - No return value or tests/validation; the script’s behavior isn’t verified.
</code></pre>

<hr/>

<h2>Permissions</h2>

<p>Ensure the GitHub token includes:</p>

<ul>
  <li>Contents:read</li>
  <li>Issues:write</li>
  <li>Pull requests:write</li>
  <li>Webhooks:write</li>
</ul>
