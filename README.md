[![Build Status](https://travis-ci.org/plus3it/mcafee-agent-windows-formula.svg)](https://travis-ci.org/plus3it/mcafee-agent-windows-formula)

# mcafee-agent

This salt formula will install McAfee Agent, for use with a McAfee ePolicy
Orchestrator (ePO) server. The formula depends on the Salt Windows Package
Manager (winrepo), and a package definition must be present for the McAfee
Agent.

The formula currently supports no configuration of the agent itself; it is
assumed all configuration is handled by the ePO server. However, the formula
does use pillar to define the name of the winrepo package, and the version to
install.


## Available States

- [mcafee-agent-windows](#mcafee-agent-windows)


### mcafee-agent-windows

Install the McAfee Agent for Windows.


## Configuration

This formula supports configuration via pillar for the name of the winrepo
package and the version of the package to install.


### mcafee-agent:package

The `package` parameter is the name of the package as defined in the winrepo
package definition.

>**Required**: `False`

>**Default**: `'mcafee-agent'`

**Example**:

```
mcafee-agent:
  package: 'mcafee-agent'
```


### mcafee-agent:version

The `version` parameter is the version of the package as defined in the
winrepo package definition.

>**Required**: `False`

>**Default**: `''`

**Example**:

```
mcafee-agent:
  version: '4.8.2003'
```
