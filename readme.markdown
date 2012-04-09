=== HumansNotBots - Easy, Accessible Email Cloaker ===

"email AT address DOT com" (without quotes) is converted to a clickable version of email@address.com if JavaScript is enabled.

== Description ==

This email cloaking method: 

* is accessible for people browsing with screen readers (e.g., blind people); 
* degrades gracefully for browsers without JavaScript; 
* works just like a normal, clickable email address for browsers with JavaScript enabled; and
* requires no shortcodes.

Email addresses in the form `email AT address DOT com` are converted to a clickable version, [email@address.com](mailto:email@address.com), if JavaScript is enabled. If JavaScript is not enabled (such as for screen readers), then the email address in the form `email AT address DOT com` is still readable to humans.


== Frequently Asked Questions ==

= Won't email scrapers figure out email addresses in the form `email AT address DOT com`? =

In a test comparing the [effectiveness of different obfuscation methods](http://techblog.tilllate.com/2008/07/20/ten-methods-to-obfuscate-e-mail-addresses-compared/) in 2008, the obfuscation method "Using ATs and DOTs" received much less spam than "Replacing @ and . with Entities". Assuming that the 2008 test is an accurate model, this plugin should reduce over 99% of spam without compromising accessibility.

"CSS display: none" should *not* be used, because screen readers cannot read content styled with `display: none` either. Reversing email addresses and using ROT-13 encryption are obviously not accessible, either.

= Do email addresses that end with ".ca" or ".info" work? =

Yes. Any email address with a TLD (top-level domain) of two, three, or four characters would work.

= Do email addresses that end with "co.uk" work? =

Yes. Use the form `user AT somewhere.co DOT uk`.

== Advanced ==

If you want to use a non-English language, use the translated strings of "AT" and "DOT" as parameters of the HumansNotBots function. For example, for Italian, you can use

    HumansNotBots('PRESSO', 'PUNTO');
