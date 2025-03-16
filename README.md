<h1><strong>Tom Kashefi's AI Code Review Action</strong> 🚀</h1>
<p><strong>AI-Driven GitHub Pull Request Reviewer Powered by Google Gemini AI</strong></p>
<h2><strong>🔹 What It Does</strong></h2>
<p>This GitHub Action leverages <strong>Google Gemini AI</strong> to automatically evaluate pull requests, delivering clear and practical feedback on your code updates.</p>
<ul>
<li>✅ <strong>Approves PRs</strong> when no critical problems are detected.</li>
<li>🔍 <strong>Spots bugs, security vulnerabilities, and performance concerns</strong>.</li>
<li>✨ <strong>Offers best practice tips</strong> (optional, non-blocking advice).</li>
<li>⏳ <strong>Keeps feedback objective</strong>, skipping subjective style opinions.</li>
</ul>
<hr>
<h2><strong>⚙️ How It Operates</strong></h2>
<ol>
<li>Upon <strong>opening a pull request</strong>, it retrieves the code changes.</li>
<li>The <strong>altered code</strong> is analyzed by <strong>Google Gemini AI</strong>.</li>
<li>The AI provides feedback rooted in software engineering standards.</li>
<li>A <strong>comment is added to the PR</strong> with the AI’s insights.</li>
</ol>
<hr>
<h2><strong>🛠 Getting Started</strong></h2>
<p>Add this workflow file to your GitHub repository to enable the action:</p>
<pre><code class="language-yaml">name: Tom Kashefi's AI Code Review
on: pull_request
jobs:
  ai_review:
    runs-on: ubuntu-latest
    steps:
      - name: Execute Tom Kashefi's AI Code Review
        uses: tom-kashefi/ai-code-review-action@v1
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          google_api_key: ${{ secrets.GOOGLE_API_KEY }}
</code></pre>
<h3><strong>🔑 Essential Inputs</strong></h3>

Name | Description | Required
-- | -- | --
github_token | GitHub Token for PR interaction | ✅ Yes
google_api_key | Google Gemini AI API Key | ✅ Yes

<blockquote>
<p>📌 <strong>Tip</strong>: Securely store these as <strong>GitHub Secrets</strong> in your repo settings.</p>
</blockquote>
<hr>
<h2><strong>📝 Sample PR Feedback</strong></h2>
<p>Here’s how Tom Kashefi’s AI Code Reviewer might comment on a PR:</p>
<pre><code>✅ Looks solid! No major concerns—ready to merge! 🚀
</code></pre>
<p>Or, if it finds issues:</p>
<pre><code>**File: `auth_service.dart`**
- **Problem:** Storing tokens in plaintext poses a security risk.
- **Reason:** Could leak sensitive data if breached.
- **Fix:** Encrypt tokens or use a secure storage solution.

**File: `performance_helper.dart`**
- **Problem:** Multiple loops over a large list.
- **Reason:** Hurts performance in bigger apps.
- **Fix:** Optimize with a single-pass approach.

---
🔍 *Address these for stronger security & efficiency!*
</code></pre>
<hr>
<h2><strong>💡 Why Choose This Action?</strong></h2>
<p>✅ <strong>Streamlines PR Reviews</strong> with AI-driven insights.<br>
🕒 <strong>Cuts Review Time</strong> by flagging key issues fast.<br>
📈 <strong>Boosts Code Quality</strong> with expert suggestions.<br>
🔒 <strong>Strengthens Security & Performance</strong> across your project.</p>
<hr>
<h2><strong>📌 Additional Info</strong></h2>
<ul>
<li>Needs a <strong>Google Gemini AI API key</strong> from <a href="https://aistudio.google.com/">Google AI Studio</a>.</li>
<li>Supports <strong>all coding languages</strong>.</li>
<li>Delivers <strong>brief, focused feedback</strong>.</li>
</ul>
<hr>