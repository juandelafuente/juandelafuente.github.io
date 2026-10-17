---
title: "Getting your Python package version"
pubDate: 2021-12-20
---

<p>While debugging, deployment or during your DevSecOps strategy you want to print, write to a log, or whatever, your package version.</p><p>I have been dealing with this stuff for long, and I’m typically using the next approach using <strong>pkg_resources</strong>:</p><script src="https://gist.github.com/juandelafuente/2a912122a431846f77b08901d4f1a9ae.js"></script><p>The package is expected to be installed using a <strong>setup.py</strong> containing name value as <strong>mysamplepackage</strong> in this example.</p><p>Remember to import pkg_resources in order to use this function.</p><pre>import pkg_resources</pre><p>You can also use, for <em>modern</em> Python versions, distribution functions from importlib_metadata package</p><pre> from importlib_metadata import distribution</pre><p>It works in a similar way so the code would be</p><script src="https://gist.github.com/juandelafuente/93768d74527c2dee319d81c5531d691d.js"></script><p>What’s your way? More on <a href="https://twitter.com/jdelafuente">https://twitter.com/jdelafuente</a></p>
