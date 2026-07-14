# Naming Conventions

> **Project:** Enterprise Data Platform SDK
>
> **Organization:** Data & AI Cafe

---

# Purpose

This document defines the naming conventions used throughout the Enterprise Data Platform SDK.

Consistent naming improves readability, maintainability, discoverability, and collaboration.

When naming anything, prefer **clarity over brevity**.

---

# General Principles

Names should be:

- Meaningful
- Consistent
- Predictable
- Easy to read
- Easy to search

A good name should clearly communicate its purpose without requiring additional comments.

---

# General Rules

## Prefer complete words

Good

```text
Configuration
Repository
Execution
Validation
```

Avoid

```text
Config
Repo
Exec
Valid
```

---

## Avoid abbreviations

Unless they are universally accepted.

Allowed

```text
API
URL
JSON
YAML
CSV
SQL
UUID
PDF
PII
AI
LLM
SDK
```

Avoid

```text
Cfg
Mgr
Svc
Prov
Obj
Tmp
```

---

# Repository Names

Repository names should use:

- lowercase
- hyphen-separated words

Example

```text
enterprise-data-platform-sdk
enterprise-banking-lakehouse
synthetic-data-generator
```

---

# Package Names

Package names should:

- use lowercase
- use underscores only when required by Python

Example

```text
enterprise_data_platform

config

metadata

pipeline

quality

security

monitoring

plugins
```

Avoid

```text
Config

PipelineEngine

DataPlatform
```

---

# Module Names

Module (file) names should use:

snake_case

Examples

```text
configuration_manager.py

yaml_configuration_loader.py

metadata_repository.py

pipeline_engine.py

configuration_validator.py
```

Avoid

```text
ConfigMgr.py

PipelineEngine.py

Utils.py
```

---

# Class Names

Classes should:

- use PascalCase
- represent nouns

Examples

```text
ConfigurationManager

PipelineEngine

MetadataRepository

ConfigurationValidator

YamlConfigurationLoader

SecretProvider
```

Avoid

```text
Manager

Helper

Processor

Utils

Handler
```

Class names should describe what the class represents.

---

# Interface Names

Python does not require an "I" prefix.

Good

```text
ConfigurationProvider

StorageProvider

MetadataRepository
```

Avoid

```text
IConfigurationProvider

IMetadataRepository
```

---

# Method Names

Methods should:

- use snake_case
- begin with a verb

Examples

```text
load_configuration()

validate_configuration()

execute_pipeline()

resolve_secret()

register_provider()

save_metadata()
```

Avoid

```text
process()

run()

execute()

handle()

do_work()
```

Methods should clearly describe the action being performed.

---

# Variable Names

Variables should:

- use snake_case
- clearly describe the stored value

Examples

```text
application_configuration

execution_context

storage_provider

pipeline_definition

metadata_registry
```

Avoid

```text
cfg

obj

tmp

value

var

data1
```

---

# Boolean Variables

Boolean variables should answer a question.

Examples

```text
is_valid

is_enabled

has_configuration

can_execute

should_retry
```

Avoid

```text
valid

enabled

retry
```

---

# Constants

Constants should use:

UPPER_SNAKE_CASE

Examples

```text
DEFAULT_TIMEOUT_SECONDS

DEFAULT_LOG_LEVEL

SUPPORTED_FILE_FORMATS

DEFAULT_CONFIGURATION_DIRECTORY
```

---

# Enum Names

Enums use PascalCase.

Members use UPPER_SNAKE_CASE.

Example

```text
Environment

Development

Testing

Production
```

Members

```text
DEVELOPMENT

TEST

PRODUCTION
```

---

# Exception Names

Exceptions should always end with:

Exception

Examples

```text
ConfigurationException

ValidationException

MetadataException

PipelineException

StorageException
```

Avoid

```text
ConfigurationError

ConfigProblem

SomethingFailed
```

---

# Test Files

Test file names should begin with:

test_

Examples

```text
test_configuration_manager.py

test_yaml_loader.py

test_metadata_repository.py
```

---

# Test Methods

Test names should clearly describe behaviour.

Examples

```text
test_should_load_configuration()

test_should_raise_exception_when_file_is_missing()

test_should_validate_configuration()

test_should_return_default_value()
```

Avoid

```text
test1()

test_configuration()

test_method()
```

---

# Branch Names

Feature branches

```text
feature/configuration-framework

feature/metadata-framework

feature/pipeline-engine
```

Bug fixes

```text
fix/configuration-validation

fix/logging
```

Documentation

```text
docs/engineering-standards
```

Refactoring

```text
refactor/configuration-manager
```

---

# Commit Messages

The project follows Conventional Commits.

Format

```text
<type>(<scope>): <description>
```

Examples

```text
chore: initialize project structure

feat(config): add YAML configuration loader

fix(metadata): resolve validation issue

refactor(pipeline): simplify execution flow

test(config): add unit tests

docs(engineering): update coding guidelines

ci: add GitHub Actions workflow
```

---

# Configuration Files

Use lowercase.

Examples

```text
application.yaml

logging.yaml

security.yaml

monitoring.yaml

storage.yaml
```

---

# Documentation Files

Use lowercase with hyphens.

Examples

```text
engineering-standards.md

coding-guidelines.md

naming-conventions.md

testing-standards.md

definition-of-done.md
```

---

# Avoid Generic Names

Avoid creating files, classes, or methods with names like:

```text
Helper

Utils

Common

Misc

Manager (unless it truly manages something)

Handler

Processor
```

Use names that describe responsibility instead.

---

# Naming Checklist

Before naming anything, ask:

- Does the name clearly describe its purpose?
- Is it consistent with existing names?
- Can another developer understand it immediately?
- Is it searchable?
- Will it still make sense as the project grows?

If the answer to any of these questions is "No", choose a better name.

---

# Final Principle

> **Good names eliminate the need for comments.**

If a name requires additional explanation, it should be improved rather than documented.