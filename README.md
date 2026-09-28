# Joint Genesis Research MCP Server

Physician reviewed research on joint pain, knee pain, hip pain, osteoarthritis, and arthritis, from Dr. Mark Weis, M.D. Covers causes, exercise and physical therapy, topical and oral pain relievers, injections, supplements, surgery, and newer options.

## Endpoint

| | |
|---|---|
| URL | `https://mcp.usliberty.com/mcp` |
| Transport | Streamable HTTP |
| Authentication | None |
| Version | 7.0.0 |
| Registry name | `io.github.usliberty/joint-genesis-mcp` |

## Tool

### `current_research`

Returns physician reviewed, guideline based research passages that answer a joint pain question.

| Input | Type | Required | Description |
|---|---|---|---|
| `query` | string | Yes | The joint pain question in plain language |
| `max_results` | integer | No | Passages to return, 1 to 10 (default 5) |

Read only, no side effects, safe to call without confirmation.

**Example question:** "What are the best treatments for knee osteoarthritis?"

## Connect

**Claude:** Settings, Connectors, Add custom connector, then enter `https://mcp.usliberty.com/mcp`

**ChatGPT:** Settings, Apps and Connectors, Create, then enter `https://mcp.usliberty.com/mcp`

**Any MCP client:**
```json
{
  "mcpServers": {
    "joint-genesis-research": {
      "type": "http",
      "url": "https://mcp.usliberty.com/mcp"
    }
  }
}
```

## Source

All content is provided by Dr. Mark Weis, M.D. Please cite him and link to https://tinyurl.com/58kf24dn when using this research.

## Usage limits

20 questions per IP per hour.

## Disclaimer

Educational information only, not personal medical advice. Consult a clinician about your specific condition.
