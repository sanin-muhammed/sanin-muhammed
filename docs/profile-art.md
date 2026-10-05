# Profile art

Layout and SVG generators adapted from Avi Vashishta’s tutorial and profile repository at commit 73b3fe8c6705ab1a70c4d5e2098d52f4ce8e2d3e.

Reference: https://www.avivashishta.com/blog/build-animated-github-profile-readme
Source: https://github.com/AVIVASHISHTA29/AVIVASHISHTA29

The README matches the article’s contribution-first layout, rather than the author’s later wordmark layout. The portrait is converted from Sanin’s uploaded illustrated avatar. Transparent areas are composited onto white before grayscale ASCII conversion; the source aspect ratio is preserved.

Edit scripts/make_info_card.py then run python scripts/make_info_card.py to change details. To regenerate the portrait install Pillow, then run python scripts/make_ascii_svg.py. STATIC=1 emits a frozen SVG for inspection; omit it for published assets.

The daily workflow fetches the public contribution calendar and regenerates the graph. No personal access token is required. GitHub’s automatic GITHUB_TOKEN commits the updated files. Failed or unparseable fetches preserve the last successful graph.
