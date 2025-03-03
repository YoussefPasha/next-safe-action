---
sidebar_position: 4
description: Action result object is the result of an action execution, returned by hooks.
---

# Action result object

Here's how action result object is structured (all keys are optional):


| Name               | When                                                   | Value                                                                                                                                                                                                                                                               |
|--------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data?`            | Execution is successful.                               | What you returned in action's server code.                                                                                                                                                                                                                          |
| `validationError?` | Some input values are invalid.                         | A partial `Record` of input schema keys as key, and `string[]` as value. Example: `{ email: ["Email is required."] }`                                                                                                                                               |
| `serverError?`     | An error occurs during action's server code execution. | A `string` that by default is "Something went wrong while executing the operation" for every server error that occurs, but this is [configurable](/docs/safe-action-client/custom-server-error-handling#handlereturnedservererror) when instantiating a new client. |