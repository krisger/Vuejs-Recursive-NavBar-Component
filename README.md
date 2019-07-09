# Vuejs NavBar, List recuresive component

<h2>About</h2>
<p>Recursive NavBar component can be used to create dynamic navigation bar in website</p>
<p>How to use is visible in App.vue file </p>
<p>After importing component to your vue file you need pass data to:</p>
<p>NavBar navbar element with attribute :list="data"></NavBar></p>

<p>Under you can see in which format pass json data to component with :list attribute</p>
<pre lang="no-highlight">
<code>
[
	{
	  name: "one",
	  id: 1,
	  level: 0,
	  href: "/one",
	  childItems: [
		{
		  name: "onefirstchild",
		  id: 10,
		  href: "/onefirstchild",
		  level: 1,
		  childItems: [{ 
			name: "onefirstsubchild", level: 2 }]
		},
		{
		  name: "onesecondchild",
		  id: 11,
		  href: "/onesecondchild",
		  level: 1
		}
	  ]
	},
	{
	  name: "two",
	  level: 0,
	  id: 2,
	  href: "/two"
	}
]
</code>
</pre>

<h2><a id="user-content-license" class="anchor" aria-hidden="true" href="#license"></a>License</h2>
<p>This project is licensed under the MIT License - for this read License.md file</p>