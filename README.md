# Schema Library MCP Server

A Model Context Protocol server that enables AI agents to directly interact with schema library projects. Connect your favorite AI assistant to create, update, search, and manage schema library projects seamlessly.

## 🚀 Features

- **Schema Project Management**: Create and update schema library projects
- **Advanced Search**: Search for schemas across the library with intelligent filtering
- **Metadata Access**: Fetch detailed schema information and metadata
- **CoreModels Integration**: Work with schemas specifically related to CoreModels platform
- **Seamless Authentication**: Optional API token authentication handled directly in chat
- **Real-time Updates**: Live interaction with your schema library

## 📦 Installation

### For Claude Desktop

Add the following to your Claude Desktop configuration file:

**Windows:** `%APPDATA%\Claude\claude_desktop_config.json`  
**macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`  
**Linux:** `~/.config/Claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "schemaLibrary": {
      "url": "https://go.coremodels.io/mcp"
    }
  }
}
```

### For Cursor IDE

Add to your MCP configuration:

```json
{
  "mcpServers": {
    "schema-library": {
      "url": "https://go.coremodels.io/mcp"
    }
  }
}
```

### For Other MCP Clients

Use the server URL: `https://go.coremodels.io/mcp`

## 🔐 Authentication

The Schema Library MCP Server supports both authenticated and non-authenticated operations:

- **Public Operations**: Search and view public schemas (no authentication required)
- **Project Management**: Create, update, and manage your own projects (requires API token)
- **Token Entry**: When authentication is needed, simply provide your API token when prompted in the chat

## 🛠️ Available Tools

### Project Management
- **`SchemaLibrary_CreateProject`**: Create new schema library projects with metadata
- **`SchemaLibrary_UpdateProject`**: Update existing project details and classifications
- **`SchemaLibrary_QueryProject`**: Get detailed information about specific projects

### Search & Discovery
- **`SchemaLibrary_ProjectsSection`**: Search for schemas with advanced filtering options
- **`SchemaLibrary_GetMetadataOptions`**: Retrieve available metadata categories and options
- **`SchemaLibrary_GetClassifications`**: Get available schema classifications

### Use Cases Management
- **`SchemaLibrary_GetUseCaseTypes`**: Get available use case types for projects
- **`SchemaLibrary_UpdateUseCases`**: Add or remove use cases for projects

## 💡 Usage Examples

### Creating a New Schema Project
```
Create a new schema library project for a healthcare data model.
Title: 'Patient Records Schema'
Domain: Healthcare
Format: JSON Schema
Description: A comprehensive schema for patient medical records
Tags: ['healthcare', 'patient-data', 'medical-records']
```

### Searching for Existing Schemas
```
Find all JSON Schema projects related to financial data

Search for healthcare schemas with patient data

Browse projects in the e-commerce domain

Find schemas tagged with 'API' and 'REST'
```

## 🏗️ Schema Library Structure

The server works with projects that contain:

- **Metadata**: Project descriptions, domains, formats, audiences
- **Classifications**: Categorization tags for better organization  
- **Use Cases**: Specific implementation scenarios
- **Access Control**: Public/private project visibility

## 📚 API Reference

For detailed API information about available tools and parameters, the server exposes comprehensive tool definitions that your AI assistant can inspect and use dynamically.

## 🆘 Support

- **Repository**: https://github.com/qg-aramai/schema-library-mcp-server
- **Issues**: https://github.com/qg-aramai/schema-library-mcp-server/issues
- **Server Status**: https://go.coremodels.io/mcp
- **Documentation**: [Schema Library Docs](https://library.schematica.io/mcp-server)

## 🤝 Contributing

We welcome contributions! Please:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request with detailed description

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🎯 Getting Started

1. **Install**: Add the server to your MCP client configuration
2. **Test**: Ask your AI assistant: "What Schema Library tools are available?"
3. **Explore**: Try searching for schemas: "Find schemas related to [your domain]"
4. **Create**: Start building: "Create a new schema project for [your use case]"

---

*Built with ❤️ for the MCP community*
