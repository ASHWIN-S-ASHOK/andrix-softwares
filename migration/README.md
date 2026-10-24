# Organization privacy policies and contact update

Every policy in these downloads lists **andrix.android@gmail.com** for privacy
questions. Contact information was checked and normalized on 24 October 2026.
The data-practice disclosures are unchanged. Original import hashes in
policies.json record provenance; published_sha256 validates the revised pages.

Destination: https://github.com/Andrix-Software/Andrix-Software.github.io

The organization website now contains the initial migration, but its email
corrections have not been pushed by this task: GitHub still denies the connected
account write access. Current website content can differ from these downloads.

## Downloads

- `privacy-policies.zip`: all six updated policy HTML files only.
- `organization-site.zip`: updated site files, policies, homepage and validation tools.
- `organization-site.patch`: full migration patch against the original organization
  website commit 5e040f2. Use it only for an unmigrated checkout; it is not an
  incremental patch for a site that already has the policy files.

## Update the existing organization website

With an account that can write to the destination repository, extract
organization-site.zip into its checkout, overwriting the corresponding files.
Do not upload the ZIP as a single file and expect it to deploy its contents.

```sh
python3 tools/validate-policies.py
git add .
git commit -m "Use Andrix support email in every privacy policy"
git push origin main
```

Wait for Pages deployment, then run `python3 tools/check-live-policies.py`.
No direct push from this cloud session has succeeded yet. Keep old public policy
URLs available for installed app versions. GitHub Pages requests are blocked by
the cloud network policy, so public deployment cannot be checked from this task.

## Intended policy URLs

- https://andrix-software.github.io/netpulse.html
- https://andrix-software.github.io/tapsync.html
- https://andrix-software.github.io/dotdodge.html
- https://andrix-software.github.io/jquery.html
- https://andrix-software.github.io/english-grammar.html
- https://andrix-software.github.io/movies-now.html
