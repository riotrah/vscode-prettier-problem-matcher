# Prettier Problem Matchers for VS Code

Provides [problem matchers](https://code.visualstudio.com/docs/editor/tasks#_processing-task-output-with-problem-matchers) for use with JS/TS projects using Prettier.

## Features

Provides the following problem matchers:

- $prettier - basic, prettier errors become Error problems
- $prettier-warning - not so useful imo, but it reports file-level warnings for style check fails as Warning problems
- $prettier-watch - for when prettier is run in 'watch mode' via onchange cli (per prettier docs)
- $prettier-warning-watch - same as above, but reports warnings as well

## Usage

The following example shows how to add problem matchers to your project:

```json
{
	"version": "2.0.0",
	"tasks": [
		{
			"type": "npm",
			"script": "prettier",
			"problemMatcher": ["$prettier"]
		},
		{
			"type": "npm",
			"script": "prettier-watch",
			"isBackground": true,
			"problemMatcher": ["$prettier-watch"]
		}
	]
}
```
