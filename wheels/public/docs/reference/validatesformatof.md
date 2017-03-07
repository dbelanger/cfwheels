```coldfusion
<span class="cm-s-neo"><span class="cm-comment">// Make sure that the user has entered a correct credit card</span> <span class="cm-variable">validatesFormatOf</span>(<span class="cm-variable">property</span><span class="cm-operator">=</span><span class="cm-string">"cc"</span>, <span class="cm-variable">type</span><span class="cm-operator">=</span><span class="cm-string">"creditcard"</span>); <span class="cm-comment">/*</span> <span class="cm-comment"> * Make sure that the user has entered an email address ending with the</span> <span class="cm-comment"> * `.se` domain when the `ipCheck()` method returns `true`, and it's not</span> <span class="cm-comment"> * Sunday. Also supply a custom error message that overrides the CFWheels</span> <span class="cm-comment"> * default one</span> <span class="cm-comment"> */</span> <span class="cm-variable">validatesFormatOf</span>( <span class="cm-variable">property</span><span class="cm-operator">=</span><span class="cm-string">"email"</span>, <span class="cm-variable">regEx</span><span class="cm-operator">=</span><span class="cm-string">"^.*@.*\.se$"</span>, <span class="cm-variable">condition</span><span class="cm-operator">=</span><span class="cm-string">"ipCheck()"</span>, <span class="cm-variable">unless</span><span class="cm-operator">=</span><span class="cm-string">"DayOfWeek() eq 1"</span> <span class="cm-variable">message</span><span class="cm-operator">=</span><span class="cm-string">"Sorry, you must have a Swedish email address to use this website."</span> );</span>
```