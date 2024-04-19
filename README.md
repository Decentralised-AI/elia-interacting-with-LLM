# Elia

A terminal ChatGPT client built with Textual

![img.png](https://github.com/darrenburns/elia/assets/49741340/80453ed8-ec94-4095-b721-89d32d9fc327)

> **Note**
> Elia is still a work in progress. How far will I go with this? I have no idea...

## Quickstart

Install Elia with [pipx](https://github.com/pypa/pipx), set your `OPENAI_API_KEY` environment variable,
and start the app:

```bash
pipx install git+https://github.com/darrenburns/elia
export OPENAI_API_KEY="xxxxxxxxxxxxxx"
elia
```

If you're a member of multiple organizations on the OpenAI platform, you may also need to set the `OPENAI_ORGANIZATION` environment variable to your organization ID, found on the OpenAI dashboard for your organization.

```bash
export OPENAI_ORGANIZATION="org-klj8ashdkJHKJas"
```

### Wiping the Chat History

Chat history is stored in a SQLite database alongside the Elia application.
To wipe the chat history, simply run the db reset command:

```bash
elia reset
```

### Changing the Chat Directive

By default, Elia's conversations with ChatGPT are primed with a
directive for the GPT model:

`You are a helpful assistant.`

This can be changed by setting the `ELIA_DIRECTIVE` environment variable before
starting a new conversation. A directive is set for the lifetime of a conversation.

```bash
export ELIA_DIRECTIVE="You are a helpful assistant who talks like a pirate."
elia
```

### Launching Directly into a Conversation

```bash
elia chat write python code to detect a palindrome
```

## Progress updates

### June 2023

Messages are now tokenized and you can see how messages are split into tokens using the "Message Details" modal.

<img width="700" alt="image" src="https://github.com/darrenburns/elia/assets/5740731/395fd2b5-ca83-49cc-b86b-163a44fe7750">

### May 29th 2023

SQLite/SQLModel chosen for persistence.
Conversations can be imported from ChatGPT and they'll be displayed in the sidebar.
Selecting a conversation in the sidebar will load it into the main window.
Raw markdown can be displayed.

https://github.com/darrenburns/elia/assets/5740731/0a348cc9-4fab-4266-95f6-d04143b70e7b

### May 24th 2023

Much of the core UI is in place, with some placeholders. No persistence yet, but I've begun to explore it.

https://github.com/darrenburns/elia/assets/5740731/bbdbb2b4-f571-40e4-b181-525e8e9de6f3

### May 4th 2023

Initial proof of concept.

https://user-images.githubusercontent.com/5740731/236323494-3d3ab56a-673b-45a9-b501-830926ca8fea.mov
