# Testing and Updating All Archon Features

This guide will help you test and update all features of Archon using your Gitpod workspace.

## Step 1: Update Your Code to the Latest Version

In your Gitpod terminal, run the following commands to get the latest code:

```bash
git remote add upstream https://github.com/coleam00/Archon.git
git fetch upstream
git reset --hard upstream/main
```

## Step 2: Enable All Features

Edit your `.env` file to enable all features:

```
# Add this line to your .env file
ENABLE_ALL_FEATURES=true
```

## Step 3: Reinstall Dependencies

To make sure you have all the required dependencies for the latest features:

```bash
pip install -r requirements.txt

# If you need to install additional packages for MCP server
pip install -r mcp/requirements.txt
```

## Step 4: Restart Streamlit

Restart the Streamlit server to apply all changes:

```bash
streamlit run streamlit_ui.py
```

## Features to Test

Here are the key features of Archon that you should test:

1. **Intro and Setup**
   - Configure your environment settings
   - Set up a Supabase vector database
   - Crawl and index documentation

2. **Build Agent**
   - Provide a description of the agent you want to build
   - Test different agent types (Pydantic AI, LangGraph, etc.)
   - Test the generated agent code

3. **Tool Library** (V6 Feature)
   - Explore the prebuilt tools
   - Test integrating tools into your agent
   - Try adding a custom tool

3. **MCP Integration** (V6 Feature)
   - Test the MCP (Master Control Program) server integration
   - Try creating an agent that uses the MCP server

4. **Workbench**
   - Test the code editor functionality
   - Try modifying and saving agent code
   - Test running agents from the workbench

## Troubleshooting

If you encounter any issues:

1. **Errors during setup**:
   - Check the terminal for specific error messages
   - Make sure all dependencies are installed
   - Verify that your OpenRouter API key is correct

2. **Streamlit UI issues**:
   - Try refreshing the page
   - Restart the Streamlit server
   - Check the terminal for errors

3. **MCP server issues**:
   - Make sure the MCP server is running
   - Check the connection settings in your `.env` file

## Updating Archon in the Future

To keep Archon updated with the latest features:

```bash
# Fetch the latest changes
git fetch upstream

# Reset your local branch to match the upstream branch
git reset --hard upstream/main

# Reinstall dependencies in case they've changed
pip install -r requirements.txt
```

## Additional Resources

- [Archon GitHub repository](https://github.com/coleam00/Archon)
- [Archon community forum](https://thinktank.ottomator.ai/c/archon/30)
- [Cole Medin's YouTube channel](https://www.youtube.com/c/ColeMedin)
