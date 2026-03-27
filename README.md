# Bug Triager

A [Valet](https://valet.dev) agent that triages Sentry alerts. Classifies each alert by severity, reviews source code for context via GitHub, and opens or updates a Linear ticket with a diagnosis.

## Prerequisites
- A [Sentry](https://sentry.io) internal integration with a client secret and access token
- A [Linear](https://linear.app) personal API key
- A [GitHub](https://github.com) PAT with repo read scope

<table>
  <tr>
    <td><strong>CHANNELS</strong></td>
    <td><code>sentry-webhook</code></td>
  </tr>
  <tr>
    <td><strong>CONNECTORS</strong></td>
    <td><code>sentry-mcp</code> <code>linear-mcp</code> <code>github-mcp</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <br />
      <a href="https://dashboard.valet.dev/setup/configure?from=github.com/valet-agents/bug-triager">
        <img src="https://raw.githubusercontent.com/valet-agents/bug-triager/main/.github/deploy-button.svg" alt="Deploy Agent →" height="40" />
      </a>
      <br /><br />
    </td>
  </tr>
</table>
