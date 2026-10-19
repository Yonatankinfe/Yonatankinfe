# ═══════════════════════════════════════════════════════════════════
#  THE SNAKE PROTOCOL — auto-regenerating contribution snake
#
#  ONE-TIME SETUP (~2 minutes):
#  1. Go to your profile repo:  github.com/Yonatankinfe/Yonatankinfe
#  2. Create the path  .github/workflows/  and save this file
#     there as  snake.yml
#  3. Open the "Actions" tab → enable workflows if prompted
#  4. Select "Generate Snake" (left sidebar) → "Run workflow"
#     → branch: main → click "Run workflow"
#  5. Wait ~1 minute — an "output" branch appears with the SVGs
#     and the snake in your README comes alive.
#
#  It then re-runs automatically every 6 hours to keep the
#  snake fed with your latest commits.
# ═══════════════════════════════════════════════════════════════════

name: Generate Snake

on:
  schedule:
    - cron: "0 */6 * * *" # regenerate every 6 hours
  workflow_dispatch: # allows manual runs anytime

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 10

    steps:
      # Generates a snake game from the contribution graph,
      # eating cells in order of contribution levels.
      - name: Generate snake SVGs
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      # Pushes the generated SVGs to the "output" branch.
      - name: Push snake to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
