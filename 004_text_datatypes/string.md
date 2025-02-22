<!-- wp:paragraph -->
<p>The str class is an abbreviation for a string of Unicode characters. The str class is an immutable ordered Collection of Unicode characters. Immutable means once it has been instantiated it cannot be later modified.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="initialisation-signature">Initialisation Signature</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Inputting str() will display the docstring of the initialisation signature of the string class as a popup balloon. Some IDEs such as JupyterLab may require the keypress shift ⇧ and tab ↹ to invoke the docstring:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Init signature:  str(self, /, *args, **kwargs)
Docstring:     
str(object='') -> str
str(bytes_or_buffer[, encoding[, errors]]) -> str

Create a new string object from the given object. If encoding or
errors is specified, then the object must expose a data buffer
that will be decoded using the given encoding and error handler.
Otherwise, returns the result of object.__str__() (if defined)
or repr(object).
encoding defaults to sys.getdefaultencoding().
errors defaults to 'strict'.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Inputting:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"? str","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #B31D28; font-style: italic\u0022\u003e?\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="? str" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #B31D28; font-style: italic">?</span><span style="color: #24292E"> </span><span style="color: #005CC5">str</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Will output the docstring in the cell output of an interactive Python notebook or an ipython cell.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The purpose of the initialisation signature is to provide the data required to initialise a new instance. Under the hood the __new__ data model constructor will create a new instance and invoke the __init__ data model initialiser to initialise this instance with instance data.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The initialisation signature shows alternative ways of supplying instance data for a string. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The first way takes an already existing string instance self. The comma , is used as a delimiter to separate input arguments. In Python input arguments can be provided positionally or as named input arguments. Note when input arguments are placed before a / they will only be accepted as positional input arguments.</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">str(self, /, *args, **kwargs)</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>For example:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"str('hello')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="str('hello')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">str</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A string is typically instantiated directly using:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'hello'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'hello'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;hello&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice the difference in syntax highlighting between:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"hello","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ehello\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="hello" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">hello</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>And:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'hello'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'hello'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;hello&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The former is an object name, if this object name does not exist, Python will display a NameError:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>NameError: name 'hello' is not defined</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The latter is a string and the contents of a string are enclosed in single quotations ' '.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The second way uses a named keyword input argument object and assigns it to an empty string:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">str(object='') -> str</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>This named input argument can be explicitly assigned to a new value:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"str(object='hello')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003eobject\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="str(object='hello')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">str</span><span style="color: #24292E">(</span><span style="color: #E36209">object</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If the named input argument is not supplied, then object takes on its default value '' returning an empty string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"str()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="str()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">str</span><span style="color: #24292E">()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>''</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>An instance name can be conceptualised as a label, that is used to reference an instance. In Python objects with no instance name have no reference and are immediately removed by Pythons garbage collection. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If the instance instead is instantiated to an instance name or label greeting, the ipython cell displays no output:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = str(object='hello')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003eobject\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = str(object='hello')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">str</span><span style="color: #24292E">(</span><span style="color: #E36209">object</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code> </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><strong>Notice the subtlety in spacing which follows Pythons PEP8 styling convention</strong>. The assignment operator to the instance name is subtly emphasised using the spacing. The keyword argument within the function call have no spacing as spacing within a function call is instead typically used with the , separator to visually separate out input arguments from one another.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Using the object name in another ipython cell displays the formal representation of the string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Some IDEs such as Spyder have a Variable Explorer and the instance name and associated value will display alongside the instance class type and other properties such as the length of the string:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":56812,"sizeSlug":"full","linkDestination":"media"} -->
<figure class="wp-block-image size-full"><a href="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image.png"><img src="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image.png" alt="" class="wp-image-56812"/></a></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="identifiers">Identifiers</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Two instances can be created:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello'\nfarewell = 'bye'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;bye\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello'
farewell = 'bye'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello&#39;</span></span>
<span class="line"><span style="color: #24292E">farewell </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;bye&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Notice that there is no output on the ipython console and both of these display on the variable explorer:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":56816,"sizeSlug":"full","linkDestination":"media"} -->
<figure class="wp-block-image size-full"><a href="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image-1.png"><img src="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image-1.png" alt="" class="wp-image-56816"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>If the instance greeting is input followed by a dot . a list of identifiers will display. Some IDEs such as JupyterLab may require the keypress tab ↹ to invoke the list of identifiers:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>capitalize - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>casefold - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>center - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>count - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>encode - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>endswith - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>expandtabs - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>find - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format_map - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>index - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalnum - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalpha - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isascii - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isdecimal - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isdigit - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isidentifier - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>islower - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalnumeric - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isprintable - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isspace - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>istitle - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isupper - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>join - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ljust - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>lower - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>lstrip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>maketrans - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>partition - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>removeprefix - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>removesuffix - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>replace - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rfind - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rindex - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rjust - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rpartition - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rsplit - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rstrip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>split - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>splitlines - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>startswith - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>strip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>swapcase - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>title - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>translate - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>upper - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>zfill - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>If the instance farewell is input followed by a dot . a list of identifiers will display. Notice that these are the same list of identifiers:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"UAGDay":[]} -->
<ul><!-- wp:list-item -->
<li>capitalize - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>casefold -function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>center - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>count - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>encode - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>endswith - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>expandtabs - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>find - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format_map - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>index - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalnum - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalpha - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isascii - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isdecimal - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isdigit - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isidentifier - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>islower - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalnumeric - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isprintable - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isspace - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>istitle - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isupper - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>join - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ljust - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>lower - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>lstrip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>maketrans - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>partition - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>removeprefix - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>removesuffix - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>replace - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rfind - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rindex - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rjust - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rpartition - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rsplit - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rstrip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>split - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>splitlines - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>startswith - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>strip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>swapcase - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>title - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>translate - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>upper - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>zfill - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>This identifiers come from the string class. If str is input followed by a dot . an almost identical list of identifiers display:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"UAGDay":[]} -->
<ul><!-- wp:list-item -->
<li>capitalize - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>casefold -function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>center - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>count - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>encode - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>endswith - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>expandtabs - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>find - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format_map - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>index - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalnum - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalpha - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isascii - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isdecimal - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isdigit - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isidentifier - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>islower - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isalnumeric - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isprintable - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isspace - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>istitle - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isupper - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>join - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ljust - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>lower - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>lstrip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>maketrans - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>mro - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>partition - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>removeprefix - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>removesuffix - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>replace - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rfind - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rindex - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rjust - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rpartition - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rsplit - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>rstrip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>split - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>splitlines - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>startswith - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>strip - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>swapcase - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>title - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>translate - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>upper - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>zfill - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="data-model-identifiers">Data Model Identifiers</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>There is an addition called mro, which stands for method resolution order. If str.mro() is input the docstring should display: </p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  str.mro()
Docstring: Return a type's method resolution order.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Notice that there are no input arguments as the mro will return the method resolution order of the string class itself and therefore no additional information is required to call the function:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"str.mro()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e.mro()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="str.mro()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">str</span><span style="color: #24292E">.mro()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&#91;str, object]</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The method resolution order is a list which has two items, the str class itself and the object class. Python is an Object Orientated Programming (OOP) language and therefore everything is based on an object and the design pattern of an object. The object is an abstract class and isn't normally directly instantiated, its docstring can be examined by inputting object()</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Init signature:  object()
Docstring:     
The base class of the class hierarchy.

When called, it accepts no arguments and returns a new featureless
instance that has no instance attributes and cannot be given any.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The identifiers from object can be seen by inputting object followed by a dot .</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>mro - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>If object followed by a dot . and two underscores __ is input, additional hidden data model identifiers can be seen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>__annotations__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__base__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__bases__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__basicsize__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__call__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__class__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__delattr__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__dict__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__dict_offset__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__dir__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__doc__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__eq__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__flags__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__format__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getattribute__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__hash__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__init__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__init_subclass__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__instancecheck__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__itemsize__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__module__ statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__mro__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__name__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__ne__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__new__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__prepare__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__qualname__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__reduce__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__reduce_ex__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__repr__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__setattr__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__sizeof__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__slots__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__str__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__subclasscheck__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__subclasses__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__text_signature__ - statement</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__weakrefoffset__ - statement</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>If str followed by a dot . and two underscores __ is input, all the data model identifiers from the object class can be seen alongside the additional data model identifiers:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>__add__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__ge__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getitem__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getnewargs__- function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__ge__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getitem__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getnewargs__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__gt__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__iter__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__le__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__len__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__lt__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__mod__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__reversed__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__rmul__ - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>If the help function is used on the str and the object classes details about each identifier is given. The output splits the identifiers into four groups:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>methods - functions bound to an instance and designed to work on instance data.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>class methods - functions bound to a class. These are normally used as alternative constructors.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>static methods - functions in the classes namespace but not bound to an instance or class.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>data and other attributes</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>It is worthwhile browsing through the output given by help as it gives an overview of the identifiers used in the str and the object classes. Recall the method resolution order of the str class is [str, object] which means that the str class has all of the identifiers in the object class. Most of these identifiers are redefined in the str class, however some are not shown for example __reduce__. The identifiers not shown are copied over from the parent object class without modification and details about these identifiers, therefore should be read by examining the help of the object class.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If the help function is used on the str and the object classes details about each methods are given:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"help(str)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ehelp\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="help(str)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">help</span><span style="color: #24292E">(</span><span style="color: #005CC5">str</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Help on class str in module builtins:

class str(object)
 |  str(object='') -> str
 |  str(bytes_or_buffer&#91;, encoding&#91;, errors]]) -> str
 |  
 |  Create a new string object from the given object. If encoding or
 |  errors is specified, then the object must expose a data buffer
 |  that will be decoded using the given encoding and error handler.
 |  Otherwise, returns the result of object.__str__() (if defined)
 |  or repr(object).
 |  encoding defaults to sys.getdefaultencoding().
 |  errors defaults to 'strict'.
 |  
 |  Methods defined here:
 |  
 |  __add__(self, value, /)
 |      Return self+value.
 |  
 |  __contains__(self, key, /)
 |      Return key in self.
 |  
 |  __eq__(self, value, /)
 |      Return self==value.
 |  
 |  __format__(self, format_spec, /)
 |      Return a formatted version of the string as described by format_spec.
 |  
 |  __ge__(self, value, /)
 |      Return self>=value.
 |  
 |  __getattribute__(self, name, /)
 |      Return getattr(self, name).
 |  
 |  __getitem__(self, key, /)
 |      Return self&#91;key].
 |  
 |  __getnewargs__(...)
 |  
 |  __gt__(self, value, /)
 |      Return self>value.
 |  
 |  __hash__(self, /)
 |      Return hash(self).
 |  
 |  __iter__(self, /)
 |      Implement iter(self).
 |  
 |  __le__(self, value, /)
 |      Return self&lt;=value.
 |  
 |  __len__(self, /)
 |      Return len(self).
 |  
 |  __lt__(self, value, /)
 |      Return self&lt;value.
 |  
 |  __mod__(self, value, /)
 |      Return self%value.
 |  
 |  __mul__(self, value, /)
 |      Return self*value.
 |  
 |  __ne__(self, value, /)
 |      Return self!=value.
 |  
 |  __repr__(self, /)
 |      Return repr(self).
 |  
 |  __rmod__(self, value, /)
 |      Return value%self.
 |  
 |  __rmul__(self, value, /)
 |      Return value*self.
 |  
 |  __sizeof__(self, /)
 |      Return the size of the string in memory, in bytes.
 |  
 |  __str__(self, /)
 |      Return str(self).
 |  
 |  capitalize(self, /)
 |      Return a capitalized version of the string.
 |      
 |      More specifically, make the first character have upper case and the rest lower
 |      case.
 |  
 |  casefold(self, /)
 |      Return a version of the string suitable for caseless comparisons.
 |  
 |  center(self, width, fillchar=' ', /)
 |      Return a centered string of length width.
 |      
 |      Padding is done using the specified fill character (default is a space).
 |  
 |  count(...)
 |      S.count(sub&#91;, start&#91;, end]]) -> int
 |      
 |      Return the number of non-overlapping occurrences of substring sub in
 |      string S&#91;start:end].  Optional arguments start and end are
 |      interpreted as in slice notation.
 |  
 |  encode(self, /, encoding='utf-8', errors='strict')
 |      Encode the string using the codec registered for encoding.
 |      
 |      encoding
 |        The encoding in which to encode the string.
 |      errors
 |        The error handling scheme to use for encoding errors.
 |        The default is 'strict' meaning that encoding errors raise a
 |        UnicodeEncodeError.  Other possible values are 'ignore', 'replace' and
 |        'xmlcharrefreplace' as well as any other name registered with
 |        codecs.register_error that can handle UnicodeEncodeErrors.
 |  
 |  endswith(...)
 |      S.endswith(suffix&#91;, start&#91;, end]]) -> bool
 |      
 |      Return True if S ends with the specified suffix, False otherwise.
 |      With optional start, test S beginning at that position.
 |      With optional end, stop comparing S at that position.
 |      suffix can also be a tuple of strings to try.
 |  
 |  expandtabs(self, /, tabsize=8)
 |      Return a copy where all tab characters are expanded using spaces.
 |      
 |      If tabsize is not given, a tab size of 8 characters is assumed.
 |  
 |  find(...)
 |      S.find(sub&#91;, start&#91;, end]]) -> int
 |      
 |      Return the lowest index in S where substring sub is found,
 |      such that sub is contained within S&#91;start:end].  Optional
 |      arguments start and end are interpreted as in slice notation.
 |      
 |      Return -1 on failure.
 |  
 |  format(...)
 |      S.format(*args, **kwargs) -> str
 |      
 |      Return a formatted version of S, using substitutions from args and kwargs.
 |      The substitutions are identified by braces ('{' and '}').
 |  
 |  format_map(...)
 |      S.format_map(mapping) -> str
 |      
 |      Return a formatted version of S, using substitutions from mapping.
 |      The substitutions are identified by braces ('{' and '}').
 |  
 |  index(...)
 |      S.index(sub&#91;, start&#91;, end]]) -> int
 |      
 |      Return the lowest index in S where substring sub is found,
 |      such that sub is contained within S&#91;start:end].  Optional
 |      arguments start and end are interpreted as in slice notation.
 |      
 |      Raises ValueError when the substring is not found.
 |  
 |  isalnum(self, /)
 |      Return True if the string is an alpha-numeric string, False otherwise.
 |      
 |      A string is alpha-numeric if all characters in the string are alpha-numeric and
 |      there is at least one character in the string.
 |  
 |  isalpha(self, /)
 |      Return True if the string is an alphabetic string, False otherwise.
 |      
 |      A string is alphabetic if all characters in the string are alphabetic and there
 |      is at least one character in the string.
 |  
 |  isascii(self, /)
 |      Return True if all characters in the string are ASCII, False otherwise.
 |      
 |      ASCII characters have code points in the range U+0000-U+007F.
 |      Empty string is ASCII too.
 |  
 |  isdecimal(self, /)
 |      Return True if the string is a decimal string, False otherwise.
 |      
 |      A string is a decimal string if all characters in the string are decimal and
 |      there is at least one character in the string.
 |  
 |  isdigit(self, /)
 |      Return True if the string is a digit string, False otherwise.
 |      
 |      A string is a digit string if all characters in the string are digits and there
 |      is at least one character in the string.
 |  
 |  isidentifier(self, /)
 |      Return True if the string is a valid Python identifier, False otherwise.
 |      
 |      Call keyword.iskeyword(s) to test whether string s is a reserved identifier,
 |      such as "def" or "class".
 |  
 |  islower(self, /)
 |      Return True if the string is a lowercase string, False otherwise.
 |      
 |      A string is lowercase if all cased characters in the string are lowercase and
 |      there is at least one cased character in the string.
 |  
 |  isnumeric(self, /)
 |      Return True if the string is a numeric string, False otherwise.
 |      
 |      A string is numeric if all characters in the string are numeric and there is at
 |      least one character in the string.
 |  
 |  isprintable(self, /)
 |      Return True if the string is printable, False otherwise.
 |      
 |      A string is printable if all of its characters are considered printable in
 |      repr() or if it is empty.
 |  
 |  isspace(self, /)
 |      Return True if the string is a whitespace string, False otherwise.
 |      
 |      A string is whitespace if all characters in the string are whitespace and there
 |      is at least one character in the string.
 |  
 |  istitle(self, /)
 |      Return True if the string is a title-cased string, False otherwise.
 |      
 |      In a title-cased string, upper- and title-case characters may only
 |      follow uncased characters and lowercase characters only cased ones.
 |  
 |  isupper(self, /)
 |      Return True if the string is an uppercase string, False otherwise.
 |      
 |      A string is uppercase if all cased characters in the string are uppercase and
 |      there is at least one cased character in the string.
 |  
 |  join(self, iterable, /)
 |      Concatenate any number of strings.
 |      
 |      The string whose method is called is inserted in between each given string.
 |      The result is returned as a new string.
 |      
 |      Example: '.'.join(&#91;'ab', 'pq', 'rs']) -> 'ab.pq.rs'
 |  
 |  ljust(self, width, fillchar=' ', /)
 |      Return a left-justified string of length width.
 |      
 |      Padding is done using the specified fill character (default is a space).
 |  
 |  lower(self, /)
 |      Return a copy of the string converted to lowercase.
 |  
 |  lstrip(self, chars=None, /)
 |      Return a copy of the string with leading whitespace removed.
 |      
 |      If chars is given and not None, remove characters in chars instead.
 |  
 |  partition(self, sep, /)
 |      Partition the string into three parts using the given separator.
 |      
 |      This will search for the separator in the string.  If the separator is found,
 |      returns a 3-tuple containing the part before the separator, the separator
 |      itself, and the part after it.
 |      
 |      If the separator is not found, returns a 3-tuple containing the original string
 |      and two empty strings.
 |  
 |  removeprefix(self, prefix, /)
 |      Return a str with the given prefix string removed if present.
 |      
 |      If the string starts with the prefix string, return string&#91;len(prefix):].
 |      Otherwise, return a copy of the original string.
 |  
 |  removesuffix(self, suffix, /)
 |      Return a str with the given suffix string removed if present.
 |      
 |      If the string ends with the suffix string and that suffix is not empty,
 |      return string&#91;:-len(suffix)]. Otherwise, return a copy of the original
 |      string.
 |  
 |  replace(self, old, new, count=-1, /)
 |      Return a copy with all occurrences of substring old replaced by new.
 |      
 |        count
 |          Maximum number of occurrences to replace.
 |          -1 (the default value) means replace all occurrences.
 |      
 |      If the optional argument count is given, only the first count occurrences are
 |      replaced.
 |  
 |  rfind(...)
 |      S.rfind(sub&#91;, start&#91;, end]]) -> int
 |      
 |      Return the highest index in S where substring sub is found,
 |      such that sub is contained within S&#91;start:end].  Optional
 |      arguments start and end are interpreted as in slice notation.
 |      
 |      Return -1 on failure.
 |  
 |  rindex(...)
 |      S.rindex(sub&#91;, start&#91;, end]]) -> int
 |      
 |      Return the highest index in S where substring sub is found,
 |      such that sub is contained within S&#91;start:end].  Optional
 |      arguments start and end are interpreted as in slice notation.
 |      
 |      Raises ValueError when the substring is not found.
 |  
 |  rjust(self, width, fillchar=' ', /)
 |      Return a right-justified string of length width.
 |      
 |      Padding is done using the specified fill character (default is a space).
 |  
 |  rpartition(self, sep, /)
 |      Partition the string into three parts using the given separator.
 |      
 |      This will search for the separator in the string, starting at the end. If
 |      the separator is found, returns a 3-tuple containing the part before the
 |      separator, the separator itself, and the part after it.
 |      
 |      If the separator is not found, returns a 3-tuple containing two empty strings
 |      and the original string.
 |  
 |  rsplit(self, /, sep=None, maxsplit=-1)
 |      Return a list of the substrings in the string, using sep as the separator string.
 |      
 |        sep
 |          The separator used to split the string.
 |      
 |          When set to None (the default value), will split on any whitespace
 |          character (including \\n \\r \\t \\f and spaces) and will discard
 |          empty strings from the result.
 |        maxsplit
 |          Maximum number of splits (starting from the left).
 |          -1 (the default value) means no limit.
 |      
 |      Splitting starts at the end of the string and works to the front.
 |  
 |  rstrip(self, chars=None, /)
 |      Return a copy of the string with trailing whitespace removed.
 |      
 |      If chars is given and not None, remove characters in chars instead.
 |  
 |  split(self, /, sep=None, maxsplit=-1)
 |      Return a list of the substrings in the string, using sep as the separator string.
 |      
 |        sep
 |          The separator used to split the string.
 |      
 |          When set to None (the default value), will split on any whitespace
 |          character (including \\n \\r \\t \\f and spaces) and will discard
 |          empty strings from the result.
 |        maxsplit
 |          Maximum number of splits (starting from the left).
 |          -1 (the default value) means no limit.
 |      
 |      Note, str.split() is mainly useful for data that has been intentionally
 |      delimited.  With natural text that includes punctuation, consider using
 |      the regular expression module.
 |  
 |  splitlines(self, /, keepends=False)
 |      Return a list of the lines in the string, breaking at line boundaries.
 |      
 |      Line breaks are not included in the resulting list unless keepends is given and
 |      true.
 |  
 |  startswith(...)
 |      S.startswith(prefix&#91;, start&#91;, end]]) -> bool
 |      
 |      Return True if S starts with the specified prefix, False otherwise.
 |      With optional start, test S beginning at that position.
 |      With optional end, stop comparing S at that position.
 |      prefix can also be a tuple of strings to try.
 |  
 |  strip(self, chars=None, /)
 |      Return a copy of the string with leading and trailing whitespace removed.
 |      
 |      If chars is given and not None, remove characters in chars instead.
 |  
 |  swapcase(self, /)
 |      Convert uppercase characters to lowercase and lowercase characters to uppercase.
 |  
 |  title(self, /)
 |      Return a version of the string where each word is titlecased.
 |      
 |      More specifically, words start with uppercased characters and all remaining
 |      cased characters have lower case.
 |  
 |  translate(self, table, /)
 |      Replace each character in the string using the given translation table.
 |      
 |        table
 |          Translation table, which must be a mapping of Unicode ordinals to
 |          Unicode ordinals, strings, or None.
 |      
 |      The table must implement lookup/indexing via __getitem__, for instance a
 |      dictionary or list.  If this operation raises LookupError, the character is
 |      left untouched.  Characters mapped to None are deleted.
 |  
 |  upper(self, /)
 |      Return a copy of the string converted to uppercase.
 |  
 |  zfill(self, width, /)
 |      Pad a numeric string with zeros on the left, to fill a field of the given width.
 |      
 |      The string is never truncated.
 |  
 |  ----------------------------------------------------------------------
 |  Static methods defined here:
 |  
 |  __new__(*args, **kwargs) from builtins.type
 |      Create and return a new object.  See help(type) for accurate signature.
 |  
 |  maketrans(...)
 |      Return a translation table usable for str.translate().
 |      
 |      If there is only one argument, it must be a dictionary mapping Unicode
 |      ordinals (integers) or characters to Unicode ordinals, strings or None.
 |      Character keys will be then converted to ordinals.
 |      If there are two arguments, they must be strings of equal length, and
 |      in the resulting dictionary, each character in x will be mapped to the
 |      character at the same position in y. If there is a third argument, it
 |      must be a string, whose characters will be mapped to None in the result.</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"help(object)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ehelp\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eobject\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="help(object)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">help</span><span style="color: #24292E">(</span><span style="color: #005CC5">object</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Help on class object in module builtins:

class object
 |  The base class of the class hierarchy.
 |  
 |  When called, it accepts no arguments and returns a new featureless
 |  instance that has no instance attributes and cannot be given any.
 |  
 |  Built-in subclasses:
 |      anext_awaitable
 |      ArgNotFound
 |      async_generator
 |      async_generator_asend
 |      ... and 116 other subclasses
 |  
 |  Methods defined here:
 |  
 |  __delattr__(self, name, /)
 |      Implement delattr(self, name).
 |  
 |  __dir__(self, /)
 |      Default dir() implementation.
 |  
 |  __eq__(self, value, /)
 |      Return self==value.
 |  
 |  __format__(self, format_spec, /)
 |      Default object formatter.
 |  
 |  __ge__(self, value, /)
 |      Return self>=value.
 |  
 |  __getattribute__(self, name, /)
 |      Return getattr(self, name).
 |  
 |  __getstate__(self, /)
 |      Helper for pickle.
 |  
 |  __gt__(self, value, /)
 |      Return self>value.
 |  
 |  __hash__(self, /)
 |      Return hash(self).
 |  
 |  __init__(self, /, *args, **kwargs)
 |      Initialize self.  See help(type(self)) for accurate signature.
 |  
 |  __le__(self, value, /)
 |      Return self&lt;=value.
 |  
 |  __lt__(self, value, /)
 |      Return self&lt;value.
 |  
 |  __ne__(self, value, /)
 |      Return self!=value.
 |  
 |  __reduce__(self, /)
 |      Helper for pickle.
 |  
 |  __reduce_ex__(self, protocol, /)
 |      Helper for pickle.
 |  
 |  __repr__(self, /)
 |      Return repr(self).
 |  
 |  __setattr__(self, name, value, /)
 |      Implement setattr(self, name, value).
 |  
 |  __sizeof__(self, /)
 |      Size of object in memory, in bytes.
 |  
 |  __str__(self, /)
 |      Return str(self).
 |  
 |  ----------------------------------------------------------------------
 |  Class methods defined here:
 |  
 |  __init_subclass__(...) from builtins.type
 |      This method is called when a class is subclassed.
 |      
 |      The default implementation does nothing. It may be
 |      overridden to extend subclasses.
 |  
 |  __subclasshook__(...) from builtins.type
 |      Abstract classes can override this to customize issubclass().
 |      
 |      This is invoked early on by abc.ABCMeta.__subclasscheck__().
 |      It should return True, False or NotImplemented.  If it returns
 |      NotImplemented, the normal algorithm is used.  Otherwise, it
 |      overrides the normal algorithm (and the outcome is cached).
 |  
 |  ----------------------------------------------------------------------
 |  Static methods defined here:
 |  
 |  __new__(*args, **kwargs) from builtins.type
 |      Create and return a new object.  See help(type) for accurate signature.
 |  
 |  ----------------------------------------------------------------------
 |  Data and other attributes defined here:
 |  
 |  __class__ = &lt;class 'type'>
 |      type(object) -> the object's type
 |      type(name, bases, dict, **kwds) -> a new type</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Data model identifiers are hidden by default as they are not typically used directly. Instead a function or operator from the builtins module is typically used. builtins is automatically imported in a Python script or notebook. However it is sometimes useful to import it directly:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"import builtins","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eimport\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e builtins\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="import builtins" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">import</span><span style="color: #24292E"> builtins</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Once imported the list of identifiers in the builtins module can be accessed by using builtins followed by a dot . and there are a large number of identifiers. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The classes named using CamelCase correspond to error classes which a user encounters when an error is found:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>ArithmeticError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>AssertionError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>BaseException - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>BaseException - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>BlockingIOError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>BrokenPipeError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>BytesWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ChildProcessError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ConnectionAbortedError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ConnectionError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ConnectionRefusedError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ConnectionResetError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>DeprecationWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>EncodingWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>EnvironmentError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>EOFError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Exception - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ExceptionGroup - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>FileExistsError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>FileNotFoundError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>FloatingPointError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>FutureWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>GeneratorExit - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ImportError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ImportWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>IndentationError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>IndexError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>InterruptedError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>IOError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>IsADirectoryError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>KeyboardInterrupt - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>KeyError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>LookupError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>MemoryError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ModuleNotFoundError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>NameError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>NotADirectoryError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>NotImplementedError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>OSError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>OverflowError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>PendingDeprciationWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>PermissionError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>RecursionError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ReferenceError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ResourceWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>RuntimeError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>RuntimeWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>StopAsyncIteration - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>StopIteration - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>SyntaxError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>SystemError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>SystemExit - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>TabError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>TimeoutError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>TypeError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UnboundLocalError - clas</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UnicodeDecodeError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UnicodeEncodeError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UnicodeError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UnicodeTranslationError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UnicodeWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>UserWarning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ValueError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Warning - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>WindowsError - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ZeroDivisionError - class</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>The lower case classes are typically the classes a user instantiates on a regular basis:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>bool - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>bytearray - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>bytes - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>classmethod - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>complex - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>dict - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>enumerate - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>filter - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>float - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>frozenset - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>int - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>list - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>map - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>object - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>property - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>range - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>reversed - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>set - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>slice - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>staticmethod - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>str - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>super - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>tuple - classmethod</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>type - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>zip - class</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>The functions are setup to invoke the data model methods that belong to an instance, which recall are defined in the instances class:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>abs - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>aiter - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>all - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>anext - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>any - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ascii - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>bin - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>breakpoint - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>callable - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>chr - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>compile - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>delattr - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>dir - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>display - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>divmod - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>eval - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>exec - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>execfile - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>format - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>getattr - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>globals - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>hasattr - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>hash - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>hex - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>id - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>input - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>isinstance - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>issubclass - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>iter - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>len - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>locals - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>max - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>min - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>next - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>oct - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>open - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ord - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>pow - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>print - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>repr - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>round - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>runfile - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>setattr - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>sorted - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>sum - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>vars - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>The upper case instances are constants that are frequently used:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Ellipsis - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>False - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>None - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>NotImplemented - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>True - instance</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>The lower case instances are typically instances used by the Python interpretter:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>copyright - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>credits -instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>exit - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>help - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>license - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>quit - instance</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="calling-a-method">Calling a Method</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>A method is a function that is defined in an objects class. The docstring of the capitalize string method can be examined from the str class using str.capitalize()</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  str.capitalize(self, /)
Docstring:
Return a capitalized version of the string.

More specifically, make the first character have upper case and the rest lower
case.
Type:      method_descriptor</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Alternatively the docstring can be examined from the instance greeting using greeting.capitalize()</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.capitalize()
Docstring:
Return a capitalized version of the string.

More specifically, make the first character have upper case and the rest lower
case.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Notice the subtle differences between the two docstrings above, when called from a class, instance data from an instance <em>self</em> is required. On the other hand when called from an instance, the instance is already supplied, <em>self</em> is a placeholder for <em>an instance</em> in a class or <em>this instance</em> from an instance.</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  str.capitalize(self, /)
Signature:  greeting.capitalize()</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Notice also the slight difference in the type at the end of the docstring:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Type:      method_descriptor
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Methods which access instance data are known as instance methods as they are bound to the instance and instance data. Because these are the most commonly used methods, they are usually just referred to as methods. There are also class methods which are bound to the class and normally used for the purpose of alternative constructors. There are also static method which are rarer and neither bound to the class or instance but merely exist in the classes namespace for convenience. Finally there is data and other attributes, which are usually from an instance. Because data and other attributes are not functions they are accessed without parenthesis.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="case-identifiers">Case Identifiers</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>A str is immutable, which means once a string is instantiated that it cannot be modified. All the str methods therefore have a return value, returning a new str or an instance of another builtins class. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>A unitary identifier acts directly on the instance data. If the docstring of the method capitalize from the str class is compared to the docstring of the method capitalize from the instance greeting is compared:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  str.capitalize(self, /)
Docstring:
Return a capitalized version of the string.

More specifically, make the first character have upper case and the rest lower
case.
Type:      method_descriptor</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.capitalize()
Docstring:
Return a capitalized version of the string.

More specifically, make the first character have upper case and the rest lower
case.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Notice that the difference in the first line of the docstring, when calling the method from a class, an instance is required. When calling a method from an instance, the instance is already implied, in the second case <em>self</em> means <em>this instance</em> which has the instance name greeting:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  str.capitalize(self, /)
Signature:  greeting.capitalize()</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Using this method, returns a new string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.capitalize()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.capitalize()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.capitalize()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.capitalize()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'Hello'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Once again this instance is not assigned to an object name and will be collected by Pythons garbage collection. When the function call is assigned to an instance name, the return statement gets assigned to the instance name. For example:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting2 = greeting.capitalize()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting.capitalize()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting2 = greeting.capitalize()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> greeting.capitalize()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Once again because the instance is assigned to an instance name, it doesn't display in the ipython console. The assignment operator should be approached from right to the left; the operation on the right is carried out first and returns the str 'Hello'. Then this 'Hello' is assigned to the instance name greeting2.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Instead of assigning to a new instance name, the existing instance name can be reassigned.</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = greeting.capitalize()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting.capitalize()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = greeting.capitalize()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> greeting.capitalize()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Reassignment is often confused with mutation by beginners, recall that a str is immutable meaning that once it has been instantiated it cannot be modified. Like the above the assignment operator should be approached from right to the left; the operation on the right is carried out first on greeting which originally points to the str 'hello' and returns the new str instance 'Hello'. Then this new instance 'Hello' is assigned to the previous instance name greeting. greeting now points to the new str instance 'Hello' and no longer points to the old instance 'hello'. Conceptualise the instance name as a label placed on an instance and reassignment removes this label from the instance and places it on a new instance. If the old instance 'hello' has no other instance names, it has no references pointing to it meaning it is orphaned and collected by Pythons garbage collection.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are a number of other identifiers such as:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>lower</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>title</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>casefold</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>swapcase</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>which all operate on the instance data:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.lower()
Docstring: Return a copy of the string converted to lowercase.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.upper()
Docstring: Return a copy of the string converted to uppercase.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.title()
Docstring:
Return a version of the string where each word is titlecased.

More specifically, words start with uppercased characters and all remaining
cased characters have lower case.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.casefold()
Docstring: Return a version of the string suitable for caseless comparisons.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.swapcase()
Docstring: Convert uppercase characters to lowercase and lowercase characters to uppercase.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>These can all be used on the str instance greeting:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting\ngreeting.upper()\ngreeting.lower()\ngreeting.title()\ngreeting.casefold()\ngreeting.swapcase()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.upper()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.lower()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.title()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.casefold()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.swapcase()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting
greeting.upper()
greeting.lower()
greeting.title()
greeting.casefold()
greeting.swapcase()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting</span></span>
<span class="line"><span style="color: #24292E">greeting.upper()</span></span>
<span class="line"><span style="color: #24292E">greeting.lower()</span></span>
<span class="line"><span style="color: #24292E">greeting.title()</span></span>
<span class="line"><span style="color: #24292E">greeting.casefold()</span></span>
<span class="line"><span style="color: #24292E">greeting.swapcase()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'Hello' # capitalized
'HELLO' # uppercase
'hello' # lowercase
'Hello' # titlecase
'hello' # lowercase (including non-English characters)
'hELLO' # swapcase</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>These can also be used with the str instance farewell:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"farewell\nfarewell.capitalize()\nfarewell.upper()\nfarewell.lower()\nfarewell.title()\nfarewell.casefold()\nfarewell.swapcase()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell.capitalize()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell.upper()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell.lower()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell.title()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell.casefold()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efarewell.swapcase()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="farewell
farewell.capitalize()
farewell.upper()
farewell.lower()
farewell.title()
farewell.casefold()
farewell.swapcase()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">farewell</span></span>
<span class="line"><span style="color: #24292E">farewell.capitalize()</span></span>
<span class="line"><span style="color: #24292E">farewell.upper()</span></span>
<span class="line"><span style="color: #24292E">farewell.lower()</span></span>
<span class="line"><span style="color: #24292E">farewell.title()</span></span>
<span class="line"><span style="color: #24292E">farewell.casefold()</span></span>
<span class="line"><span style="color: #24292E">farewell.swapcase()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:enlighter/codeblock {"linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="generic" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">'bye' # capitalized
'Bye' # uppercase
'BYE' # lowercase
'bye' # titlecase
'Bye' # lowercase (including non-English characters) 
'bye' # swapcase</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The following methods check the properties of a str instance returning a bool:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isupper()
Docstring:
Return True if the string is an uppercase string, False otherwise.

A string is uppercase if all cased characters in the string are uppercase and
there is at least one cased character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.islower()
Docstring:
Return True if the string is a lowercase string, False otherwise.

A string is lowercase if all cased characters in the string are lowercase and
there is at least one cased character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.istitle()
Docstring:
Return True if the string is a title-cased string, False otherwise.

In a title-cased string, upper- and title-case characters may only
follow uncased characters and lowercase characters only cased ones.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>These can be used on the instance greeting:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.isupper()\ngreeting.islower()\ngreeting.istitle()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isupper()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.islower()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.istitle()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.isupper()
greeting.islower()
greeting.istitle()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.isupper()</span></span>
<span class="line"><span style="color: #24292E">greeting.islower()</span></span>
<span class="line"><span style="color: #24292E">greeting.istitle()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>False # is upper
False # is lower
True # is title</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="string-properties">Valid Identifier Names</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The isidentifier method can be used to check whether a str instance has the properties to be used as an identifier. For example:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"id1 = 'islower'\nid2 = 'is lower'\nid3 = 'is_lower'\nid4 = 'is_lower2'\nid5 = '2is_lower'\nid6 = 'is-lower'\nid7 = 'IS_UPPER'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;islower\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;is lower\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid3 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;is_lower\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid4 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;is_lower2\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid5 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;2is_lower\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid6 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;is-lower\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid7 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;IS_UPPER\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="id1 = 'islower'
id2 = 'is lower'
id3 = 'is_lower'
id4 = 'is_lower2'
id5 = '2is_lower'
id6 = 'is-lower'
id7 = 'IS_UPPER'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">id1 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;islower&#39;</span></span>
<span class="line"><span style="color: #24292E">id2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;is lower&#39;</span></span>
<span class="line"><span style="color: #24292E">id3 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;is_lower&#39;</span></span>
<span class="line"><span style="color: #24292E">id4 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;is_lower2&#39;</span></span>
<span class="line"><span style="color: #24292E">id5 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;2is_lower&#39;</span></span>
<span class="line"><span style="color: #24292E">id6 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;is-lower&#39;</span></span>
<span class="line"><span style="color: #24292E">id7 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;IS_UPPER&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"id1.isidentifier()\nid2.isidentifier()\nid3.isidentifier()\nid4.isidentifier()\nid5.isidentifier()\nid6.isidentifier()\nid7.isidentifier()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid1.isidentifier()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid2.isidentifier()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid3.isidentifier()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid4.isidentifier()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid5.isidentifier()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid6.isidentifier()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eid7.isidentifier()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="id1.isidentifier()
id2.isidentifier()
id3.isidentifier()
id4.isidentifier()
id5.isidentifier()
id6.isidentifier()
id7.isidentifier()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">id1.isidentifier()</span></span>
<span class="line"><span style="color: #24292E">id2.isidentifier()</span></span>
<span class="line"><span style="color: #24292E">id3.isidentifier()</span></span>
<span class="line"><span style="color: #24292E">id4.isidentifier()</span></span>
<span class="line"><span style="color: #24292E">id5.isidentifier()</span></span>
<span class="line"><span style="color: #24292E">id6.isidentifier()</span></span>
<span class="line"><span style="color: #24292E">id7.isidentifier()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True # all lower case characters are valid
False # a space is an invalid character
True # an underscore is a valid character
True # a number is a valid character
False # an identifier cannot start with a number
False # the - operator is an invalid character
True # all upper case characters are valid</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Recall an identifier is a class, function or instance. In Python it is typical to use lower case instance names. Upper case instance names are reserved for a constant instance, that is an immutable instance that should never be reassigned.  Python doesn't prevent reassignment of a constant, merely the upper case instance name indicates to another programmer than an instance is designed to be a constant.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>An instance name shouldn't match any of the identifiers in builtins otherwise it will override the builtin (until the kernel is restarted) which will lead to confusion when the builtin is attempted to be used.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In addition to builtins, Python has a number of keywords. The keyword module gives details about these keywords:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"import keyword","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eimport\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e keyword\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="import keyword" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">import</span><span style="color: #24292E"> keyword</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The keyword module has four identifiers:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>iskeyword - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>issoftkeyword - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>kwlist - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>softkwlist - instance</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>The identifiers kwlist and softkwlist are a list of strings:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"keyword.kwlist\nkeyword.softkwlist","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ekeyword.kwlist\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ekeyword.softkwlist\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="keyword.kwlist
keyword.softkwlist" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">keyword.kwlist</span></span>
<span class="line"><span style="color: #24292E">keyword.softkwlist</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&#91;'False',
 'None',
 'True',
 'and',
 'as',
 'assert',
 'async',
 'await',
 'break',
 'class',
 'continue',
 'def',
 'del',
 'elif',
 'else',
 'except',
 'finally',
 'for',
 'from',
 'global',
 'if',
 'import',
 'in',
 'is',
 'lambda',
 'nonlocal',
 'not',
 'or',
 'pass',
 'raise',
 'return',
 'try',
 'while',
 'with',
 'yield']

&#91;'_', 'case', 'match']</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>None of these should be used as identifier names.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Python has a&nbsp;<code>string</code>&nbsp;module which contains a number of useful strings.</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"import string","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eimport\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e string\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="import string" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">import</span><span style="color: #24292E"> string</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The string module has the following identifiers:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>ascii_letters - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ascii_lowercase - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>ascii_uppercase - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>capwords - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>digits - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Formatter - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>hexdigits - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>octdigits - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>printable - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>punctuation - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Template - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>whitespace - instance</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="ascii">ASCII</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The first computers originated from a typewriter:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":56894,"sizeSlug":"large","linkDestination":"media"} -->
<figure class="wp-block-image size-large"><a href="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/img_224.jpg"><img src="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/img_224-1024x894.jpg" alt="" class="wp-image-56894"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The American Standard Code for Information Interchange (ASCII) is as the name suggests based on an American typewriter which uses the English language. The typewriter has the letters and numbers but also has a number of whitespace commands such as the tab and the space. Physically to create a new line on a typewriter, the carriage has to return to the start of the page and the form feed has to be used to move the piece of paper up by the thickness of a line. ASCII has 128 commands, the first 32 are non-printable commands and the rest print English characters:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true,"start":0} -->
<ol start="0"><!-- wp:list-item -->
<li>null</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>start of heading</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>start of text</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>end of text</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>end of transmission</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>enquiry</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>acknowledge</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>bell</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>backspace</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>horizontal tab</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>new line</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>vertical tab</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>form feed</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>carriage return</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>shift out</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>shift in</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>data link escape</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>device control 1</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>device control 2</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>device control 3</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>device control 4</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>negative acknowledge</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>synchronous idle</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>end of transmission block</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>cancel</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>end of medium</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>substitute</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>escape</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>file separator</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>group separator</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>record separator</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>unit seperator</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>space</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>!</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>"</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>#</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>$</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>%</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>&amp;</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>'</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>(</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>)</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>*</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>+</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>,</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>-</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>/</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>0</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>1</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>2</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>3</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>4</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>5</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>6</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>7</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>8</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>9</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>:</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>;</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>&lt;</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>=</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>&gt;</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>?</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>@</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>A</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>B</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>C</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>D</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>E</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>F</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>G</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>H</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>I</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>J</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>K</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>L</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>M</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>N</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>O</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>P</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Q</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>R</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>S</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>T</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>U</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>V</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>W</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>X</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Y</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Z</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>[</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>]</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>^</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>_</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>`</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>a</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>b</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>c</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>d</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>e</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>f</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>g</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>h</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>i</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>j</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>k</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>l</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>m</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>n</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>o</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>p</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>q</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>r</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>s</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>t</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>u</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>v</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>w</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>x</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>y</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>z</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>{</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>|</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>}</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>~</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>delete</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>The string module groups the ascii, digits, punctuation and whitespace characters. ascii_letters gives the letters in the English alphabet:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.ascii_letters","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.ascii_letters\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.ascii_letters" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.ascii_letters</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>These are split into ascii_lowercase and ascii_uppercase:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.ascii_lowercase","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.ascii_lowercase\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.ascii_lowercase" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.ascii_lowercase</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'abcdefghijklmnopqrstuvwxyz'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.ascii_uppercase","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.ascii_uppercase\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.ascii_uppercase" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.ascii_uppercase</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'ABCDEFGHIJKLMNOPQRSTUVWXYZ'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>digits give the 10 digits used in the decimal numbering system:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.digits","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.digits\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.digits" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.digits</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0123456789'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>punctuation gives the characters used for punctuation:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.punctuation","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.punctuation\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.punctuation" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.punctuation</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'!"#$%&amp;\'()*+,-./:;&lt;=&gt;?@&#91;\\]^_`{|}~'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice that the \\ displays twice, \ is a special character in Python which means insert an escape character. If \ is followed by \, it means the escape character to insert is the \ itself.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>whitespace gives the representation used for whitespace. As whitespace characters cannot be seen, these normally use escape sequences:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.whitespace","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.whitespace\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.whitespace" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.whitespace</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>' \t\n\r\x0b\x0c'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>This is the space ' ', the tab '\t', the new line '\n', the carriage return '\r', the vertical tab '\x0b' and form feed '\x0c' respectively. The whitespace characters most commonly used '\t', '\n' and to a slightly lesser extent '\r' all have a 1 letter escape character. The less commonly used whitespace characters use a 2 letter hexadecimal number which corresponds to their byte sequence which will be discussed in another tutorial.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The hexdigits give the 16 characters used for hexadecimal numbers. Essentially after 0:10, the first 6 characters in the alphabet are used. These can either be lower or upper case, but typically lower case is the default:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.hexdigits","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.hexdigits\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.hexdigits" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.hexdigits</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">'0123456789abcdefABCDEF'</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>'\x0b' is the 11th value and '\x0c' is the 12th value as seen in the numeric list of the ascii characters above.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There is also the printable characters which group all of the above and are the typical characters used in a string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"string.printable","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estring.printable\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="string.printable" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">string.printable</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!"#$%&amp;\'()*+,-./:;&lt;=&gt;?@&#91;\\]^_`{|}~ \t\n\r\x0b\x0c'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Now that there is a basic understanding of ascii and the ascii subgroupings the other identifiers that are used to check if every character in a string belongs to such groupings can be examined:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isalnum()
Docstring:
Return True if the string is an alpha-numeric string, False otherwise.

A string is alpha-numeric if all characters in the string are alpha-numeric and
there is at least one character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isalpha()
Docstring:
Return True if the string is an alphabetic string, False otherwise.

A string is alphabetic if all characters in the string are alphabetic and there
is at least one character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isascii()
Docstring:
Return True if all characters in the string are ASCII, False otherwise.

ASCII characters have code points in the range U+0000-U+007F.
Empty string is ASCII too.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isdecimal()
Docstring:
Return True if the string is a decimal string, False otherwise.

A string is a decimal string if all characters in the string are decimal and
there is at least one character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isdigit()
Docstring:
Return True if the string is a digit string, False otherwise.

A string is a digit string if all characters in the string are digits and there
is at least one character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.isspace()
Docstring:
Return True if the string is a whitespace string, False otherwise.

A string is whitespace if all characters in the string are whitespace and there
is at least one character in the string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello world!'\ngreeting.isalnum()\ngreeting.isalpha()\ngreeting.isascii()\ngreeting.isdecimal()\ngreeting.isdigit()\ngreeting.isnumeric()\ngreeting.isprintable()\ngreeting.isspace()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isalnum()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isalpha()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isascii()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isdecimal()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isdigit()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isnumeric()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isprintable()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isspace()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello world!'
greeting.isalnum()
greeting.isalpha()
greeting.isascii()
greeting.isdecimal()
greeting.isdigit()
greeting.isnumeric()
greeting.isprintable()
greeting.isspace()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span>
<span class="line"><span style="color: #24292E">greeting.isalnum()</span></span>
<span class="line"><span style="color: #24292E">greeting.isalpha()</span></span>
<span class="line"><span style="color: #24292E">greeting.isascii()</span></span>
<span class="line"><span style="color: #24292E">greeting.isdecimal()</span></span>
<span class="line"><span style="color: #24292E">greeting.isdigit()</span></span>
<span class="line"><span style="color: #24292E">greeting.isnumeric()</span></span>
<span class="line"><span style="color: #24292E">greeting.isprintable()</span></span>
<span class="line"><span style="color: #24292E">greeting.isspace()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello world!'
False # '!' and ' ' are not alphanumerical
False # '!' and ' ' are not alphabetical
True # All characters are ASCII
False # None of the characters are decimal
False # None of the characters are digits
False # None of the characters are numeric
True # All of the characters are printable
False # Only the ' ' is a space</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A string is a sequence of Unicode characters and can include ASCII and non-ASCII digits:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'Hello World!'\ngreeting.isascii()\ngreek_greeting = 'Γειά σου Κόσμε!'\ngreek_greeting.isascii()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Hello World!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.isascii()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreek_greeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Γειά σου Κόσμε!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreek_greeting.isascii()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'Hello World!'
greeting.isascii()
greek_greeting = 'Γειά σου Κόσμε!'
greek_greeting.isascii()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Hello World!&#39;</span></span>
<span class="line"><span style="color: #24292E">greeting.isascii()</span></span>
<span class="line"><span style="color: #24292E">greek_greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Γειά σου Κόσμε!&#39;</span></span>
<span class="line"><span style="color: #24292E">greek_greeting.isascii()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True # All English characters except the '£' are ASCII
False # Greek characters are not ASCII</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The methods isdecimal, isdigit and isnumeric closely resemble one another when it comes to ASCII characters. They handle non-ASCII numeric characters slightly differently.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>isdecimal is the most restrictive and only includes the numbers '0123456789'. These can be different Unicode characters for example '𝟶𝟷𝟸𝟹𝟺𝟻𝟼𝟽𝟾𝟿', '𝟬𝟭𝟮𝟯𝟰𝟱𝟲𝟳𝟴𝟵' and '𝟘𝟙𝟚𝟛𝟜𝟝𝟞𝟟𝟠𝟡' which are the same characters with a different font.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>isdigit and isnumeric also include different Unicode characters that represent subscript '₀₁₂₃₄₅₆₇₈₉' and superscript '⁰¹²³⁴⁵⁶⁷⁸⁹', as well as circled digits '➀➁➂➃➄➅➆➇➈'.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>isnumeric includes Vulgar Fractions '½⅓¼⅕⅙⅐⅛⅑⅒⅔¾⅖⅗⅘⅚⅜⅝⅞⅟↉' and numeric Unicode characters that represent digits outwith '➀➁➂➃➄➅➆➇➈' such as '➉'.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="escape-characters">Escape Characters</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The \ is a special symbol used to insert an escape character. Th most commonly used escape characters have the form:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>\\ - insert a \</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\t - insert a tab</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\n - insert a new line</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\xff - insert an ASCII character as a 2 digit hexadecimal</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\uffff - insert a Unicode character as a 4 digit hexadecimal</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\' - insert a quotation</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>\" - inset a double quotation</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>A file path in Windows uses the \ as a directory delimiter. For example:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"file_path = 'C:\\\\Users\\\\Philip'\nfile_path","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efile_path \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;C:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eUsers\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ePhilip\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efile_path\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="file_path = 'C:\\Users\\Philip'
file_path" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">file_path </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;C:</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Users</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Philip&#39;</span></span>
<span class="line"><span style="color: #24292E">file_path</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'C:\\Users\\Philip'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice that the ipython cell output displays the representation of the string, i.e. the sequence of characters needed to instantiate the string.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The print function is used to print the string and all the escape characters are converted into their printable equivalents. The docstring of the print function can be examined:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Signature:  print(*args, sep=' ', end='\n', file=None, flush=False)
Docstring:
Prints the values to a stream, or to sys.stdout by default.

sep
  string inserted between values, default a space.
end
  string appended after the last value, default a newline.
file
  a file-like object (stream); defaults to the current sys.stdout.
flush
  whether to forcibly flush the stream.
Type:      builtin_function_or_method</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice that the first input argument is *args, this means a variable number of positional input arguments can be supplied to be printed. The two keywords sep and end have a default value of a space and a new line respectively. Leaving these at their defaults and printing the file_path gives:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"print(file_path)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="print(file_path)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>C:\Users\Philip</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The influence of the default values of the keyword arguments sep and end can be seen with the following:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"print(file_path, file_path, file_path)\nprint(file_path, file_path)\nprint(file_path)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path, file_path, file_path)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path, file_path)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="print(file_path, file_path, file_path)
print(file_path, file_path)
print(file_path)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path, file_path, file_path)</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path, file_path)</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>C:\Users\Philip C:\Users\Philip C:\Users\Philip
C:\Users\Philip C:\Users\Philip
C:\Users\Philip</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The behaviour of overriding these defaults can be seen with:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"print(file_path, file_path, file_path)\nprint(file_path, file_path, file_path, sep='')\nprint(file_path, file_path, file_path, sep='\\t')\nprint(file_path, file_path, end='')\nprint(file_path)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path, file_path, file_path)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path, file_path, file_path, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003esep\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path, file_path, file_path, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003esep\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\t\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path, file_path, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003eend\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="print(file_path, file_path, file_path)
print(file_path, file_path, file_path, sep='')
print(file_path, file_path, file_path, sep='\t')
print(file_path, file_path, end='')
print(file_path)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path, file_path, file_path)</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path, file_path, file_path, </span><span style="color: #E36209">sep</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path, file_path, file_path, </span><span style="color: #E36209">sep</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;</span><span style="color: #005CC5">\t</span><span style="color: #032F62">&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path, file_path, </span><span style="color: #E36209">end</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(file_path)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>C:\Users\Philip C:\Users\Philip C:\Users\Philip
C:\Users\PhilipC:\Users\PhilipC:\Users\Philip
C:\Users\Philip	C:\Users\Philip	C:\Users\Philip
C:\Users\Philip C:\Users\PhilipC:\Users\Philip</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>In Python everything is based on an object and an object has the data model identifiers __repr__ and __str__ which give the formal and informal str representation respectively:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       object.__repr__(self, /)
Call signature:  object.__repr__(*args, **kwargs)
Type:           wrapper_descriptor
String form:    &lt;slot wrapper '__repr__' of 'object' objects>
Namespace:      Python builtin
Docstring:      Return repr(self).</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       object.__str__(self, /)
Call signature:  object.__str__(*args, **kwargs)
Type:           wrapper_descriptor
String form:    &lt;slot wrapper '__str__' of 'object' objects>
Namespace:      Python builtin
Docstring:      Return str(self).</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>These data model identifiers are not typically used directly, and instead map to the repr function and str class in builtins:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  repr(obj, /)
Docstring:
Return the canonical string representation of the object.

For many object types, including most builtins, eval(repr(obj)) == obj.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Init signature:  str(self, /, *args, **kwargs)
Docstring:     
str(object='') -> str
str(bytes_or_buffer[, encoding[, errors]]) -> str

Create a new string object from the given object. If encoding or
errors is specified, then the object must expose a data buffer
that will be decoded using the given encoding and error handler.
Otherwise, returns the result of object.__str__() (if defined)
or repr(object).
encoding defaults to sys.getdefaultencoding().
errors defaults to 'strict'.
Type:           type
Subclasses:     StrEnum, DeferredConfigString, _rstr, _ScriptTarget, _ModuleTarget, LSString, include, Keys, InputMode, ColorDepth, ...</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>For many objects the formal (repr) and informal string (str) representation are identical however for the str class the subtle difference can be seen. The informal representation casts the string to another string instance leaving it unchanged as expected:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"file_path = 'C:\\\\Users\\\\Philip'\nstr(file_path)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efile_path \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;C:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eUsers\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ePhilip\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003estr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="file_path = 'C:\\Users\\Philip'
str(file_path)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">file_path </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;C:</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Users</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Philip&#39;</span></span>
<span class="line"><span style="color: #005CC5">str</span><span style="color: #24292E">(file_path)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'C:\\Users\\Philip'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The formal representation will instead sequence each \ and prepend a \ to it and enclose the str literal in double quotations:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"file_path = 'C:\\\\Users\\\\Philip'\nrepr(file_path)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efile_path \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;C:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eUsers\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ePhilip\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003erepr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="file_path = 'C:\\Users\\Philip'
repr(file_path)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">file_path </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;C:</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Users</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Philip&#39;</span></span>
<span class="line"><span style="color: #005CC5">repr</span><span style="color: #24292E">(file_path)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>"'C:\\\\Users\\\\Philip'"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The purpose of this is to create a string that displays the original string when printed:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"file_path = 'C:\\\\Users\\\\Philip'\nprint(repr(file_path))","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efile_path \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;C:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eUsers\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ePhilip\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003erepr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(file_path))\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="file_path = 'C:\\Users\\Philip'
print(repr(file_path))" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">file_path </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;C:</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Users</span><span style="color: #005CC5">\\</span><span style="color: #032F62">Philip&#39;</span></span>
<span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(</span><span style="color: #005CC5">repr</span><span style="color: #24292E">(file_path))</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'C:\\Users\\Philip'</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="single-vs-double-quotations">Single vs Double quotations</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Notice the syntax highlighting below.</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'The string greeting = 'hello world!''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string greeting = \u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ehello world!\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'The string greeting = 'hello world!''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;The string greeting = &#39;</span><span style="color: #24292E">hello world!</span><span style="color: #032F62">&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The quotations within the string literal terminate the string. This gives the string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'The string greeting = '","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string greeting = \u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'The string greeting = '" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;The string greeting = &#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The instance name:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"hello","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ehello\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="hello" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">hello</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>which is not defined. The instance name:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"world!","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eworld!\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="world!" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">world!</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>which is also not defined and is an invalid identifier name and finally an empty string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>To insert the string literal into the string, the quotations can be used to insert escape characters. Notice the syntax highlighting now shows that this is a single string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'The string greeting = \\'hello world!\\''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string greeting = \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ehello world!\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'The string greeting = \'hello world!\''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;The string greeting = </span><span style="color: #005CC5">\&#39;</span><span style="color: #032F62">hello world!</span><span style="color: #005CC5">\&#39;</span><span style="color: #032F62">&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>"The string greeting = 'hello world!'"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice the cell output displays the string which includes the string literal in double quotations which is easier to read. Compare this with the printed string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"print('The string greeting = \\'hello world!\\'')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string greeting = \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ehello world!\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="print('The string greeting = \'hello world!\'')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;The string greeting = </span><span style="color: #005CC5">\&#39;</span><span style="color: #032F62">hello world!</span><span style="color: #005CC5">\&#39;</span><span style="color: #032F62">&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>The string greeting = 'hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>In Python both single quotes and double quotes can be used to enclose a string. The Python language by default prefers single quotes but uses double quotes to conveniently enclose a string literal.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Each ASCII character corresponds to an ordinal value, the function ord can be used to retrieve the ordinal value of an ASCII character:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  ord(c, /)
Docstring: Return the Unicode code point for a one-character string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"ord('a')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;a\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="ord('a')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">ord</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;a&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>97</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The function chr does the inverse, retrieving the character from the ordinal value:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  chr(i, /)
Docstring: Return a Unicode string of one character with ordinal i; 0 &lt;= i &lt;= 0x10ffff.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"chr(97)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003echr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e97\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="chr(97)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">chr</span><span style="color: #24292E">(</span><span style="color: #005CC5">97</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'a'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice that the character returned is enclosed in single quotations, the default for the Python language.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Unfortunately there is some confusion within the Python community between the use of single and double quotations in strings. Most of the data science community for example favour the use of double quotations over single quotations because the author of the popular pandas library uses double quotations by default. The Python language itself, numpy and matplotlib libraries prefer the use of single quotations.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="multiline-string">Multiline string</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Three single quotes will begin a multiline string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph = '''The quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog'''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph = '''The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog'''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">paragraph </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;&#39;&#39;The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog&#39;&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:block {"ref":56840} /-->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice the difference between the above and:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph = '''\n            The quick brown fox jumps over the lazy dog\n            The quick brown fox jumps over the lazy dog\n            The quick brown fox jumps over the lazy dog\n            The quick brown fox jumps over the lazy dog\n            '''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e            The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e            The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e            The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e            The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e            \u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph = '''
            The quick brown fox jumps over the lazy dog
            The quick brown fox jumps over the lazy dog
            The quick brown fox jumps over the lazy dog
            The quick brown fox jumps over the lazy dog
            '''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">paragraph </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;&#39;&#39;</span></span>
<span class="line"><span style="color: #032F62">            The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">            The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">            The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">            The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">            &#39;&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">paragraph</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'\n            The quick brown fox jumps over the lazy dog\n            The quick brown fox jumps over the lazy dog\n            The quick brown fox jumps over the lazy dog\n            The quick brown fox jumps over the lazy dog\n            '</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The above style syntax can be used to enclose Python collections for the purpose of making them more readable. For such collections the additional spacing and new line characters are ignored however for a multiline string these changes are incorporated into the string. Returning to:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph = '''The quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog'''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph = '''The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog'''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">paragraph </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;&#39;&#39;The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog&#39;&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Printing the above gives:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"The quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #24292E">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #24292E">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #24292E">The quick brown fox jumps over the lazy dog</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The most widely used purpose for a multiline string is a Python docstring. For example let's examine the print functions docstring again:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  print(*args, sep=' ', end='\n', file=None, flush=False)
Docstring:
Prints the values to a stream, or to sys.stdout by default.

sep
  string inserted between values, default a space.
end
  string appended after the last value, default a newline.
file
  a file-like object (stream); defaults to the current sys.stdout.
flush
  whether to forcibly flush the stream.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The docstring component is:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"printdocstring = '''Prints the values to a stream, or to sys.stdout by default.\n\nsep\n  string inserted between values, default a space.\nend\n  string appended after the last value, default a newline.\nfile\n  a file-like object (stream); defaults to the current sys.stdout.\nflush\n  whether to forcibly flush the stream.'''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eprintdocstring \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;Prints the values to a stream, or to sys.stdout by default.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003esep\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  string inserted between values, default a space.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eend\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  string appended after the last value, default a newline.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003efile\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  a file-like object (stream); defaults to the current sys.stdout.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eflush\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  whether to forcibly flush the stream.\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="printdocstring = '''Prints the values to a stream, or to sys.stdout by default.

sep
  string inserted between values, default a space.
end
  string appended after the last value, default a newline.
file
  a file-like object (stream); defaults to the current sys.stdout.
flush
  whether to forcibly flush the stream.'''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">printdocstring </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;&#39;&#39;Prints the values to a stream, or to sys.stdout by default.</span></span>
<span class="line"></span>
<span class="line"><span style="color: #032F62">sep</span></span>
<span class="line"><span style="color: #032F62">  string inserted between values, default a space.</span></span>
<span class="line"><span style="color: #032F62">end</span></span>
<span class="line"><span style="color: #032F62">  string appended after the last value, default a newline.</span></span>
<span class="line"><span style="color: #032F62">file</span></span>
<span class="line"><span style="color: #032F62">  a file-like object (stream); defaults to the current sys.stdout.</span></span>
<span class="line"><span style="color: #032F62">flush</span></span>
<span class="line"><span style="color: #032F62">  whether to forcibly flush the stream.&#39;&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Notice that the sep and end default arguments are assigned to string literals which use single quotations. If more details about the possible valid string literals are to be included in the docstring, it is more convenient to use double quotations to enclose the docstring:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"printdocstring = \u0022\u0022\u0022Prints the values to a stream, or to sys.stdout by default.\n\nsep\n  string inserted between values, default a ' '.\nend\n  string appended after the last value, default a '\\\\n'.\nfile\n  a file-like object (stream); defaults to the current sys.stdout.\nflush\n  whether to forcibly flush the stream.\u0022\u0022\u0022","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eprintdocstring \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026quot;\u0026quot;\u0026quot;Prints the values to a stream, or to sys.stdout by default.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003esep\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  string inserted between values, default a \u0026#39; \u0026#39;.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eend\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  string appended after the last value, default a \u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\\\\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003en\u0026#39;.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003efile\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  a file-like object (stream); defaults to the current sys.stdout.\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eflush\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e  whether to forcibly flush the stream.\u0026quot;\u0026quot;\u0026quot;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="printdocstring = &quot;&quot;&quot;Prints the values to a stream, or to sys.stdout by default.

sep
  string inserted between values, default a ' '.
end
  string appended after the last value, default a '\\n'.
file
  a file-like object (stream); defaults to the current sys.stdout.
flush
  whether to forcibly flush the stream.&quot;&quot;&quot;" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">printdocstring </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&quot;&quot;&quot;Prints the values to a stream, or to sys.stdout by default.</span></span>
<span class="line"></span>
<span class="line"><span style="color: #032F62">sep</span></span>
<span class="line"><span style="color: #032F62">  string inserted between values, default a &#39; &#39;.</span></span>
<span class="line"><span style="color: #032F62">end</span></span>
<span class="line"><span style="color: #032F62">  string appended after the last value, default a &#39;</span><span style="color: #005CC5">\\</span><span style="color: #032F62">n&#39;.</span></span>
<span class="line"><span style="color: #032F62">file</span></span>
<span class="line"><span style="color: #032F62">  a file-like object (stream); defaults to the current sys.stdout.</span></span>
<span class="line"><span style="color: #032F62">flush</span></span>
<span class="line"><span style="color: #032F62">  whether to forcibly flush the stream.&quot;&quot;&quot;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>When functions are made, the docstring typically starts off as a single line docstring and sometimes this is enough for example:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  object.mro()
Docstring: Return a type's method resolution order.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Triple double quotes are generally used so that it is easier for subsequent expansion over multiple lines and is easy to add string literals to it:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"fillmeinlater = \u0022\u0022\u0022This is a placeholder docstring\u0022\u0022\u0022","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efillmeinlater \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026quot;\u0026quot;\u0026quot;This is a placeholder docstring\u0026quot;\u0026quot;\u0026quot;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="fillmeinlater = &quot;&quot;&quot;This is a placeholder docstring&quot;&quot;&quot;" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">fillmeinlater </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&quot;&quot;&quot;This is a placeholder docstring&quot;&quot;&quot;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"fillmeinlater = \u0022\u0022\u0022This is a placeholder docstring\nAdd note about string literal 'hello' and 'bye'\u0022\u0022\u0022","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003efillmeinlater \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026quot;\u0026quot;\u0026quot;This is a placeholder docstring\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eAdd note about string literal \u0026#39;hello\u0026#39; and \u0026#39;bye\u0026#39;\u0026quot;\u0026quot;\u0026quot;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="fillmeinlater = &quot;&quot;&quot;This is a placeholder docstring
Add note about string literal 'hello' and 'bye'&quot;&quot;&quot;" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">fillmeinlater </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&quot;&quot;&quot;This is a placeholder docstring</span></span>
<span class="line"><span style="color: #032F62">Add note about string literal &#39;hello&#39; and &#39;bye&#39;&quot;&quot;&quot;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="ascii-and-unicode-escape-characters">ASCII and Unicode Escape Characters</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>If the ordinal values of the English letter 'a' (ASCII) and Greek letter 'α' (Unicode) are compared:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"ord('a')\nord('α')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;a\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;α\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="ord('a')
ord('α')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">ord</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;a&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #005CC5">ord</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;α&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>97
945</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice that the ASCII letter is between 0-128 and the ASCII letter is in the range 256-65536. Let's examine what these numbers mean in a bit more detail. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Under the hood a computers memory consists of a series of binary switches. A single switch can be conceptualised as an LED that is either off or on, which correspond to the values 0 and 1 respectively:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":56986,"sizeSlug":"full","linkDestination":"media"} -->
<figure class="wp-block-image size-full"><a href="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image-2.png"><img src="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image-2.png" alt="" class="wp-image-56986"/></a></figure>
<!-- /wp:image -->

<!-- wp:image {"id":56987,"sizeSlug":"full","linkDestination":"media"} -->
<figure class="wp-block-image size-full"><a href="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image-3.png"><img src="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/image-3.png" alt="" class="wp-image-56987"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>For 1 bit there are only 2 ** 1 configurations:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"2 ** 1","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e**\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="2 ** 1" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">2</span><span style="color: #24292E"> </span><span style="color: #D73A49">**</span><span style="color: #24292E"> </span><span style="color: #005CC5">1</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>2</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>This gives the range from 0-2 using zero-order indexing. In zero-order indexing the lowest bound 0 is included however the upper bound is exclusive, so 0-2 means 0 inclusive of 0, going up in steps of 1 until 2 is reached but not including 2 itself, giving the possible values 0 and 1. To count to larger numbers, the bits are commonly arranged into groupings of 8 known as a bit:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":56990,"width":770,"height":253,"sizeSlug":"large","linkDestination":"media"} -->
<figure class="wp-block-image size-large is-resized"><a href="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/img_225.png"><img src="https://dellwindowsreinstallationguide.com/wp-content/uploads/2023/04/img_225-1024x337.png" alt="" class="wp-image-56990" width="770" height="253"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>A byte has 8 bits and each bit has 2 combinations. The total number of combinations in a byte is:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"2 ** 8","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e**\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e8\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="2 ** 8" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">2</span><span style="color: #24292E"> </span><span style="color: #D73A49">**</span><span style="color: #24292E"> </span><span style="color: #005CC5">8</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>256</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>This gives the values 0-256 (inclusive of 0 and exclusive of 256). The function bin can be used to convert a decimal integer into a binary integer:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  bin(number, /)
Docstring:
Return the binary representation of an integer.

>>> bin(2796202)
'0b1010101010101010101010'
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Recall that the character 'a' had an ordinal value of 97:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"bin(97)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ebin\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e97\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="bin(97)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">bin</span><span style="color: #24292E">(</span><span style="color: #005CC5">97</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0b1100001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>0b is the prefix meaning binary and the 7 bits following the b is the binary sequence. The trailing zero is not shown, for a byte this is 01100001. Notice this is the 97th configuration of the byte and is the same as the LED sequence indicated above.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Binary is machine readable but not human readable; it is easy for a human to mis-transcribe a large binary sequence. As a consequence four binary digits of 2 characters which have:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"2 ** 4","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e**\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e4\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="2 ** 4" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">2</span><span style="color: #24292E"> </span><span style="color: #D73A49">**</span><span style="color: #24292E"> </span><span style="color: #005CC5">4</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">16</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>configurations are instead grouped into a single hexadecimal character. There are 16 hexadecimal characters 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f. The docstring of the hex function can be examined:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  hex(number, /)
Docstring:
Return the hexadecimal representation of an integer.

>>> hex(12648430)
'0xc0ffee'
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"hex(97)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ehex\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e97\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="hex(97)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">hex</span><span style="color: #24292E">(</span><span style="color: #005CC5">97</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0x61'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice the prefix 0x meaning hexadecimal, this prefix distinguishes the hexadecimal 0x61 from the decimal 61; recalling the hexadecimal 61 equals the decimal 97.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Each ASCII character corresponds to 1 byte which is eight bits or two hexadecimal integers. A Unicode character normally corresponds to 2 bytes which is sixteen bits or four hexadecimal characters.</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"bin(945)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ebin\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e945\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="bin(945)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">bin</span><span style="color: #24292E">(</span><span style="color: #005CC5">945</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0b1110110001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There are 10 bits here, to bring the trailing zeros up to 2 bytes (16 bits), this would be 0000001110110001. In hex this is:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"hex(945)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ehex\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e945\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="hex(945)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">hex</span><span style="color: #24292E">(</span><span style="color: #005CC5">945</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0x3b1'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>This gives 3 hexadecimal characters, to bring the trailing zeros up to 2 bytes (4 hexadecimal characters), this would be 03b1.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The \x and \u escape sequences can be used to insert an ASCII or Unicode escape character into a string. These escape sequences expect 2 hexadecimal digits or 4 hexadecimal digits respectively:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'\\x61'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\x61\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'\x61'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;</span><span style="color: #005CC5">\x61</span><span style="color: #032F62">&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'a'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'\\u03b1'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\u03b1\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'\u03b1'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;</span><span style="color: #005CC5">\u03b1</span><span style="color: #032F62">&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'α'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>ASCII is a subset of Unicode, however the trailing zeros need to be added to give 4 hexadecimal characters when the Unicode escape character is inserted:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'\\u0061'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\u0061\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'\u0061'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;</span><span style="color: #005CC5">\u0061</span><span style="color: #032F62">&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'a'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>ASCII characters and Unicode characters are normally included directly in a Unicode string opposed to using escape sequences like the above.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="raw-string">Raw String</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>A raw string is a string without escape sequences and the \ is a character. The raw string is prefixed by r. The most common purpose is for a file path or a regular expression:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"r'C:\\Users\\Philip'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003er\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;C:\\Users\\Philip\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="r'C:\Users\Philip'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">r</span><span style="color: #032F62">&#39;C:\Users\Philip&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'C:\\Users\\Philip'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"print(r'C:\\Users\\Philip')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003er\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;C:\u003c/span\u003e\u003cspan style=\u0022color: #22863A; font-weight: bold\u0022\u003e\\U\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003esers\u003c/span\u003e\u003cspan style=\u0022color: #22863A; font-weight: bold\u0022\u003e\\P\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003ehilip\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="print(r'C:\Users\Philip')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">print</span><span style="color: #24292E">(</span><span style="color: #D73A49">r</span><span style="color: #032F62">&#39;C:</span><span style="color: #22863A; font-weight: bold">\U</span><span style="color: #032F62">sers</span><span style="color: #22863A; font-weight: bold">\P</span><span style="color: #032F62">hilip&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>C:\Users\Philip</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="formatted-strings">Formatted Strings</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Supposing the following string is instantiated:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody = 'The string to 0 is 1 2!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to 0 is 1 2!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody = 'The string to 0 is 1 2!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The string to 0 is 1 2!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The format method can be used to insert other variables into a string body using an optional format specification:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.format(*args, **kwargs) -> str

Return a formatted version of S, using substitutions from args and kwargs.
The substitutions are identified by braces ('{' and '}').
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>In a formatted string braces { } are used as placeholders for the variables, this means the stringbody should be updated to:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody = 'The string to {0} is {1} {2}!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{0}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{1}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{2}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody = 'The string to {0} is {1} {2}!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{0}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{1}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{2}</span><span style="color: #032F62">!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The format method can take in a variable number of positional input arguments *args, these *args should correspond to the numeric placeholders above. Since 0, 1 and 2 are provided, three positional input arguments should be provided in the format method. Let's create three strings:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"str0 = 'print'\nstr1 = 'hello'\nstr2 = 'world'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;print\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;world\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="str0 = 'print'
str1 = 'hello'
str2 = 'world'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">str0 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;print&#39;</span></span>
<span class="line"><span style="color: #24292E">str1 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello&#39;</span></span>
<span class="line"><span style="color: #24292E">str2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;world&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Now the format method can be used supplying these three strings as positional input arguments:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody.format(str0, str1, str2)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody.format(str0, str1, str2)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody.format(str0, str1, str2)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody.format(str0, str1, str2)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The string to print is hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Alternatively if the placeholders are changed to instance names:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody = 'The string to {str0} is {str1} {str2}!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{str0}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{str1}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{str2}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody = 'The string to {str0} is {str1} {str2}!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{str0}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{str1}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{str2}</span><span style="color: #032F62">!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Then a variable number of named keyword arguments **kwargs can be specified, these should match the instance names in the stringbody:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody.format(str0='print', str1='hello', str2='world')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody.format(\u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003estr0\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;print\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003estr1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003estr2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;world\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody.format(str0='print', str1='hello', str2='world')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody.format(</span><span style="color: #E36209">str0</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;print&#39;</span><span style="color: #24292E">, </span><span style="color: #E36209">str1</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E">, </span><span style="color: #E36209">str2</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;world&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The string to print is hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>It is more common for the values to be assigned to previously created instances:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"str0 = 'print'\nstr1 = 'hello'\nstr2 = 'world'\n\nstringbody = 'The string to {str0} is {str1} {str2}!'\nformattedstring = stringbody.format(str0=str0, str1=str1, str2=str2)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;print\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;world\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{str0}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{str1}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{str2}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eformattedstring \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e stringbody.format(\u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003estr0\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003estr1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003estr2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="str0 = 'print'
str1 = 'hello'
str2 = 'world'

stringbody = 'The string to {str0} is {str1} {str2}!'
formattedstring = stringbody.format(str0=str0, str1=str1, str2=str2)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">str0 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;print&#39;</span></span>
<span class="line"><span style="color: #24292E">str1 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello&#39;</span></span>
<span class="line"><span style="color: #24292E">str2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;world&#39;</span></span>
<span class="line"></span>
<span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{str0}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{str1}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{str2}</span><span style="color: #032F62">!&#39;</span></span>
<span class="line"><span style="color: #24292E">formattedstring </span><span style="color: #D73A49">=</span><span style="color: #24292E"> stringbody.format(</span><span style="color: #E36209">str0</span><span style="color: #D73A49">=</span><span style="color: #24292E">str0, </span><span style="color: #E36209">str1</span><span style="color: #D73A49">=</span><span style="color: #24292E">str1, </span><span style="color: #E36209">str2</span><span style="color: #D73A49">=</span><span style="color: #24292E">str2)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Notice in the last two lines the duplication of each instance name. These two lines are typically combined and abbreviated using a f string. A f string under the hood uses the format method and inserts the variables directly into the formatted string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"formattedstring = f'The string to {str0} is {str1} {str2}!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eformattedstring \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="formattedstring = f'The string to {str0} is {str1} {str2}!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">formattedstring </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{</span><span style="color: #24292E">str0</span><span style="color: #005CC5">}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{</span><span style="color: #24292E">str1</span><span style="color: #005CC5">}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{</span><span style="color: #24292E">str2</span><span style="color: #005CC5">}</span><span style="color: #032F62">!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The object and hence all other classes has the data model method __format__:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  object.__format__(self, format_spec, /)
Docstring: Default object formatter.
Type:      method_descriptor</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>By default an object being inserted in a placeholder string is inserted using the syntax {obj} and uses its informal string representation. The data model method __format__ under the hood specifies how the object is to be represented as a string when inserted alongside a format specifier. When a format specifier is used the syntax is {obj:formatspec} which has a loose similarity to a mapping. Since these are strings, the string format specifier s will be used:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The string to {str0:s} is {str1:s} {str2:s}!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The string to {str0:s} is {str1:s} {str2:s}!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{</span><span style="color: #24292E">str0</span><span style="color: #D73A49">:s</span><span style="color: #005CC5">}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{</span><span style="color: #24292E">str1</span><span style="color: #D73A49">:s</span><span style="color: #005CC5">}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{</span><span style="color: #24292E">str2</span><span style="color: #D73A49">:s</span><span style="color: #005CC5">}</span><span style="color: #032F62">!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The string to print is hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Note there is no space around the colon. If a space is inserted before the colon which is the typical syntax used for a mapping:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The string to {str0: s} is {str1: s} {str2: s}!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e: s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e: s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e: s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The string to {str0: s} is {str1: s} {str2: s}!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{</span><span style="color: #24292E">str0</span><span style="color: #D73A49">: s</span><span style="color: #005CC5">}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{</span><span style="color: #24292E">str1</span><span style="color: #D73A49">: s</span><span style="color: #005CC5">}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{</span><span style="color: #24292E">str2</span><span style="color: #D73A49">: s</span><span style="color: #005CC5">}</span><span style="color: #032F62">!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>ValueError: Space not allowed in string format specifier</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If an integer is prefixed before the string format specifier, any string shorter than the number will occupy the number of specified places using trailing whitespace. If the integer is prefixed with 0, the trailing whitespace will be replaced by 0. For example:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The string to {str0:8s} is {str1} {str2:08s}!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The string to \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr0\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:8s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e is \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr1\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estr2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:08s\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The string to {str0:8s} is {str1} {str2:08s}!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The string to </span><span style="color: #005CC5">{</span><span style="color: #24292E">str0</span><span style="color: #D73A49">:8s</span><span style="color: #005CC5">}</span><span style="color: #032F62"> is </span><span style="color: #005CC5">{</span><span style="color: #24292E">str1</span><span style="color: #005CC5">}</span><span style="color: #032F62"> </span><span style="color: #005CC5">{</span><span style="color: #24292E">str2</span><span style="color: #D73A49">:08s</span><span style="color: #005CC5">}</span><span style="color: #032F62">!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The string to print    is hello world000!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Formatted strings are frequently used to insert numbers into a string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"num1 = 1\nnum2 = 0.0000123456789\nnum3 = 12.3456789\n\nf'The numbers are {num1}, {num2} and {num3}.' ","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e0.0000123456789\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e12.3456789\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="num1 = 1
num2 = 0.0000123456789
num3 = 12.3456789

f'The numbers are {num1}, {num2} and {num3}.' " style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">num1 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">1</span></span>
<span class="line"><span style="color: #24292E">num2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">0.0000123456789</span></span>
<span class="line"><span style="color: #24292E">num3 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">12.3456789</span></span>
<span class="line"></span>
<span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span><span style="color: #24292E"> </span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 1.23456789e-05 and 12.3456789.'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>num1 is a decimal integer, which is a whole number.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>num2 is a small floating point number much smaller than a unit. Because it is much smaller than a unit, it is displayed in scientific notation. A floating point much larger than a unit is also displayed in scientific notation.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>num3 is a floating point number comparable to a unit and shown using standard notation.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are additional format specifiers for other datatypes:</p>
<!-- /wp:paragraph -->

<!-- wp:jetpack/markdown {"source":"|datatype|specifier|\n|\u002d\u002d-|\u002d\u002d-|\n|string|:s|\n|general format|:g|\n|decimal integer|:d|\n|fixed point format (standard format)|:f|\n|exponent format (scientific notation)|:e|"} -->
<div class="wp-block-jetpack-markdown"><table>
<thead>
<tr>
<th>datatype</th>
<th>specifier</th>
</tr>
</thead>
<tbody>
<tr>
<td>string</td>
<td>:s</td>
</tr>
<tr>
<td>general format</td>
<td>:g</td>
</tr>
<tr>
<td>decimal integer</td>
<td>:d</td>
</tr>
<tr>
<td>fixed point format (standard format)</td>
<td>:f</td>
</tr>
<tr>
<td>exponent format (scientific notation)</td>
<td>:e</td>
</tr>
</tbody>
</table>
</div>
<!-- /wp:jetpack/markdown -->

<!-- wp:paragraph -->
<p>For numeric variables by default the general format is used:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:g}, {num2:g} and {num3:g}.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:g}, {num2:g} and {num3:g}.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">'The numbers are 1, 1.23457e-05 and 12.3457.'</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>The decimal integer format can be used for the whole number, this can be prefixed with the number of desired spaces and a zero to show leading zeros:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:d}, {num2:g} and {num3:g}.' ","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:d}, {num2:g} and {num3:g}.' " style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span><span style="color: #24292E"> </span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 1.23457e-05 and 12.3457.'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:5d}, {num2:g} and {num3:g}.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:5d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:5d}, {num2:g} and {num3:g}.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:5d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are     1, 1.23457e-05 and 12.3457.'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:05d}, {num2:g} and {num3:g}.' ","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:05d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:05d}, {num2:g} and {num3:g}.' " style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:05d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span><span style="color: #24292E"> </span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 00001, 1.23457e-05 and 12.3457.'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice the change in num2 and num3 when the fixed point format and exponentials are used:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:d}, {num2:g} and {num3:g}.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:g\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:d}, {num2:g} and {num3:g}.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:g</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 1.23457e-05 and 12.3457.'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:d}, {num2:f} and {num3:f}.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:f\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:f\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:d}, {num2:f} and {num3:f}.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:f</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:f</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 0.000012 and 12.345679.'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:d}, {num2:e} and {num3:e}.' ","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:e\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:e\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:d}, {num2:e} and {num3:e}.' " style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:e</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:e</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span><span style="color: #24292E"> </span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 1.234568e-05 and 1.234568e+01.'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><span style="font-family: -apple-system, BlinkMacSystemFont, &quot;Segoe WPC&quot;, &quot;Segoe UI&quot;, system-ui, Ubuntu, &quot;Droid Sans&quot;, sans-serif; font-size: 14px; white-space: normal;">The format specification in either case be change to .3 which indicates a precision of 3 digits past the decimal point</span>:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:d}, {num2:.3f} and {num3:.3f}.' ","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:.3f\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:.3f\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:d}, {num2:.3f} and {num3:.3f}.' " style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:.3f</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:.3f</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span><span style="color: #24292E"> </span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 0.000 and 12.346.'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"f'The numbers are {num1:d}, {num2:.3e} and {num3:.3e}.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ef\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:.3e\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:.3e\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="f'The numbers are {num1:d}, {num2:.3e} and {num3:.3e}.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">f</span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{</span><span style="color: #24292E">num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{</span><span style="color: #24292E">num2</span><span style="color: #D73A49">:.3e</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{</span><span style="color: #24292E">num3</span><span style="color: #D73A49">:.3e</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 1.235e-05 and 1.235e+01.'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The keys of the mapping can be included in the placeholder, alongside an optional format specifier:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"numbers = {'num1': 1, 'num2': 0.0000123456789, 'num3': 12.3456789}\n           \nstringbody = 'The numbers are {num1:d}, {num2:.3e} and {num3:.3e}.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enumbers \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e {\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;num1\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;num2\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e0.0000123456789\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;num3\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e12.3456789\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e}\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e           \u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{num1\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:d\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{num2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:.3e\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e{num3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e:.3e\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e}\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="numbers = {'num1': 1, 'num2': 0.0000123456789, 'num3': 12.3456789}
           
stringbody = 'The numbers are {num1:d}, {num2:.3e} and {num3:.3e}.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">numbers </span><span style="color: #D73A49">=</span><span style="color: #24292E"> {</span><span style="color: #032F62">&#39;num1&#39;</span><span style="color: #24292E">: </span><span style="color: #005CC5">1</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;num2&#39;</span><span style="color: #24292E">: </span><span style="color: #005CC5">0.0000123456789</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;num3&#39;</span><span style="color: #24292E">: </span><span style="color: #005CC5">12.3456789</span><span style="color: #24292E">}</span></span>
<span class="line"><span style="color: #24292E">           </span></span>
<span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">{num1</span><span style="color: #D73A49">:d</span><span style="color: #005CC5">}</span><span style="color: #032F62">, </span><span style="color: #005CC5">{num2</span><span style="color: #D73A49">:.3e</span><span style="color: #005CC5">}</span><span style="color: #032F62"> and </span><span style="color: #005CC5">{num3</span><span style="color: #D73A49">:.3e</span><span style="color: #005CC5">}</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>There is another string method called format_map which creates a formatted string from a mapping:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.format_map(mapping) -> str

Return a formatted version of S, using substitutions from mapping.
The substitutions are identified by braces ('{' and '}').
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody.format_map(numbers)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody.format_map(numbers)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody.format_map(numbers)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody.format_map(numbers)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">'The numbers are 1, 1.235e-05 and 1.235e+01.'</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>Note in the above that there is spacing after each colon in the mapping which follows PEP8 and emphasises the separation of the key and the value in the mapping. This is not done in the string body as the space would otherwise get incorporated to give 'num1 ' instead of 'num1'. This can be seen with:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"numbers = {'num1': 1, 'num2': 0.0000123456789, 'num3': 12.3456789}\n\nstringbody = 'The numbers are {num1 :d}, {num2 :.3e} and {num3 :.3e}.'\n\nstringbody.format_map(numbers)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enumbers \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e {\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;num1\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;num2\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e0.0000123456789\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;num3\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e12.3456789\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e}\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are {num1 :d}, {num2 :.3e} and {num3 :.3e}.\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody.format_map(numbers)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="numbers = {'num1': 1, 'num2': 0.0000123456789, 'num3': 12.3456789}

stringbody = 'The numbers are {num1 :d}, {num2 :.3e} and {num3 :.3e}.'

stringbody.format_map(numbers)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">numbers </span><span style="color: #D73A49">=</span><span style="color: #24292E"> {</span><span style="color: #032F62">&#39;num1&#39;</span><span style="color: #24292E">: </span><span style="color: #005CC5">1</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;num2&#39;</span><span style="color: #24292E">: </span><span style="color: #005CC5">0.0000123456789</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;num3&#39;</span><span style="color: #24292E">: </span><span style="color: #005CC5">12.3456789</span><span style="color: #24292E">}</span></span>
<span class="line"></span>
<span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The numbers are {num1 :d}, {num2 :.3e} and {num3 :.3e}.&#39;</span></span>
<span class="line"></span>
<span class="line"><span style="color: #24292E">stringbody.format_map(numbers)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>KeyError: 'num1 '</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There is also an older style of formatted strings which uses the % as a placeholder followed by a format specifier:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody = 'The numbers are %d, %.3e and %.3e.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%d\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%.3e\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%.3e\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody = 'The numbers are %d, %.3e and %.3e.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">%d</span><span style="color: #032F62">, </span><span style="color: #005CC5">%.3e</span><span style="color: #032F62"> and </span><span style="color: #005CC5">%.3e</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The behaviour of the mod operator % is defined by the __mod__ data model identifier:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       stringbody.__mod__(value, /)
Call signature:  placeholder.__mod__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__mod__' of str object at 0x000002D0F7DE4570>
Docstring:      Return self%value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>For an old style formatted string, the mod operator % can be used with a tuple which has the same number of elements as the number of % placeholders in the string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'The numbers are %d, %.3f and %.3f.' % (num1, num2, num3)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are %d, %.3f and %.3f.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e%\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e (num1, num2, num3)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'The numbers are %d, %.3f and %.3f.' % (num1, num2, num3)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;The numbers are %d, %.3f and %.3f.&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">%</span><span style="color: #24292E"> (num1, num2, num3)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 0.000 and 12.346.'</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'The numbers are %d, %.3e and %.3e.' % (num1, num2, num3)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are %d, %.3e and %.3e.\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e%\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e (num1, num2, num3)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'The numbers are %d, %.3e and %.3e.' % (num1, num2, num3)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;The numbers are %d, %.3e and %.3e.&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">%</span><span style="color: #24292E"> (num1, num2, num3)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 1.235e-05 and 1.235e+01.'</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading">Object Design Pattern</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The data models __init__, __new__, __repr__, __str__ and __format__ have been examined which are present in the parent class object. There are a number of additional identifiers present in the parent class which are commonly used by the str class. Let's look at the object instance instance and string instance greeting to compare these: </p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance = object()\ngreeting = 'hello world!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eobject\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance = object()
greeting = 'hello world!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">instance </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">object</span><span style="color: #24292E">()</span></span>
<span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The __doc__ instance returns the docstring as a string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance.__doc__\ngreeting.__doc__","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance.\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e__doc__\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e__doc__\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance.__doc__
greeting.__doc__" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">instance.</span><span style="color: #005CC5">__doc__</span></span>
<span class="line"><span style="color: #24292E">greeting.</span><span style="color: #005CC5">__doc__</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The base class of the class hierarchy.\n\nWhen called, it accepts no arguments and returns a new featureless\ninstance that has no instance attributes and cannot be given any.\n'</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>"str(object='') -> str\nstr(bytes_or_buffer&#91;, encoding&#91;, errors]]) -> str\n\nCreate a new string object from the given object. If encoding or\nerrors is specified, then the object must expose a data buffer\nthat will be decoded using the given encoding and error handler.\nOtherwise, returns the result of object.__str__() (if defined)\nor repr(object).\nencoding defaults to sys.getdefaultencoding().\nerrors defaults to 'strict'."</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice for the string class, the docstring contains string literals so is enclosed in double quotations. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The docstring is more commonly used with the operator ? which provides some other additional information and prints the docstring:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"? instance\n? greeting","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #B31D28; font-style: italic\u0022\u003e?\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e instance\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #B31D28; font-style: italic\u0022\u003e?\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="? instance
? greeting" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #B31D28; font-style: italic">?</span><span style="color: #24292E"> instance</span></span>
<span class="line"><span style="color: #B31D28; font-style: italic">?</span><span style="color: #24292E"> greeting</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Type:        object
String form: &lt;object object at 0x0000019E7710A120>
Docstring:  
The base class of the class hierarchy.

When called, it accepts no arguments and returns a new featureless
instance that has no instance attributes and cannot be given any.</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Type:        str
String form: hello world!
Length:      12
Docstring:  
str(object='') -> str
str(bytes_or_buffer&#91;, encoding&#91;, errors]]) -> str

Create a new string object from the given object. If encoding or
errors is specified, then the object must expose a data buffer
that will be decoded using the given encoding and error handler.
Otherwise, returns the result of object.__str__() (if defined)
or repr(object).
encoding defaults to sys.getdefaultencoding().
errors defaults to 'strict'.</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The type of the classes are object and str respectively. The type can be read off using the attribute __class__:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance.__class__\ngreeting.__class__","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance.\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e__class__\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e__class__\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance.__class__
greeting.__class__" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">instance.</span><span style="color: #005CC5">__class__</span></span>
<span class="line"><span style="color: #24292E">greeting.</span><span style="color: #005CC5">__class__</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>object
str</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The data model identifier is typically not used directly, instead the builtins class type is used:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Init signature:  type(self, /, *args, **kwargs)
Docstring:     
type(object) -> the object's type
type(name, bases, dict, **kwds) -> a new type
Type:           type
Subclasses:     ABCMeta, EnumType, _AnyMeta, NamedTupleMeta, _TypedDictMeta, _DeprecatedType, _ABC, MetaHasDescriptors, PyCStructType, UnionType, ...</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"type(instance)\ntype(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003etype\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(instance)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003etype\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="type(instance)
type(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">type</span><span style="color: #24292E">(instance)</span></span>
<span class="line"><span style="color: #005CC5">type</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>object
str</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Recall that the data model identifier __str__ defines the behaviour of the str class on the object giving the informal string representation. For the object the str just gives the class type and its location in memory. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The location in memory is represented as an integer value using the builtins identification id:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  id(obj, /)
Docstring:
Return the identity of an object.

This is guaranteed to be unique among simultaneously existing objects.
(CPython uses the object's memory address.)
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"id(instance)\nid(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eid\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(instance)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eid\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="id(instance)
id(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">id</span><span style="color: #24292E">(instance)</span></span>
<span class="line"><span style="color: #005CC5">id</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>1780114039072
1780109053360</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Each id is unique as expected.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The length is Collection specific and not available for an object which is not a Collection. This should not be confused with the identifier __sizeof__ which defines the behaviour of sys.getsizeof and returns the size of an object in bytes:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.__sizeof__()
Docstring: Return the size of the string in memory, in bytes.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"import sys","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eimport\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e sys\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="import sys" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">import</span><span style="color: #24292E"> sys</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
getsizeof(object [, default]) -> int

Return the size of object in bytes.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"sys.getsizeof(instance)\nsys.getsizeof(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003esys.getsizeof(instance)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003esys.getsizeof(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="sys.getsizeof(instance)
sys.getsizeof(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">sys.getsizeof(instance)</span></span>
<span class="line"><span style="color: #24292E">sys.getsizeof(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>16
61</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If a directory is explored in a file explorer, each directory contains files and sub directories. In Python, an object is conceptualised as a directory and the identifiers in the directory can be output as a list. The data model identifier __dir__ defines the behaviour of the dir function. </p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.__dir__()
Docstring: Default dir() implementation.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
dir([object]) -> list of strings

If called without an argument, return the names in the current scope.
Else, return an alphabetized list of names comprising (some of) the attributes
of the given object, and of attributes reachable from it.
If the object supplies a method named __dir__, it will be used; otherwise
the default dir() logic is used and returns:
  for a module object: the module's attributes.
  for a class object:  its attributes, and recursively the attributes
    of its bases.
  for any other object: its attributes, its class's attributes, and
    recursively the attributes of its class's base classes.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>dir can be used on instance and greeting:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"dir(instance)\ndir(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003edir\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(instance)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003edir\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="dir(instance)
dir(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">dir</span><span style="color: #24292E">(instance)</span></span>
<span class="line"><span style="color: #005CC5">dir</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&#91;'__class__',
 '__delattr__',
 '__dir__',
 '__doc__',
 '__eq__',
 '__format__',
 '__ge__',
 '__getattribute__',
 '__getstate__',
 '__gt__',
 '__hash__',
 '__init__',
 '__init_subclass__',
 '__le__',
 '__lt__',
 '__ne__',
 '__new__',
 '__reduce__',
 '__reduce_ex__',
 '__repr__',
 '__setattr__',
 '__sizeof__',
 '__str__',
 '__subclasshook__']</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&#91;'__add__',
 '__class__',
 '__contains__',
 '__delattr__',
 '__dir__',
 '__doc__',
 '__eq__',
 '__format__',
 '__ge__',
 '__getattribute__',
 '__getitem__',
 '__getnewargs__',
 '__getstate__',
 '__gt__',
 '__hash__',
 '__init__',
 '__init_subclass__',
 '__iter__',
 '__le__',
 '__len__',
 '__lt__',
 '__mod__',
 '__mul__',
 '__ne__',
 '__new__',
 '__reduce__',
 '__reduce_ex__',
 '__repr__',
 '__rmod__',
 '__rmul__',
 '__setattr__',
 '__sizeof__',
 '__str__',
 '__subclasshook__',
 'capitalize',
 'casefold',
 'center',
 'count',
 'encode',
 'endswith',
 'expandtabs',
 'find',
 'format',
 'format_map',
 'index',
 'isalnum',
 'isalpha',
 'isascii',
 'isdecimal',
 'isdigit',
 'isidentifier',
 'islower',
 'isnumeric',
 'isprintable',
 'isspace',
 'istitle',
 'isupper',
 'join',
 'ljust',
 'lower',
 'lstrip',
 'maketrans',
 'partition',
 'removeprefix',
 'removesuffix',
 'replace',
 'rfind',
 'rindex',
 'rjust',
 'rpartition',
 'rsplit',
 'rstrip',
 'split',
 'splitlines',
 'startswith',
 'strip',
 'swapcase',
 'title',
 'translate',
 'upper',
 'zfill']</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="length-and-type">Immutable Ordered Collection ABC Design Pattern</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Let's have a look at the str instance:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello world!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello world!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Earlier it was seen that the str was a subclass of the object and therefore followed the design pattern of an object. The design pattern of the str class actually has a number of abstract base classes. An abstract base class is a conceptual class, that isn't instantiated directly but used as a design pattern for numerous Python classes so their behaviour is consistent.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The str has a Container abstract base class, which means it has the data model method __contains__:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__contains__(key, /)
Call signature:  greeting.__contains__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__contains__' of str object at 0x0000019E76C48DB0>
Docstring:      Return key in self.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>This data model method maps to the keyword in, which can be used to check whether a substring is in a string or if a string contains a substring. This can be used with the following letter and substring:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"letter = 'h'\nword = 'hello'\nletter in greeting\nword in greeting","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eletter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;h\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eword \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eletter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eword \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="letter = 'h'
word = 'hello'
letter in greeting
word in greeting" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">letter </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;h&#39;</span></span>
<span class="line"><span style="color: #24292E">word </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello&#39;</span></span>
<span class="line"><span style="color: #24292E">letter </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greeting</span></span>
<span class="line"><span style="color: #24292E">word </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greeting</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True
True</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Note this is case-sensitive so if the following letter and substring are searched for the results will be False:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"letter = 'H'\nword = 'Hello'\nletter in greeting\nword in greeting","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eletter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;H\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eword \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eletter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eword \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="letter = 'H'
word = 'Hello'
letter in greeting
word in greeting" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">letter </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;H&#39;</span></span>
<span class="line"><span style="color: #24292E">word </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Hello&#39;</span></span>
<span class="line"><span style="color: #24292E">letter </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greeting</span></span>
<span class="line"><span style="color: #24292E">word </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greeting</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>False
False</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If the case-sensitivity is to be dropped, the casefold method can be used:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"letter.casefold() in greeting.casefold()\nword.casefold() in greeting.casefold()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eletter.casefold() \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting.casefold()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eword.casefold() \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting.casefold()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="letter.casefold() in greeting.casefold()
word.casefold() in greeting.casefold()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">letter.casefold() </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greeting.casefold()</span></span>
<span class="line"><span style="color: #24292E">word.casefold() </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greeting.casefold()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True
True</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The string is also Hashable which means it has the data model method __hash__ which maps to builtins hash:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__hash__()
Call signature:  greeting.__hash__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__hash__' of str object at 0x0000019E76C48DB0>
Docstring:      Return hash(self).</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  hash(obj, /)
Docstring:
Return the hash value for the given object.

Two objects that compare equal must also have the same hash value, but the
reverse is not necessarily true.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The hash value corresponds to an integer:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"hash(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ehash\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="hash(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">hash</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>6476820586813634871</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Having a hash value, means the object can be used as a key in a mapping and the key is used to index into a mapping to retrieve the associated value:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"colors = {'red': '#ff0000', 'green': '#00b050', 'blue': '#0070c0'}\nhash('red')\ncolors['red']","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ecolors \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e {\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;red\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;#ff0000\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;green\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;#00b050\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;blue\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;#0070c0\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e}\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ehash\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;red\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ecolors[\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;red\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="colors = {'red': '#ff0000', 'green': '#00b050', 'blue': '#0070c0'}
hash('red')
colors['red']" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">colors </span><span style="color: #D73A49">=</span><span style="color: #24292E"> {</span><span style="color: #032F62">&#39;red&#39;</span><span style="color: #24292E">: </span><span style="color: #032F62">&#39;#ff0000&#39;</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;green&#39;</span><span style="color: #24292E">: </span><span style="color: #032F62">&#39;#00b050&#39;</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;blue&#39;</span><span style="color: #24292E">: </span><span style="color: #032F62">&#39;#0070c0&#39;</span><span style="color: #24292E">}</span></span>
<span class="line"><span style="color: #005CC5">hash</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;red&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">colors[</span><span style="color: #032F62">&#39;red&#39;</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>9014713669131661868
'#ff0000'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The str is an Iterable which has the data model method __iter__, that controls the behaviour of the builtins iter:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__iter__()
Call signature:  greeting.__iter__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__iter__' of str object at 0x0000019E76C48DB0>
Docstring:      Implement iter(self).</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
iter(iterable) -> iterator
iter(callable, sentinel) -> iterator

Get an iterator from an object.  In the first form, the argument must
supply its own iterator, or be a sequence.
In the second form, the callable is called until it returns the sentinel.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>This constructs an iterator from the str.  </p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"forward = iter(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eforward \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eiter\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="forward = iter(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">forward </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">iter</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;str_ascii_iterator at 0x19e75d05cc0></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>An iterator has no regular identifiers but has a number of data model identifiers:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>__class__ - class</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__delattr__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__dir__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__doc__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__eq__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__format__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__ge__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getattribute__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__getstate__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__gt__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__hash__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__init__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__init_subclass__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__iter__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__le__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__length_hint__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__lt__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__ne__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__new__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__next__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__reduce__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__reduce_ex__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__repr__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__setattr__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__setstate__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__sizeof__ - function</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__str__ - instance</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>__subclasshook__ - function</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Most of these are inherited from the object parent class. An iterator has the data model identifier __next__ which defines how the builtins next behaves:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       forward.__next__()
Call signature:  forward.__next__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__next__' of str_ascii_iterator object at 0x0000019E75D05CC0>
Docstring:      Implement next(self).</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
next(iterator[, default])

Return the next item from the iterator. If default is given and the iterator
is exhausted, it is returned instead of raising StopIteration.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>An iterator takes on a single value at a time and advances using the builtins next. When an iterator advances the previous value it takes is consumed. For the ASCII iterator obtained from the str, the iterator takes on the next ASCII character every time next is invoked:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"next(forward)\nnext(forward)\nnext(forward)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(forward)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(forward)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(forward)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="next(forward)
next(forward)
next(forward)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(forward)</span></span>
<span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(forward)</span></span>
<span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(forward)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'h'
'e'
'l'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A slightly different str_iterator will be obtained when the str being converted to an iterator contains Unicode characters:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greek_greeting = 'Γειά σου Κόσμε!'\nforward = iter(greek_greeting)\nforward","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreek_greeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Γειά σου Κόσμε!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eforward \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eiter\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greek_greeting)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eforward\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greek_greeting = 'Γειά σου Κόσμε!'
forward = iter(greek_greeting)
forward" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greek_greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Γειά σου Κόσμε!&#39;</span></span>
<span class="line"><span style="color: #24292E">forward </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">iter</span><span style="color: #24292E">(greek_greeting)</span></span>
<span class="line"><span style="color: #24292E">forward</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;str_iterator at 0x19e75d2b700></code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"next(forward)\nnext(forward)\nnext(forward)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(forward)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(forward)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(forward)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="next(forward)
next(forward)
next(forward)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(forward)</span></span>
<span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(forward)</span></span>
<span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(forward)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'Γ'
'ε'
'ι'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>When a for loop is used with a str, under the hood an iterator is created and consumed by the for loop. A simple for loop can be made which prints each letter twice:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"for letter in greek_greeting:\n    print(letter, sep='', end='')\n    print(letter, sep='', end='')\n","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003efor\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e letter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greek_greeting:\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(letter, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003esep\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003eend\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(letter, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003esep\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #E36209\u0022\u003eend\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="for letter in greek_greeting:
    print(letter, sep='', end='')
    print(letter, sep='', end='')
" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">for</span><span style="color: #24292E"> letter </span><span style="color: #D73A49">in</span><span style="color: #24292E"> greek_greeting:</span></span>
<span class="line"><span style="color: #24292E">    </span><span style="color: #005CC5">print</span><span style="color: #24292E">(letter, </span><span style="color: #E36209">sep</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;&#39;</span><span style="color: #24292E">, </span><span style="color: #E36209">end</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">    </span><span style="color: #005CC5">print</span><span style="color: #24292E">(letter, </span><span style="color: #E36209">sep</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;&#39;</span><span style="color: #24292E">, </span><span style="color: #E36209">end</span><span style="color: #D73A49">=</span><span style="color: #032F62">&#39;&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>ΓΓεειιάά  σσοουυ  ΚΚόόσσμμεε!!</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>for loops will be covered in a subsequent tutorial on programming constructs.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>What is important to note here is the str is an Iterable but not an Iterator. An Iterable means an Iterator can be created from the Iterable using the iter function from builtins. This means the str itself does not possess the data model method __next__.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The string is also Sized which means it has the data model method __len__ which defines the behaviour of the builtins function len:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__len__()
Call signature:  greeting.__len__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__len__' of str object at 0x0000019E76C48DB0>
Docstring:      Return len(self).</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  len(obj, /)
Docstring: Return the number of items in a container.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The len function will return the integer number of Unicode characters in a string:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"len(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003elen\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="len(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">len</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>12</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The number of letters can be counted using a for loop:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"for index, letter in enumerate(greeting):\n    print(index, letter)\n    ","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003efor\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e index, letter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eenumerate\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting):\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(index, letter)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="for index, letter in enumerate(greeting):
    print(index, letter)
    " style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">for</span><span style="color: #24292E"> index, letter </span><span style="color: #D73A49">in</span><span style="color: #24292E"> </span><span style="color: #005CC5">enumerate</span><span style="color: #24292E">(greeting):</span></span>
<span class="line"><span style="color: #24292E">    </span><span style="color: #005CC5">print</span><span style="color: #24292E">(index, letter)</span></span>
<span class="line"><span style="color: #24292E">    </span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>0 h
1 e
2 l
3 l
4 o
5  
6 w
7 o
8 r
9 l
10 d
11 !</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A string is a Collection, which means it has all the properties from Sized, Iterable and Container seen above.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>A string is also an Sequence which means it contains the data model identifiers __getitem__, __len__, __contains__, __iter__ and __reversed__ alongside the identifiers index and count.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The data model identifier __getitem__ defines the behaviour when indexing into the Collection using square brackets [ ]:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__getitem__(key, /)
Call signature:  greeting.__getitem__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__getitem__' of str object at 0x0000019E76C48DB0>
Docstring:      Return self[key].</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>For example:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[1]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[1]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">1</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'e'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Recall that zero-order indexing is used, so the 2nd Unicode character is at an index of 1, and the 1st Unicode character is at an index of 0. Confer with the output of for loop used above for more details.</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"for index, letter in enumerate(greeting):\n    print(index - len(greeting), letter)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003efor\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e index, letter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eenumerate\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting):\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(index \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e-\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003elen\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting), letter)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="for index, letter in enumerate(greeting):
    print(index - len(greeting), letter)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">for</span><span style="color: #24292E"> index, letter </span><span style="color: #D73A49">in</span><span style="color: #24292E"> </span><span style="color: #005CC5">enumerate</span><span style="color: #24292E">(greeting):</span></span>
<span class="line"><span style="color: #24292E">    </span><span style="color: #005CC5">print</span><span style="color: #24292E">(index </span><span style="color: #D73A49">-</span><span style="color: #24292E"> </span><span style="color: #005CC5">len</span><span style="color: #24292E">(greeting), letter)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>-12 h
-11 e
-10 l
-9 l
-8 o
-7  
-6 w
-5 o
-4 r
-3 l
-2 d
-1 !</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[-5]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e-\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[-5]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[</span><span style="color: #D73A49">-</span><span style="color: #005CC5">5</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'o'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The builtins slice function can be used to create a substring by slicing within square brackets:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Init signature:  slice(self, /, *args, **kwargs)
Docstring:     
slice(stop)
slice(start, stop[, step])

Create a slice object.  This is used for extended slicing (e.g. a[0:10:2]).
Type:           type
Subclasses:     </pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The slice object also uses zero-order indexing. It has three possible forms:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"slice(stop) # 1\nslice(start, stop) # 2\nslice(start, stop, step) # 3","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eslice\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(stop) \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# 1\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eslice\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(start, stop) \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# 2\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eslice\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(start, stop, step) \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# 3\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="slice(stop) # 1
slice(start, stop) # 2
slice(start, stop, step) # 3" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">slice</span><span style="color: #24292E">(stop) </span><span style="color: #6A737D"># 1</span></span>
<span class="line"><span style="color: #005CC5">slice</span><span style="color: #24292E">(start, stop) </span><span style="color: #6A737D"># 2</span></span>
<span class="line"><span style="color: #005CC5">slice</span><span style="color: #24292E">(start, stop, step) </span><span style="color: #6A737D"># 3</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>When the first form is used, only one input argument is supplied, the start is assumed to be 0 and the step is assumed to be 1.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>When the second form is used, two input arguments are supplied and the step is assumed to be 1.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The three forms above are normally represented using colon slicing notation which is more flexible:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":":stop # 1\nstart:stop # 2\nstart:stop:step # 3\n\n: # all\n:: # all\nstart: # start only\n::step # step only\nstart:: # start and step only","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:stop \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# 1\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estart:stop \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# 2\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estart:stop:step \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# 3\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e: \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# all\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:: \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# all\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estart: \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# start only\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e::step \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# step only\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estart:: \u003c/span\u003e\u003cspan style=\u0022color: #6A737D\u0022\u003e# start and step only\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code=":stop # 1
start:stop # 2
start:stop:step # 3

: # all
:: # all
start: # start only
::step # step only
start:: # start and step only" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">:stop </span><span style="color: #6A737D"># 1</span></span>
<span class="line"><span style="color: #24292E">start:stop </span><span style="color: #6A737D"># 2</span></span>
<span class="line"><span style="color: #24292E">start:stop:step </span><span style="color: #6A737D"># 3</span></span>
<span class="line"></span>
<span class="line"><span style="color: #24292E">: </span><span style="color: #6A737D"># all</span></span>
<span class="line"><span style="color: #24292E">:: </span><span style="color: #6A737D"># all</span></span>
<span class="line"><span style="color: #24292E">start: </span><span style="color: #6A737D"># start only</span></span>
<span class="line"><span style="color: #24292E">::step </span><span style="color: #6A737D"># step only</span></span>
<span class="line"><span style="color: #24292E">start:: </span><span style="color: #6A737D"># start and step only</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>For positive steps when a:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>start value is not specified it is assumed to be the default 0.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>stop value is not specified it is assumed to be the default len(string)</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>For a negative step when a:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>start value is not specified it is assumed to be the value before 0 which is -1</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>stop value is not specified it is assumed to be -len(string) - 1</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>To get the first and second word of greeting using slicing, the following slices are required:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello world!'\ngreeting[0:5]\ngreeting[6:11]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e0\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e6\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e11\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello world!'
greeting[0:5]
greeting[6:11]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span>
<span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">0</span><span style="color: #24292E">:</span><span style="color: #005CC5">5</span><span style="color: #24292E">]</span></span>
<span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">6</span><span style="color: #24292E">:</span><span style="color: #005CC5">11</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello'</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'world'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Slicing from the start, end and a copy of the string can be made using:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[:5]\ngreeting[6:]\ngreeting[:]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e6\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:]\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[:]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[:5]
greeting[6:]
greeting[:]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[:</span><span style="color: #005CC5">5</span><span style="color: #24292E">]</span></span>
<span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">6</span><span style="color: #24292E">:]</span></span>
<span class="line"><span style="color: #24292E">greeting[:]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello'</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'world!'</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Notice the inclusion of the last character at index 11 the '!' in 'World!'. To specify a slice that includes this character explicitly a stop value the length of the string needs to be used:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[6:12]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e6\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e12\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[6:12]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">6</span><span style="color: #24292E">:</span><span style="color: #005CC5">12</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Attempting to access this position gives an IndexError because zero-order indexing is used and the last index is therefore the length minus 1 which is 11:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[12]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e12\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[12]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">12</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>IndexError: string index out of range</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A step can be included to select every 2nd Unicode character. The starting position will dictate whether characters at even or odd indexes will be selected:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[:5:2]\ngreeting[1:5:2]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[:5:2]
greeting[1:5:2]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[:</span><span style="color: #005CC5">5</span><span style="color: #24292E">:</span><span style="color: #005CC5">2</span><span style="color: #24292E">]</span></span>
<span class="line"><span style="color: #24292E">greeting[</span><span style="color: #005CC5">1</span><span style="color: #24292E">:</span><span style="color: #005CC5">5</span><span style="color: #24292E">:</span><span style="color: #005CC5">2</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hlo'</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'el'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>When the step is negative and the start and stop are at their defaults, the string will be reversed:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[::-1]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[::\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e-\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[::-1]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[::</span><span style="color: #D73A49">-</span><span style="color: #005CC5">1</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'!dlrow olleh'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Care needs to be taken when using a reverse step as the start bound is still inclusive and the stop bound is still exclusive. The default value for the start bound becomes the value before <code>0</code> which is <code>-1</code>. The <code>stop</code> value becomes the negative length of the string <code>-1</code>:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting[-1:-13:-1]","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting[\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e-\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e-\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e13\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e:\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e-\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e]\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting[-1:-13:-1]" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting[</span><span style="color: #D73A49">-</span><span style="color: #005CC5">1</span><span style="color: #24292E">:</span><span style="color: #D73A49">-</span><span style="color: #005CC5">13</span><span style="color: #24292E">:</span><span style="color: #D73A49">-</span><span style="color: #005CC5">1</span><span style="color: #24292E">]</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'!dlrow olleh'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The string class doesn't have the data model identifier __reversed__ defined however because it is an ordered sequence the builtins function reversed can be used on a string instance to create a reversed iterator:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Init signature:  reversed(sequence, /)
Docstring:      Return a reverse iterator over the values of the given sequence.
Type:           type
Subclasses:</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"backward = reversed(greeting)\nbackward","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ebackward \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ereversed\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ebackward\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="backward = reversed(greeting)
backward" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">backward </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">reversed</span><span style="color: #24292E">(greeting)</span></span>
<span class="line"><span style="color: #24292E">backward</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;reversed at 0x1f166c2bdc0></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The builtins next works in a similar manner as seen before. Since the iterator is reversed, the last Unicode character in the string is displayed first and Unicode characters in the string are consumed backwards:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"next(backward)\nnext(backward)\nnext(backward)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(backward)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(backward)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003enext\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(backward)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="next(backward)
next(backward)
next(backward)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(backward)</span></span>
<span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(backward)</span></span>
<span class="line"><span style="color: #005CC5">next</span><span style="color: #24292E">(backward)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'!'
'd'
'l'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The numeric index has previously been used to retrieve the corresponding Unicode character at the respective numeric index. </p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"for num, letter in enumerate(greeting):\n    print(num, letter)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003efor\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e num, letter \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eenumerate\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting):\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(num, letter)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="for num, letter in enumerate(greeting):
    print(num, letter)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #D73A49">for</span><span style="color: #24292E"> num, letter </span><span style="color: #D73A49">in</span><span style="color: #24292E"> </span><span style="color: #005CC5">enumerate</span><span style="color: #24292E">(greeting):</span></span>
<span class="line"><span style="color: #24292E">    </span><span style="color: #005CC5">print</span><span style="color: #24292E">(num, letter)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>0 h
1 e
2 l
3 l
4 o
5  
6 w
7 o
8 r
9 l
10 d
11 !</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The index identifier instead retrieves the index corresponding to the first occurrence of a character or substring:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.index(sub[, start[, end]]) -> int

Return the lowest index in S where substring sub is found,
such that sub is contained within S[start:end].  Optional
arguments start and end are interpreted as in slice notation.

Raises ValueError when the substring is not found.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The letter 'l' occurs 3 times at the indexes 2, 3 and 9. To get the first value:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.index('l')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.index(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.index('l')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.index(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>2</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>To get the other index values, the start index value to restrict the search from needs to be added:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.index('l', 2+1)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.index(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.index('l', 2+1)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.index(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">, </span><span style="color: #005CC5">2</span><span style="color: #D73A49">+</span><span style="color: #005CC5">1</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>3</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.index('l', 3+1)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.index(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.index('l', 3+1)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.index(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">, </span><span style="color: #005CC5">3</span><span style="color: #D73A49">+</span><span style="color: #005CC5">1</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>9</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If a value is not found, a ValueError displays:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.index('l', 9+1)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.index(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e9\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.index('l', 9+1)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.index(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">, </span><span style="color: #005CC5">9</span><span style="color: #D73A49">+</span><span style="color: #005CC5">1</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>ValueError: substring not found</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A Unicode substring can also be searched for opposed to a Unicode character:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.index('world')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.index(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;world\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.index('world')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.index(</span><span style="color: #032F62">&#39;world&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>6</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The string also has a number of associated identifiers that are not part of the Sequence abstract base class. There is for example the closely associated method find which has analogous input arguments and returns the integer -1 when a value is not found instead of a ValueError:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.count(sub[, start[, end]]) -> int

Return the number of non-overlapping occurrences of substring sub in
string S[start:end].  Optional arguments start and end are
interpreted as in slice notation.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.find('l')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.find(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.find('l')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.find(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>2</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.find('l', 2+1)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.find(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e2\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.find('l', 2+1)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.find(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">, </span><span style="color: #005CC5">2</span><span style="color: #D73A49">+</span><span style="color: #005CC5">1</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>3</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.find('l', 3+1)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.find(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e3\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.find('l', 3+1)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.find(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">, </span><span style="color: #005CC5">3</span><span style="color: #D73A49">+</span><span style="color: #005CC5">1</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>9</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.find('l', 9+1)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.find(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e9\u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.find('l', 9+1)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.find(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">, </span><span style="color: #005CC5">9</span><span style="color: #D73A49">+</span><span style="color: #005CC5">1</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>-1</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There is an associated method right find rfind that begins searches from the right of the string instead of the left:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.rfind(sub[, start[, end]]) -> int

Return the highest index in S where substring sub is found,
such that sub is contained within S[start:end].  Optional
arguments start and end are interpreted as in slice notation.

Return -1 on failure.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.rfind('l')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.rfind(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;l\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.rfind('l')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.rfind(</span><span style="color: #032F62">&#39;l&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>9</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The string identifier startswith searches for a string prefix and returns a boolean value of True if present, otherwise returns a boolean value of False:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.startswith(prefix[, start[, end]]) -> bool

Return True if S starts with the specified prefix, False otherwise.
With optional start, test S beginning at that position.
With optional end, stop comparing S at that position.
prefix can also be a tuple of strings to try.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.startswith('hello')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.startswith(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.startswith('hello')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.startswith(</span><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The associated identifier endswith looks for a suffix:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Docstring:
S.endswith(suffix[, start[, end]]) -> bool

Return True if S ends with the specified suffix, False otherwise.
With optional start, test S beginning at that position.
With optional end, stop comparing S at that position.
suffix can also be a tuple of strings to try.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.endswith('!')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.endswith(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;!\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.endswith('!')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.endswith(</span><span style="color: #032F62">&#39;!&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The replace method can be used to replace an old substring old with a new substring new. It has an optional argument count which has a default value of -1 and this means it allows for all replacements by default. The / trailing the input arguments once again indicates that the input arguments are to be supplied positionally:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.replace(old, new, count=-1, /)
Docstring:
Return a copy with all occurrences of substring old replaced by new.

  count
    Maximum number of occurrences to replace.
    -1 (the default value) means replace all occurrences.

If the optional argument count is given, only the first count occurrences are
replaced.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.replace('hello', 'bye')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.replace(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;bye\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.replace('hello', 'bye')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.replace(</span><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;bye&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'bye world'</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="fill-center-and-justify">Fill, Center and Justify</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Supposing the following string is</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If greeting and the len of greeting are examined:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello world!'\nlen(greeting)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003elen\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(greeting)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello world!'
len(greeting)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span>
<span class="line"><span style="color: #005CC5">len</span><span style="color: #24292E">(greeting)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>12</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The center method can be used to center the string over a specified width using whitespace (default) or a specified fill character. Alternatively the ljust and rjust are used to left and right justify the string and have consistent input arguments. Note the / in the input arguments meaning they have to be specified positionally:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.center(width, fillchar=' ', /)
Docstring:
Return a centered string of length width.

Padding is done using the specified fill character (default is a space).
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.ljust(width, fillchar=' ', /)
Docstring:
Return a left-justified string of length width.

Padding is done using the specified fill character (default is a space).
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.rjust(width, fillchar=' ', /)
Docstring:
Return a right-justified string of length width.

Padding is done using the specified fill character (default is a space).
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.center(20)\ngreeting.center(20, '◯')\ngreeting.ljust(20, '◯')\ngreeting.rjust(20, '◯')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.center(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e20\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.center(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e20\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.ljust(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e20\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.rjust(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e20\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.center(20)
greeting.center(20, '◯')
greeting.ljust(20, '◯')
greeting.rjust(20, '◯')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting.center(</span><span style="color: #005CC5">20</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting.center(</span><span style="color: #005CC5">20</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting.ljust(</span><span style="color: #005CC5">20</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting.rjust(</span><span style="color: #005CC5">20</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'    hello world!    '
'◯◯◯◯hello world!◯◯◯◯'
'◯◯◯◯◯◯◯◯hello world!'
'hello world!◯◯◯◯◯◯◯◯'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If the following string is created:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting2 = greeting.center(20, '◯')\ngreeting2","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting.center(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e20\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting2 = greeting.center(20, '◯')
greeting2" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> greeting.center(</span><span style="color: #005CC5">20</span><span style="color: #24292E">, </span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting2</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'◯◯◯◯hello world!◯◯◯◯'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The opposite operation can be carried out using the identifiers lstrip and rstrip which left strip and right strip whitespace by default or a specified fill character or character sequence:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting2.lstrip(chars=None, /)
Docstring:
Return a copy of the string with leading whitespace removed.

If chars is given and not None, remove characters in chars instead.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting2.rstrip(chars=None, /)
Docstring:
Return a copy of the string with trailing whitespace removed.

If chars is given and not None, remove characters in chars instead.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting2.lstrip('◯')\ngreeting2.lstrip('◯').rstrip('◯')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2.lstrip(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2.lstrip(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e).rstrip(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting2.lstrip('◯')
greeting2.lstrip('◯').rstrip('◯')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting2.lstrip(</span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting2.lstrip(</span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">).rstrip(</span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello world!◯◯◯◯'
'hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There are the associated identifiers removeprefix and removesuffix that are more precise and will only remove a specified prefix or suffix:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting2.removeprefix(prefix, /)
Docstring:
Return a str with the given prefix string removed if present.

If the string starts with the prefix string, return string[len(prefix):].
Otherwise, return a copy of the original string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting2.removesuffix(suffix, /)
Docstring:
Return a str with the given suffix string removed if present.

If the string ends with the suffix string and that suffix is not empty,
return string[:-len(suffix)]. Otherwise, return a copy of the original
string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting2.removeprefix('◯◯◯')\ngreeting2.removesuffix('◯')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2.removeprefix(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯◯◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting2.removesuffix(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;◯\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting2.removeprefix('◯◯◯')
greeting2.removesuffix('◯')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">greeting2.removeprefix(</span><span style="color: #032F62">&#39;◯◯◯&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting2.removesuffix(</span><span style="color: #032F62">&#39;◯&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'◯hello world!◯◯◯◯'
'◯◯◯◯hello world!◯◯◯'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Earlier the binary number corresponding to the character 'a' was computed:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"bin(ord('a'))","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ebin\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;a\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e))\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="bin(ord('a'))" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">bin</span><span style="color: #24292E">(</span><span style="color: #005CC5">ord</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;a&#39;</span><span style="color: #24292E">))</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0b1100001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The string identifier removeprefix can be used to remove the '0b':</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"bin(ord('a')).removeprefix('0b')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ebin\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;a\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)).removeprefix(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;0b\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="bin(ord('a')).removeprefix('0b')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #005CC5">bin</span><span style="color: #24292E">(</span><span style="color: #005CC5">ord</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;a&#39;</span><span style="color: #24292E">)).removeprefix(</span><span style="color: #032F62">&#39;0b&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'1100001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There is also the string method zfill which can be used to zero fill a string and is mainly intended for strings of numeric values:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"lettera = bin(ord('a')).removeprefix('0b')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003elettera \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003ebin\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;a\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)).removeprefix(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;0b\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="lettera = bin(ord('a')).removeprefix('0b')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">lettera </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">bin</span><span style="color: #24292E">(</span><span style="color: #005CC5">ord</span><span style="color: #24292E">(</span><span style="color: #032F62">&#39;a&#39;</span><span style="color: #24292E">)).removeprefix(</span><span style="color: #032F62">&#39;0b&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:enlighter/codeblock {"language":"raw"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  lettera.zfill(width, /)
Docstring:
Pad a numeric string with zeros on the left, to fill a field of the given width.

The string is never truncated.
Type:      builtin_function_or_method
</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Since this is a byte, the width can be specified as 8, once again this is specified positionally as the input argument is followed by a /</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"lettera = lettera.zfill(8)\nlettera","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003elettera \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e lettera.zfill(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e8\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003elettera\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="lettera = lettera.zfill(8)
lettera" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">lettera </span><span style="color: #D73A49">=</span><span style="color: #24292E"> lettera.zfill(</span><span style="color: #005CC5">8</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">lettera</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'01100001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>In the above reassignment is used. Recall that the assignment operator should be approached from right to left, so the operation on the right should be calculated using the original string. After the zfill of the original string '1100001', there is a new string '01100001'. The instance name should be conceptualised as a label and before the reassignment points to the original string '1100001' and after the assignment points to the new string '01100001'.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading">Binary Operators</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The string is an ordered immutable Sequence as previously discussed. An immutable Sequence often has the data model identifiers addition __add__ and multiplication __mul__ which map to the operators + and * respectively. For a mutable sequence these perform the task of concatenation and replication with an integer respectively. The reverse multiplication __rmul__ is also typically defined which operates if the integer is multiplied by the string instead of the string multiplied by the integer giving the same result. Note that these data model identifiers alongside the previously examined __mod__ data model identifier which maps to the % operator have different behaviour in numeric data types where they instead behave differently and perform a numeric operation. The typical functionality of these data model identifiers is different for Sequences and numbers.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The __add__ data model identifier is called a binary operator as it requires the string instance <em>self</em> and the string instance value.</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       lettera.__add__(value, /)
Call signature:  lettera.__add__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__add__' of str object at 0x000001F166FEB6B0>
Docstring:      Return self+value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The binary prefix '0b' can be added to the string lettera:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'0b' + lettera","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;0b\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e lettera\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'0b' + lettera" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #032F62">&#39;0b&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">+</span><span style="color: #24292E"> lettera</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0b01100001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Note in the above that '0b' is the instance self and lettera is the instance value because '0b' is on the left hand side of the + operator. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The return value can be reassigned to lettera, recall that the operation on the right hand side of the assignment operator is carried out first and creates a new instance. Then the assignment of this new object to the instance name is carried out. The instance name be conceptualised as a label then initially pointed at the string '01100001' and now points to the new string '0b01100001':</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"lettera = '0b' + lettera\nlettera","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003elettera \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;0b\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e+\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e lettera\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003elettera\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="lettera = '0b' + lettera
lettera" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff"><code><span class="line"><span style="color: #24292E">lettera </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;0b&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">+</span><span style="color: #24292E"> lettera</span></span>
<span class="line"><span style="color: #24292E">lettera</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'0b01100001'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The __mul__ data model identifier defines how the * operator behaves:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__mul__(value, /)
Call signature:  greeting.__mul__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__mul__' of str object at 0x00000201D22435B0>
Docstring:      Return self*value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>For a string the __mul__ works with a string instance <em>self</em> and integer <em>value</em>. <em>self </em>should be at the left hand side of the multiplication operator.</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting * 3","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e*\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e3\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting * 3" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">*</span><span style="color: #24292E"> </span><span style="color: #005CC5">3</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello world!hello world!hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The data model identifier __rmul__ is also defined:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__rmul__(value, /)
Call signature:  greeting.__rmul__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__rmul__' of str object at 0x00000201D22435B0>
Docstring:      Return value*self.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>This defines the behaviour of the multiplication operator when the str is used to the right hand side of the multiplication operator and the integer instance is used to the left hand side of the multiplication operator:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"5 * greeting","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e*\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="5 * greeting" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #005CC5">5</span><span style="color: #24292E"> </span><span style="color: #D73A49">*</span><span style="color: #24292E"> greeting</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'hello world!hello world!hello world!hello world!hello world!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The use of __mod__ was seen before and required a string instance with % placeholders:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"stringbody = 'The numbers are %d, %.3e and %.3e.'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%d\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%.3e\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%.3e\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="stringbody = 'The numbers are %d, %.3e and %.3e.'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">%d</span><span style="color: #032F62">, </span><span style="color: #005CC5">%.3e</span><span style="color: #032F62"> and </span><span style="color: #005CC5">%.3e</span><span style="color: #032F62">.&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The __mod__ data model identifier controls the behaviour of the % operator and is a binary operation between a string and a tuple of corresponding placeholders:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       stringbody.__mod__(value, /)
Call signature:  stringbody.__mod__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__mod__' of str object at 0x00000201D22FE430>
Docstring:      Return self%value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"num1 = 1\nnum2 = 0.0000123456789\nnum3 = 12.3456789\n\nstringbody = 'The numbers are %d, %.3e and %.3e.'\nstringbody % (num1, num2, num3)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e1\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e0.0000123456789\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003enum3 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e12.3456789\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;The numbers are \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%d\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e, \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%.3e\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e and \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e%.3e\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e.\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003estringbody \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e%\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e (num1, num2, num3)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="num1 = 1
num2 = 0.0000123456789
num3 = 12.3456789

stringbody = 'The numbers are %d, %.3e and %.3e.'
stringbody % (num1, num2, num3)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">num1 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">1</span></span>
<span class="line"><span style="color: #24292E">num2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">0.0000123456789</span></span>
<span class="line"><span style="color: #24292E">num3 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">12.3456789</span></span>
<span class="line"></span>
<span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;The numbers are </span><span style="color: #005CC5">%d</span><span style="color: #032F62">, </span><span style="color: #005CC5">%.3e</span><span style="color: #032F62"> and </span><span style="color: #005CC5">%.3e</span><span style="color: #032F62">.&#39;</span></span>
<span class="line"><span style="color: #24292E">stringbody </span><span style="color: #D73A49">%</span><span style="color: #24292E"> (num1, num2, num3)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'The numbers are 1, 0.000 and 12.346.'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>It is common to use a binary operator and reassign the output to the instance name. Recall the operation on the right is carried out using the original string and then the instance name, which can be conceptualised as a label then points to the new object:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello world!'\ngreeting = greeting * 5","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e greeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e*\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello world!'
greeting = greeting * 5" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span>
<span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> greeting </span><span style="color: #D73A49">*</span><span style="color: #24292E"> </span><span style="color: #005CC5">5</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>This second line can be carried out using the equivalent binary in place operator:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello world!'\ngreeting *= 5","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello world!\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e*=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e5\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello world!'
greeting *= 5" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello world!&#39;</span></span>
<span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">*=</span><span style="color: #24292E"> </span><span style="color: #005CC5">5</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The second form more clearly denotes that the multiplication is carried out first to create a new string instance and then reassignment of the instance name to that new instance occurs. Recall that a string instance is immutable and cannot be modified once instantiated. </p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading">Binary Comparison Operators</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>When the object class is used to create instances:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance1 = object()\ninstance2 = object()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eobject\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance2 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eobject\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance1 = object()
instance2 = object()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">instance1 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">object</span><span style="color: #24292E">()</span></span>
<span class="line"><span style="color: #24292E">instance2 </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #005CC5">object</span><span style="color: #24292E">()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>Each instance is a unique object stored in a different memory location:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance1\ninstance2","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance1\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance2\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance1
instance2" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">instance1</span></span>
<span class="line"><span style="color: #24292E">instance2</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;object at 0x201d20293d0>
&lt;object at 0x201d2029410></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The operator is checks to see if two objects are the same object, i.e. are stored in the same memory location:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"object1 is object2\nobject1 is object1","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eobject1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eis\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e object2\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eobject1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eis\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e object1\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="object1 is object2
object1 is object1" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">object1 </span><span style="color: #D73A49">is</span><span style="color: #24292E"> object2</span></span>
<span class="line"><span style="color: #24292E">object1 </span><span style="color: #D73A49">is</span><span style="color: #24292E"> object1</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>False
True</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There are also two data model identifiers equals __eq__ and not equals __ne__ which check to see if two objects are equal or not equal to one another. These map to the equals operator == and != operator respectively. The equals operator == should not be confused with the assignment operator = seen previously:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       instance1.__eq__(value, /)
Call signature:  instance1.__eq__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__eq__' of object object at 0x00000201D20293D0>
Docstring:      Return self==value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       instance1.__ne__(value, /)
Call signature:  instance1.__ne__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__ne__' of object object at 0x00000201D20293D0>
Docstring:      Return self!=value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance1 == instance2\ninstance1 != instance2","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e==\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e instance2\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e!=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e instance2\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance1 == instance2
instance1 != instance2" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">instance1 </span><span style="color: #D73A49">==</span><span style="color: #24292E"> instance2</span></span>
<span class="line"><span style="color: #24292E">instance1 </span><span style="color: #D73A49">!=</span><span style="color: #24292E"> instance2</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>False
True</code></pre>
<!-- /wp:code -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"instance1 == instance1\ninstance1 != instance1","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e==\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e instance1\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003einstance1 \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e!=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e instance1\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="instance1 == instance1
instance1 != instance1" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">instance1 </span><span style="color: #D73A49">==</span><span style="color: #24292E"> instance1</span></span>
<span class="line"><span style="color: #24292E">instance1 </span><span style="color: #D73A49">!=</span><span style="color: #24292E"> instance1</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>True
False</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>There is a subtle difference between using is and is equal to but it is not observed in the object class which is basic.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Recall that a character in a string is ordinal:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"import string\nfor character in string.printable:\n    print(ord(character), repr(character), character)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003eimport\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e string\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003efor\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e character \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003ein\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e string.printable:\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e    \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eprint\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003eord\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(character), \u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003erepr\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e(character), character)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="import string
for character in string.printable:
    print(ord(character), repr(character), character)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #D73A49">import</span><span style="color: #24292E"> string</span></span>
<span class="line"><span style="color: #D73A49">for</span><span style="color: #24292E"> character </span><span style="color: #D73A49">in</span><span style="color: #24292E"> string.printable:</span></span>
<span class="line"><span style="color: #24292E">    </span><span style="color: #005CC5">print</span><span style="color: #24292E">(</span><span style="color: #005CC5">ord</span><span style="color: #24292E">(character), </span><span style="color: #005CC5">repr</span><span style="color: #24292E">(character), character)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>48 '0' 0
49 '1' 1
50 '2' 2
51 '3' 3
52 '4' 4
53 '5' 5
54 '6' 6
55 '7' 7
56 '8' 8
57 '9' 9
97 'a' a
98 'b' b
99 'c' c
100 'd' d
101 'e' e
102 'f' f
103 'g' g
104 'h' h
105 'i' i
106 'j' j
107 'k' k
108 'l' l
109 'm' m
110 'n' n
111 'o' o
112 'p' p
113 'q' q
114 'r' r
115 's' s
116 't' t
117 'u' u
118 'v' v
119 'w' w
120 'x' x
121 'y' y
122 'z' z
65 'A' A
66 'B' B
67 'C' C
68 'D' D
69 'E' E
70 'F' F
71 'G' G
72 'H' H
73 'I' I
74 'J' J
75 'K' K
76 'L' L
77 'M' M
78 'N' N
79 'O' O
80 'P' P
81 'Q' Q
82 'R' R
83 'S' S
84 'T' T
85 'U' U
86 'V' V
87 'W' W
88 'X' X
89 'Y' Y
90 'Z' Z
33 '!' !
34 '"' "
35 '#' #
36 '$' $
37 '%' %
38 '&amp;' &amp;
39 "'" '
40 '(' (
41 ')' )
42 '*' *
43 '+' +
44 ',' ,
45 '-' -
46 '.' .
47 '/' /
58 ':' :
59 ';' ;
60 '&lt;' &lt;
61 '=' =
62 '>' >
63 '?' ?
64 '@' @
91 '&#91;' &#91;
92 '\\' \
93 ']' ]
94 '^' ^
95 '_' _
96 '`' `
123 '{' {
124 '|' |
125 '}' }
126 '~' ~
32 ' '  
9 '\t' 	
10 '\n' 

13 '\r' 
11 '\x0b' 
12 '\x0c' 
​</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Because each of these characters is ordinal, the string class redefines the operators __eq__ and __ne__ which recall map to == and !=:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__eq__(value, /)
Call signature:  greeting.__eq__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__eq__' of str object at 0x00000201D22435B0>
Docstring:      Return self==value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__ne__(value, /)
Call signature:  greeting.__ne__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__ne__' of str object at 0x00000201D22435B0>
Docstring:      Return self!=value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The string class also has four other ordinal based comparison data model identifiers less than __lt__, greater than __gt__, less than or equal to __le__ and greater than or equal to __ge__ which map to &lt;, >, &lt;= and >= respectively:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__lt__(value, /)
Call signature:  greeting.__lt__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__lt__' of str object at 0x00000201D22435B0>
Docstring:      Return self&lt;value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__gt__(value, /)
Call signature:  greeting.__gt__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__gt__' of str object at 0x00000201D22435B0>
Docstring:      Return self>value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__le__(value, /)
Call signature:  greeting.__le__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__le__' of str object at 0x00000201D22435B0>
Docstring:      Return self&lt;=value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:       greeting.__ge__(value, /)
Call signature:  greeting.__ge__(*args, **kwargs)
Type:           method-wrapper
String form:    &lt;method-wrapper '__ge__' of str object at 0x00000201D22435B0>
Docstring:      Return self>=value.</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"'hello' == 'Hello'\n'hello' != 'Hello'\n'hello' \u003e 'Hello'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e==\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e!=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e\u0026gt;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;Hello\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="'hello' == 'Hello'
'hello' != 'Hello'
'hello' &gt; 'Hello'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">==</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Hello&#39;</span></span>
<span class="line"><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">!=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Hello&#39;</span></span>
<span class="line"><span style="color: #032F62">&#39;hello&#39;</span><span style="color: #24292E"> </span><span style="color: #D73A49">&gt;</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;Hello&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>False
True
True</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2 class="wp-block-heading">Splitting and Joining Strings</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The string has a number of identifiers which are used for splitting and joining a string. These generally involve casting to a Python collection such as a tuple of strings or a list of strings. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For example the identifier partition and right partition rpartition will partition a string into a three element tuple containing the substring before the partition, the partition substring and the substring after the partition respectively. To make it more obvious the following string will be instantiated:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting = 'hello|world|!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;hello|world|!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting = 'hello|world|!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">greeting </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;hello|world|!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.partition(sep, /)
Docstring:
Partition the string into three parts using the given separator.

This will search for the separator in the string.  If the separator is found,
returns a 3-tuple containing the part before the separator, the separator
itself, and the part after it.

If the separator is not found, returns a 3-tuple containing the original string
and two empty strings.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  greeting.rpartition(sep, /)
Docstring:
Partition the string into three parts using the given separator.

This will search for the separator in the string, starting at the end. If
the separator is found, returns a 3-tuple containing the part before the
separator, the separator itself, and the part after it.

If the separator is not found, returns a 3-tuple containing two empty strings
and the original string.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"greeting.partition('|')\ngreeting.rpartition('|')","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.partition(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;|\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003egreeting.rpartition(\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;|\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="greeting.partition('|')
greeting.rpartition('|')" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">greeting.partition(</span><span style="color: #032F62">&#39;|&#39;</span><span style="color: #24292E">)</span></span>
<span class="line"><span style="color: #24292E">greeting.rpartition(</span><span style="color: #032F62">&#39;|&#39;</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>('hello', '|', 'world|!')
greeting.rpartition('|')</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>More generally the split and join identifiers can be used to split a string into a list of strings or join a list of strings up into a single string. For example if the following sentence is created:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"sentence = 'the fat black cat sat on the mat!'","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003esentence \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;the fat black cat sat on the mat!\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="sentence = 'the fat black cat sat on the mat!'" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">sentence </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;the fat black cat sat on the mat!&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The identifier split can be examined:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  sentence.split(sep=None, maxsplit=-1)
Docstring:
Return a list of the substrings in the string, using sep as the separator string.

  sep
    The separator used to split the string.

    When set to None (the default value), will split on any whitespace
    character (including \\n \\r \\t \\f and spaces) and will discard
    empty strings from the result.
  maxsplit
    Maximum number of splits (starting from the left).
    -1 (the default value) means no limit.

Note, str.split() is mainly useful for data that has been intentionally
delimited.  With natural text that includes punctuation, consider using
the regular expression module.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>Since the values to be split from are whitespace, the input arguments can be left unspecified defaulting to their default values. This gives a list of strings:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"words = sentence.split()\nwords","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ewords \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e sentence.split()\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003ewords\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="words = sentence.split()
words" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">words </span><span style="color: #D73A49">=</span><span style="color: #24292E"> sentence.split()</span></span>
<span class="line"><span style="color: #24292E">words</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&#91;'the', 'fat', 'black', 'cat', 'sat', 'on', 'the', 'mat!']</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>To join the words a delimiterstring needs to be can created for example a space:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"delimiterstring = ' '","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003edelimiterstring \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39; \u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="delimiterstring = ' '" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">delimiterstring </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39; &#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  delimiterstring.join(iterable, /)
Docstring:
Concatenate any number of strings.

The string whose method is called is inserted in between each given string.
The result is returned as a new string.

Example: '.'.join(['ab', 'pq', 'rs']) -> 'ab.pq.rs'
Type:      builtin_function_or_method
​</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The join method can be used on this delimiter string and the list of strings can be supplied as the iterable:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"delimiterstring.join(words)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003edelimiterstring.join(words)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="delimiterstring.join(words)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">delimiterstring.join(words)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'the fat black cat sat on the mat!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>More generally this is called from a space itself:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"' '.join(words)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39; \u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e.join(words)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="' '.join(words)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #032F62">&#39; &#39;</span><span style="color: #24292E">.join(words)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'the fat black cat sat on the mat!'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>If a multiline string is created:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph = '''The quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\n'''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;The quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph = '''The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
The quick brown fox jumps over the lazy dog
'''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">paragraph </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;&#39;&#39;The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">&#39;&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>There is an associated identifier split, which splits the string into a list using the newline. It has an input argument keepends which defaults to False and therefor excludes the newline character:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  paragraph.splitlines(keepends=False)
Docstring:
Return a list of the lines in the string, breaking at line boundaries.

Line breaks are not included in the resulting list unless keepends is given and
true.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>This can be used to get a list of sentences:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph.splitlines()","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph.splitlines()\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph.splitlines()" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">paragraph.splitlines()</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&#91;'The quick brown fox jumps over the lazy dog',
 'The quick brown fox jumps over the lazy dog',
 'The quick brown fox jumps over the lazy dog',
 'The quick brown fox jumps over the lazy dog']</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>A multiline string can be created with tabs:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph = '''\\tThe quick brown fox jumps over the lazy dog\n\\tThe quick brown fox jumps over the lazy dog\n\\tThe quick brown fox jumps over the lazy dog\n\\tThe quick brown fox jumps over the lazy dog\n'''","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph \u003c/span\u003e\u003cspan style=\u0022color: #D73A49\u0022\u003e=\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e \u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\t\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\t\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\t\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e\\t\u003c/span\u003e\u003cspan style=\u0022color: #032F62\u0022\u003eThe quick brown fox jumps over the lazy dog\u003c/span\u003e\u003c/span\u003e\n\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #032F62\u0022\u003e\u0026#39;\u0026#39;\u0026#39;\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph = '''\tThe quick brown fox jumps over the lazy dog
\tThe quick brown fox jumps over the lazy dog
\tThe quick brown fox jumps over the lazy dog
\tThe quick brown fox jumps over the lazy dog
'''" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">paragraph </span><span style="color: #D73A49">=</span><span style="color: #24292E"> </span><span style="color: #032F62">&#39;&#39;&#39;</span><span style="color: #005CC5">\t</span><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #005CC5">\t</span><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #005CC5">\t</span><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #005CC5">\t</span><span style="color: #032F62">The quick brown fox jumps over the lazy dog</span></span>
<span class="line"><span style="color: #032F62">&#39;&#39;&#39;</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:paragraph -->
<p>The tabs can be replaced by a specified number of spaces using the expandtabs identifier:</p>
<!-- /wp:paragraph -->

<!-- wp:enlighter/codeblock {"language":"raw","linenumbers":"false"} -->
<pre class="EnlighterJSRAW" data-enlighter-language="raw" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="false" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Signature:  paragraph.expandtabs(tabsize=8)
Docstring:
Return a copy where all tab characters are expanded using spaces.

If tabsize is not given, a tab size of 8 characters is assumed.
Type:      builtin_function_or_method</pre>
<!-- /wp:enlighter/codeblock -->

<!-- wp:paragraph -->
<p>The tabs can be expanded by 4 spaces using:</p>
<!-- /wp:paragraph -->

<!-- wp:kevinbatdorf/code-block-pro {"code":"paragraph.expandtabs(4)","codeHTML":"\u003cpre class=\u0022shiki github-light\u0022 style=\u0022background-color: #fff\u0022 tabindex=\u00220\u0022\u003e\u003ccode\u003e\u003cspan class=\u0022line\u0022\u003e\u003cspan style=\u0022color: #24292E\u0022\u003eparagraph.expandtabs(\u003c/span\u003e\u003cspan style=\u0022color: #005CC5\u0022\u003e4\u003c/span\u003e\u003cspan style=\u0022color: #24292E\u0022\u003e)\u003c/span\u003e\u003c/span\u003e\u003c/code\u003e\u003c/pre\u003e","language":"python","theme":"github-light","bgColor":"#fff","textColor":"#24292e","fontSize":".875rem","lineHeight":"1.25rem","headerType":"headlights","seeMoreString":"","seeMoreAfterLine":"","seeMoreTransition":false,"lineHighlightColor":"rgba(16, 41, 67, 0.2)","copyButton":true} -->
<div class="wp-block-kevinbatdorf-code-block-pro" style="font-size:.875rem;line-height:1.25rem"><span style="display:block;padding:16px 0 0 16px;margin-bottom:-1px;width:100%;text-align:left;background-color:#fff"><svg xmlns="http://www.w3.org/2000/svg" width="54" height="14" viewBox="0 0 54 14"><g fill="none" fill-rule="evenodd" transform="translate(1 1)"><circle cx="6" cy="6" r="6" fill="#FF5F56" stroke="#E0443E" stroke-width=".5"></circle><circle cx="26" cy="6" r="6" fill="#FFBD2E" stroke="#DEA123" stroke-width=".5"></circle><circle cx="46" cy="6" r="6" fill="#27C93F" stroke="#1AAB29" stroke-width=".5"></circle></g></svg></span><span role="button" tabindex="0" data-code="paragraph.expandtabs(4)" style="color:#24292e;display:none" aria-label="Copy" class="code-block-pro-copy-button"><svg xmlns="http://www.w3.org/2000/svg" style="width:24px;height:24px" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path class="with-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path><path class="without-check" stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg></span><pre class="shiki github-light" style="background-color: #fff" tabindex="0"><code><span class="line"><span style="color: #24292E">paragraph.expandtabs(</span><span style="color: #005CC5">4</span><span style="color: #24292E">)</span></span></code></pre></div>
<!-- /wp:kevinbatdorf/code-block-pro -->

<!-- wp:code -->
<pre class="wp-block-code"><code>'    The quick brown fox jumps over the lazy dog\n    The quick brown fox jumps over the lazy dog\n    The quick brown fox jumps over the lazy dog\nThe quick brown fox jumps over the lazy dog\n'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>This concludes the overview of the string class, further related concepts will be explored with the byte class in the next tutorial.</p>
<!-- /wp:paragraph -->