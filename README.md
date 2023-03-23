# Sitecore Content Hub ONE CLI

![GitHub release (latest by date)](https://img.shields.io/github/v/release/Sitecore/content-hub-one-cli)

## :tada: Features

- Establish connections to all of your tenants.
- Manage preview and delivery API keys.
- Publish and unpublish content and media items.
- Serialize and deserialize all your data (content types, content items, taxonomies and media items).


## :computer: Installation

[Binary releases](https://github.com/Sitecore/content-hub-one-cli/releases/latest) are available, but the use of a package manager is highly recommended.

```bash
# Homebrew (macOS, Linux)
brew install sitecore/content-hub/ch-one-cli

# Chocolatey (Windows)
choco install Sitecore.ContentHubOne.Cli --source https://nuget.sitecore.com/resources/v2/

# Cross-platform (requires .NET 6 SDK)
dotnet tool install --global --add-source https://nuget.sitecore.com/resources/v3/index.json ch-one-cli

# Docker
docker run --rm -it scr.sitecore.com/sch/ch-one-cli:latest
```

## :runner: Quick Start

1. Add a new tenant with the `tenant add` command:

    ```bash
    # Device Authorization Flow (requires user interaction)
    ch-one-cli tenant add --tenant-id <YOUR_TENANT_ID> --client-id <OAUTH_CLIENT_ID>

    # or

    # Client Credentials Flow
    ch-one-cli tenant add --client-id <OAUTH_CLIENT_ID> --client-secret <OAUTH_CLIENT_SECRET>
    ```
2. Execute a command against the newly added tenant:

    ```bash
    # Example: Pull all content types
    ch-one-cli serialization pull content-type
    ```

## :books: Help and Documentation

All commands support the `--help` option which shows a brief description and information about the expected and supported arguments or options.

```bash
# Example
ch-one-cli tenant add --help
```

Additional information and walkthroughs for specific features can be found in the [documentation](https://doc.sitecore.com/ch-one/en/developers/content-hub-one/content-hub-one-cli.html).
