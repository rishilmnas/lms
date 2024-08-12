---


---

<h2 id="basic-syntax">Basic Syntax</h2>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Visit a webpage</span>
cy<span class="token punctuation">.</span><span class="token function">visit</span><span class="token punctuation">(</span><span class="token string">'https://example.com'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Get an element</span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'selector'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Click an element</span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'selector'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">click</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Type into an input</span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'input[name="username"]'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">type</span><span class="token punctuation">(</span><span class="token string">'your-username'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Assert element contains text</span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'selector'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">should</span><span class="token punctuation">(</span><span class="token string">'contain'</span><span class="token punctuation">,</span> <span class="token string">'expected text'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Wait for a request</span>
cy<span class="token punctuation">.</span><span class="token function">intercept</span><span class="token punctuation">(</span><span class="token string">'GET'</span><span class="token punctuation">,</span> <span class="token string">'/api/endpoint'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token keyword">as</span><span class="token punctuation">(</span><span class="token string">'apiRequest'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
cy<span class="token punctuation">.</span><span class="token function">wait</span><span class="token punctuation">(</span><span class="token string">'@apiRequest'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Chain commands</span>
cy<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">'selector'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">click</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">type</span><span class="token punctuation">(</span><span class="token string">'text'</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">should</span><span class="token punctuation">(</span><span class="token string">'have.value'</span><span class="token punctuation">,</span> <span class="token string">'text'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

</code></pre>
<h2 id="additional-resources">Additional Resources</h2>
<ul>
<li>
<p><a href="%5B%5Bhttps://docs.cypress.io%5D(https://docs.cypress.io/)%5D(%5Bhttps://docs.cypress.io/%5D(https://docs.cypress.io/))">Cypress Documentation</a></p>
</li>
<li>
<p><a href="%5B%5Bhttps://github.com/cypress-io/cypress%5D(https://github.com/cypress-io/cypress)%5D(%5Bhttps://github.com/cypress-io/cypress%5D(https://github.com/cypress-io/cypress))">Cypress GitHub Repository</a></p>
</li>
</ul>

