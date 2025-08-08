---
title: Copilot Extension
page_title: Telerik WPF GitHub Copilot Extension
description: Learn how to add and use the Telerik WPF GitHub Copilot extension as a .NET WPF AI coding assistant and code generator for better developer productivity. The Telerik WPF GitHub Copilot extension provides proprietary context about Telerik UI for .NET WPF to AI-powered software.
slug: ai-copilot-extension
tags: telerik, wpf, ai, coding assistant, ai server
position: 10
---

# Telerik WPF GitHub Copilot Extension

The Telerik WPF [GitHub Copilot](https://github.com/features/copilot) extension is an AI-powered coding assistant that provides specialized knowledge about [Telerik UI for .NET WPF components](https://www.telerik.com/wpf). 

This extension enhances GitHub Copilot with proprietary context about Telerik WPF controls, helping you:

* Generate code snippets using Telerik WPF components.
* Get contextual suggestions for component properties and methods.
* Access best practices and implementation patterns.
* Speed up development with AI-powered code completion.

## Prerequisites

Before using the Telerik WPF GitHub Copilot extension, ensure you have:

* An active [GitHub Copilot](https://github.com/features/copilot) subscription. You can enable or configure GitHub Copilot on the [Copilot Settings page in your GitHub account](https://github.com/settings/copilot).
@[template](/_contentTemplates/ai-coding-assistant.md#getting-started)
* The latest version of your [Copilot-enabled app](https://docs.github.com/en/copilot/building-copilot-extensions/about-building-copilot-extensions#supported-clients-and-ides) (Visual Studio).

## Installation

Follow these steps to install and configure the Telerik WPF Copilot extension:

1. Go to the [Telerik WPF GitHub App](https://github.com/apps/telerikwpf) page and click the **Install** button.
1. You will see a list that includes your GitHub account and all GitHub organizations that you are part of. Select your GitHub account.
1. Click the **Install & Allow** button. This will allow the GitHub Copilot extension to integrate with your GitHub account.
1. Enter your GitHub password when prompted.
1. You will be redirected to telerik.com. Enter your Telerik account credentials if prompted. This step links the GitHub Copilot extension with your Telerik account.
1. Upon successful Telerik authentication, you will be redirected to a confirmation page that indicates successful Copilot extension installation.
1. Restart your [Copilot-enabled app](https://docs.github.com/en/copilot/building-copilot-extensions/about-building-copilot-extensions#supported-clients-and-ides) (Visual Studio).
1. Start a new chat session in Copilot.

## Usage

To use the Telerik WPF Copilot extension:

1. Open the GitHub Copilot chat window in your [Copilot-enabled app](https://docs.github.com/en/copilot/building-copilot-extensions/about-building-copilot-extensions#supported-clients-and-ides) (Visual Studio).
1. Ensure you are in **Chat** mode and not in **Edit** or **Agent** mode. The Edit and Agent modes do not use the Telerik Copilot extension. However, the Agent mode can use the [Telerik WPF MCP server]({%slug ai-mcp-server%}).
1. Start your prompt with `@TelerikWPF` and type your request. Verify that `@TelerikWPF` is recognized and highlighted; otherwise, the extension may not be properly installed.
1. Look for a status label such as **Telerik WPF working...** or **Telerik WPF generating response...** in the output to confirm the extension is active.
1. Grant permission to the Telerik WPF extension to read your workspace files when prompted. This is required only the first time to send a prompt. Also, it might be required to restart Visual Studio again.
1. For unrelated queries, start a new chat session in a new window to avoid context pollution from previous conversations.

### Sample Prompts

The following examples demonstrate useful prompts for the Telerik WPF extension:

* "`@TelerikWPF` Generate a GridView with sorting and paging enabled."
* "`@TelerikWPF` Create a Telerik ComboBox for WPF with multiple selection enabled."
* "`@TelerikWPF` Show me how to implement a Chart with line series."
* "`@TelerikWPF` Generate a QueryableCollectionView with grouping and filtering capabilities."

![Image showing the TelerikWPF trigger word](images/ai-copilot-extension-0.png)

## Number of Requests

@[template](/_contentTemplates/ai-coding-assistant.md#number-of-requests)

## Troubleshooting

If you encounter issues:

* Ensure the `@TelerikWPF` mention is properly highlighted in your prompt.
* Verify that you have an active GitHub Copilot subscription.
* Restart your IDE after installation.
* Check that you're in Ask mode, not Edit or Agent mode.

## See Also 

* [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
* [GitHub Copilot Tutorials](https://github.com/features/copilot/tutorials)
* [Telerik WPF MCP Server]({%slug ai-mcp-server%})
* [Telerik UI for .NET WPF Documentation](https://docs.telerik.com/devtools/wpf/)