# Strands Langfuse Integration

This guide explains how to set up and test the Langfuse integration in the `agent.py` file.

## Environment Setup

Set the following environment variables in your `agent.py` file:

```python
os.environ["LANGFUSE_PUBLIC_KEY"] = "pk-..."  # Replace with your Langfuse public key
os.environ["LANGFUSE_SECRET_KEY"] = "sk-..."  # Replace with your Langfuse secret key
```

## Steps to Configure

1. Run the following command to auto-create the settings:

   ```bash
   agentcore configure --entrypoint agent.py --name strands_langfuse

   ```

2. Launch the agent:
   ```bash
   agentcore launch
   ```

## Testing the Integration

To test the Langfuse integration, invoke the agent with a sample payload:

```bash
agentcore invoke '{"prompt": "test langfuse"}'
```

Check langfuse dashboard

## Notes

- Replace placeholder keys (`pk-...` and `sk-...`) with your actual Langfuse keys.
- Ensure all dependencies are installed and the environment is properly configured before running the commands.
