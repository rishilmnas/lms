---


---

<p><strong>Practice 1</strong></p>
<p><strong>Objective:</strong> Learn how to navigate to a webpage using Cypress.</p>
<p><strong>Steps:</strong></p>
<ol>
<li>
<p>Open your Cypress test file.</p>
</li>
<li>
<p>Use the <strong>cy.visit()</strong> command to navigate to a test webpage.</p>
</li>
<li>
<p>Verify that the page has loaded by asserting the page title or content.</p>
</li>
</ol>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token function">describe</span><span class="token punctuation">(</span><span class="token string">'Visit Webpage Practice'</span><span class="token punctuation">,</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
  <span class="token function">it</span><span class="token punctuation">(</span><span class="token string">'should visit the example webpage'</span><span class="token punctuation">,</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
    cy<span class="token punctuation">.</span><span class="token function">visit</span><span class="token punctuation">(</span><span class="token string">'https://example.com'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    cy<span class="token punctuation">.</span><span class="token function">title</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">should</span><span class="token punctuation">(</span><span class="token string">'include'</span><span class="token punctuation">,</span> <span class="token string">'Example Domain'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p><strong>Expected Outcome:</strong></p>
<ul>
<li>The test should open the specified website.</li>
</ul>
<p><strong>Practice 2</strong></p>
<p><strong>Objective:</strong> Write a basic test to open a YouTube video and check for specific elements.</p>
<p><strong>Steps:</strong></p>
<ol>
<li>
<p>Create a new test file in the <strong>cypress/e2e</strong> directory:</p>
<pre class=" language-javascript"><code class="prism  language-javascript">touch cypress<span class="token operator">/</span>e2e<span class="token operator">/</span>youtube<span class="token punctuation">.</span>spec<span class="token punctuation">.</span>js
</code></pre>
</li>
<li>
<p>Open <strong>youtube.spec.js</strong> in your code editor and add the following code:</p>
</li>
</ol>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token function">describe</span><span class="token punctuation">(</span><span class="token string">'YouTube Video Test'</span><span class="token punctuation">,</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> <span class="token function">it</span><span class="token punctuation">(</span><span class="token string">'should open a YouTube video and verify elements'</span><span class="token punctuation">,</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> 

<span class="token comment">// Visit a YouTube video page</span>
cy<span class="token punctuation">.</span><span class="token function">visit</span><span class="token punctuation">(</span><span class="token string">'https://www.youtube.com/watch?v=dQw4w9WgXcQ'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 

<span class="token comment">// Verify the page contains the video player </span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'video'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">should</span><span class="token punctuation">(</span><span class="token string">'be.visible'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 

<span class="token comment">// Verify the video title is present </span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'h1.title'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">should</span><span class="token punctuation">(</span><span class="token string">'be.visible'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 

<span class="token comment">// Verify the subscribe button is present </span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'ytd-subscribe-button-renderer'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">should</span><span class="token punctuation">(</span><span class="token string">'be.visible'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

</code></pre>
<ul>
<li>This script visits a specific YouTube video page and checks for the presence of the video player, the video title, and the subscribe button.</li>
</ul>
<p><strong>Hints:</strong></p>
<ul>
<li>Use  <code>cy.visit()</code>  to navigate to a URL.</li>
<li>Use  <code>cy.get()</code>  to select DOM elements and perform assertions on them.</li>
</ul>
<p><strong>Expected Outcome:</strong></p>
<ul>
<li>The test should open the specified YouTube video page, check for the video player’s presence, verify the video title, and ensure the subscribe button is visible.</li>
</ul>

