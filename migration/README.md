# Organization privacy-policy migration

Destination: https://github.com/Andrix-Software/Andrix-Software.github.io

The destination changes are prepared and locally validated, but the connected
GitHub account `ASHWIN-S-ASHOK` was denied write access to that repository.
**The organization site has not been updated by this migration yet.**
The current personal policy pages and their links remain unchanged.

## Files

- `organization-site.zip`: the ready-to-publish static site files. Extract it;
  uploading the ZIP itself does not deploy its contents.
- `organization-site.patch`: the equivalent Git patch, including the organization
  homepage updates and all six policy pages.

The original policy wording, effective dates and individual contact addresses are
preserved. Existing app-ads.txt publisher information is preserved. NetPulse,
TapSync and Dot Dodge use the latest personal-site versions, rather than older
app-repository snapshots. jQuery and English Grammar come from their app repos;
Movies Now comes from its existing policy site. Exact sources and import hashes
are recorded in policies.json.

## Apply with an account that can write to the organization repository

Download organization-site.patch to a local path, then run:

```sh
git clone https://github.com/Andrix-Software/Andrix-Software.github.io.git
cd Andrix-Software.github.io
git apply --check /path/to/organization-site.patch
git apply /path/to/organization-site.patch
python3 tools/validate-policies.py --verify-imports
git add .
git commit -m "Centralize app privacy policies on the organization website"
git push origin main
```

Alternatively, extract the ZIP and upload its contents to the destination repo,
including the new policy pages and the updated index.html. Keep app-ads.txt at
the site root. If necessary, enable GitHub Pages from main / (root).

After Pages deployment completes, run `python3 tools/check-live-policies.py`.
Only then update Play Console and in-app links. Keep the old pages readable for
installed app versions. The old index can link to the organization site's
privacy.html catalogue after those checks pass.

## Intended public addresses after deployment

- https://andrix-software.github.io/netpulse.html
- https://andrix-software.github.io/tapsync.html
- https://andrix-software.github.io/dotdodge.html
- https://andrix-software.github.io/jquery.html
- https://andrix-software.github.io/english-grammar.html
- https://andrix-software.github.io/movies-now.html

GitHub Pages requests are blocked by the cloud environment's current network
policy, so public deployment cannot be confirmed from this task. Local HTML,
import hashes, links and 320/390/1024px homepage layouts were verified.
