# GitHub MCP Server Plus

MCP Server for the GitHub API, enabling file operations, repository management, search functionality, and more.

### Features

- **Automatic Branch Creation**: When creating/updating files or pushing changes, branches are automatically created if they don't exist
- **Comprehensive Error Handling**: Clear error messages for common issues
- **Git History Preservation**: Operations maintain proper Git history without force pushing
- **Batch Operations**: Support for both single-file and multi-file operations with content or file paths
- **Advanced Search**: Support for searching code, issues/PRs, and users


## Tools

1. `create_or_update_file`
   - Create or update a single file in a repository
   - Inputs:
     - `owner` (string): Repository owner (username or organization)
     - `repo` (string): Repository name
     - `path` (string): Path where to create/update the file
     - `content` (string): Content of the file
     - `message` (string): Commit message
     - `branch` (string): Branch to create/update the file in
     - `sha` (optional string): SHA of file being replaced (for updates)
   - Returns: File content and commit details

2. `push_files_content`
   - Push multiple files with direct content in a single commit
   - Inputs:
     - `owner` (string): Repository owner
     - `repo` (string): Repository name
     - `branch` (string): Branch to push to
     - `files` (array): Files to push, each with `path` and `content`
     - `message` (string): Commit message
   - Returns: Updated branch reference

3. `push_files_from_path`
   - Push multiple files from filesystem paths in a single commit
   - Inputs:
     - `owner` (string): Repository owner
     - `repo` (string): Repository name
     - `branch` (string): Branch to push to
     - `files` (array): Files to push, each with:
       - `path` (string): Target path in the repository
       - `filepath` (string): Source filesystem path to read from
     - `message` (string): Commit message
   - Returns: Updated branch reference

[Rest of original content remains the same...]