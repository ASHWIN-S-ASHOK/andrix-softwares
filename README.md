# App privacy policies

Public privacy policies for Android apps developed by Ashwin S Ashok. The static HTML pages are published through GitHub Pages from this repository.

- [NetPulse](https://ashwin-s-ashok.github.io/access-privacy-policies/netpulse.html)
- [TapSync](https://ashwin-s-ashok.github.io/access-privacy-policies/tapsync.html)
- [Dot Dodge](https://ashwin-s-ashok.github.io/access-privacy-policies/dotdodge.html)

When an app changes SDKs or data practices, review its policy against the actual implementation and update the revision date. Keep the app's privacy link and Google Play listing pointed to the same public page. App-specific audience, consent, SDK retention, and Google Play Data safety declarations must match the shipped configuration.

## Authorized ad sellers

[app-ads.txt](https://ashwin-s-ashok.github.io/access-privacy-policies/app-ads.txt) declares the Google AdMob publisher used by TapSync.

AdMob discovers this file at the root of the developer website hostname, ignoring the path in the Play Store website URL. Publishing it in this project repository alone does not complete verification: `https://ashwin-s-ashok.github.io/app-ads.txt` must also serve this content (or an HTTP redirect to it). On GitHub Pages, publish the same file in the user-site repository `ASHWIN-S-ASHOK.github.io`. An HTML or JavaScript redirect is not sufficient.

Keep both copies synchronized. Set the app's developer website in the Play Store listing to the public website, then request another check in AdMob after the root URL is live. See [Google's setup instructions](https://support.google.com/admob/answer/9363762).
