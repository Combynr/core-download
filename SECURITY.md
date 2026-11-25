# Security Policy

## Reporting a vulnerability

Please report security problems privately. Do not open a public issue or pull request for them.

Use one of these:

- Email: security@combynr.com
- GitHub private vulnerability reporting: the "Report a vulnerability" button under the Security tab of this repository.

Include as much of the following as you can:

- the version of combynr:core (shown on the System check page) and your operating system;
- a description of the problem and its impact;
- the steps to reproduce it, or a proof of concept;
- any suggested fix, if you have one.

We will acknowledge your report, investigate it, and keep you informed of progress. We ask that you keep the details private until a fix is available.

## Supported versions

Only the latest release of combynr:core receives security fixes. Please check that the problem exists in the latest release before you report it.

## Security model

- The app binds to 127.0.0.1 only. It does not listen on other network interfaces.
- The Python code sandbox applies limits and defence-in-depth checks: a script cannot open or change files outside its run folder through the guarded calls (it may read Python's standard library), cannot open network sockets, and gets a cleared environment and a time limit. It can still see the names of files and folders elsewhere, for example by listing a folder. It is not a security boundary and does not isolate code from your machine. Code that the model writes runs with your user's permissions.
- Only run code, and only connect MCP servers, that you are willing to run on your own machine.
