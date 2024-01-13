# gh-deployment-manager
A command-line tool for managing deployments on GitHub repositories.

## Usage 
```
./deployment-cli <command> [options]
```

### options

```
--authorization_header: GitHub API authorization header (default: value from environment variable GITHUB_AUTH_HEADER).
--verbose: Enable verbose mode.
--api_url: GitHub API URL (default: https://api.github.com).
--repo-owner: Repository owner.
--repo-name: Repository name.
--payload: JSON data to create a new deployment.
```

### Examples 
```
# List all environments
./deployment-cli get

# List all deployments in the 'production' environment
./deployment-cli get production

# View details of the deployment with ID '123456' in the 'staging' environment
./deployment-cli get staging 123456

# Delete the 'staging' environment and all deployments in that
./deployment-cli delete staging

# Delete the deployment with ID '123456'
./deployment-cli delete 123456

# Create a new deployment with a JSON payload
./deployment-cli create --payload '{"description": "New deployment", "ref": "main", "environment": "staging", "auto_merge": true}' 

```
