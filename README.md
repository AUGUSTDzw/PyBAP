# ps: Edit in vscode

In order to avoid the issue : "No module named:xxx".
You need add following configuration:

1. In launch.json(you may need create it manually) add following configuration,
   **"env": { "PYTHONPATH": "${workspaceRoot}" }**
```json
{
	"version": "0.2.0",
	"configurations": [
		{
			"name": "Python Debugger: Current File",
			"type": "debugpy",
			"request": "launch",
			"program": "${file}",
			"console": "integratedTerminal",
			"env": { "PYTHONPATH": "${workspaceRoot}" }
		}
	]
}
```

2. In settings.json(you may need create it manually) add following configuration,
```json
{
	"terminal.integrated.env.windows": {
		"PYTHONPATH": "${workspaceFolder};${env:PYTHONPATH}"
	}
}
```
