# Suparank MCP Server Setup

## Overview

This document describes the Suparank MCP (Model Context Protocol) server configuration for Claude Code.

## Configuration

The Suparank MCP server has been configured at: `/root/.config/claude-code/config.json`

### Configuration Details

```json
{
  "mcpServers": {
    "suparank": {
      "command": "npx",
      "args": ["suparank"],
      "env": {
        "SUPARANK_API_KEY": "sk_live_xxxxx...",
        "GEMINI_API_KEY": "AIzaSyxxxx..."
      }
    }
  }
}
```

**Note**: The actual API keys have been configured in the file at `/root/.config/claude-code/config.json`

## Available Tools

Once Claude Code restarts, the following Suparank tools will be available:

### 1. **seo_strategy**
Create comprehensive SEO strategy and content brief
- Auto-detects search intent from keyword
- Creates detailed content briefs for writers
- Suggests optimal word count and structure

### 2. **keyword_research**
Conduct keyword research and competitive analysis
- Analyzes search volume, difficulty, and opportunity
- Creates keyword clusters
- Identifies content opportunities

### 3. **topical_map**
Design pillar-cluster content architecture for topical authority
- Creates content hierarchy
- Suggests internal linking strategy
- Available depths: 1 (quick), 2 (standard), 3 (full)

### 4. **content_calendar**
Create editorial calendar and publication schedule
- Supports week, month, or quarter planning periods
- Aligns with project keywords and niche

### 5. **content_write**
Write comprehensive, SEO-optimized blog articles
- Creates engaging content with proper structure
- Includes internal links and semantic optimization
- Uses project brand voice by default

### 6. **image_prompt**
Create optimized prompts for AI image generation (Gemini)
- Designs prompts for hero images, diagrams, and illustrations
- Integrated with Gemini API for image generation

### 7. **internal_links**
Develop strategic internal linking plan
- Analyzes existing content
- Identifies linking opportunities
- Improves site architecture

### 8. **geo_optimize**
Optimize content for AI search engines (ChatGPT, Google SGE, Perplexity)
- Implements GEO (Generative Engine Optimization) best practices
- Creates LLM-friendly content structure

### 9. **quality_check**
Perform comprehensive pre-publish quality assurance
- Checks grammar, SEO requirements, brand consistency
- Validates accessibility and technical accuracy

## Usage

After restarting Claude Code, you can use these tools by invoking them through the MCP interface. The tools will automatically use:
- Your Suparank API key for SEO operations
- Your Gemini API key for image generation

## API Keys Configured

- **Suparank API Key**: Configured and ready for SEO tools
- **Gemini API Key**: Configured for AI image generation

## Next Steps

To complete the setup:

1. **Restart Claude Code** to load the MCP server configuration
2. **Verify Connection**: Once restarted, try using one of the Suparank tools
3. **Provide Project Slug** (optional for CLI): If you want to complete the CLI setup, run:
   ```bash
   npx suparank setup
   ```
   And provide your project slug when prompted.

## Troubleshooting

If the MCP server doesn't load:
- Ensure the config file exists at `/root/.config/claude-code/config.json`
- Verify that `npx` is available in your PATH
- Check that you have internet connectivity for `npx suparank` to download the package

## References

- Suparank Dashboard: https://app.suparank.io/dashboard
- API Keys: https://app.suparank.io/dashboard/settings/api-keys
