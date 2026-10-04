# Codeboard Agent Plugin

Free skills for drawing, storyboarding, and 2D animation with [Codeboard](https://codeboard.nonom.xyz). No Nonom account or Suporter subscription is required. Your agent provider may charge separately.

Plugin version: **0.2.0**. Bundled engine references: **0.2.1**.

## Install

Install the [Codeboard engine](https://codeboard.nonom.xyz/docs/install/) first and verify `codeboard --version`. The engine and FFmpeg are not bundled in this plugin.

For Codex with plugin support:

```sh
codex plugin marketplace add https://art.nonom.xyz/api/registry/git/codeboard.git
codex plugin add codeboard@nonom-codeboard
```

For Claude Code:

```sh
claude plugin marketplace add https://art.nonom.xyz/api/registry/git/codeboard.git
claude plugin install codeboard@nonom-codeboard
```

This public repository is also a standalone marketplace: use `https://github.com/nonomnonom/codeboard-plugin.git` in place of the registry URL above.

Start a new agent session in your artwork folder. Ask it to use Codeboard to draw one editable panel, render and inspect it, and keep both the script and `.cboard` project.

## Included skills

`codeboard`, `codeboard-draw`, `codeboard-brushes`, `codeboard-storyboard`, `codeboard-animate`, `codeboard-camera`, `codeboard-audio`, `codeboard-revise`, `codeboard-review`, and `codeboard-debug`.

The package contains skill instructions, manuals, API references, and example source. It has no MCP server or hooks. Agent file access and CLI execution follow the host session's permissions.

## Source and verification

Authored in the `plugin/` directory of [Codeboard](https://github.com/nonomnonom/codeboard). This dedicated repository distributes only the plugin. Update the source manuals and regenerate the reference bundle in the engine project before publishing a new version; do not hand-edit generated references here.

The source package passes `npm run check:plugin`, including checks of ten skills and forty bundled reference files. Package validation does not establish full host compatibility. Claude host installation and automatic skill selection have not been verified.

MIT license for code and instructions; see [LICENSE](LICENSE). Original example artwork and synthesized audio are CC0; see [NOTICE](NOTICE).
