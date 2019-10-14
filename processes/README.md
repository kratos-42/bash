# Processes related commands

### `find_process`

Finds all processes related to the provided process name (or part of it). This avoid to search for a given process/processes in the `top` list.

#### Example

*Input*

```sh
> find_process Chr
```

or

```sh
> find_process Chrome
```

*Output*

```sh
31530	 Process: /Applications/Google
31531	 Process: /Applications/Google
```
