# Changelog

All notable changes to **ansible.windows** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.5.0] - 2026-05-15

### Added

- `win_credential_info` module for querying Windows Credential Manager entries
- Shared `CredentialManager.cs` module utility extracted from win_credential
- Integration tests for `win_credential_info` module
- Changelog fragment for `win_credential_info`

### Fixed

- Treat empty string filter as null for `CredEnumerateW`
- Use `CredEnumerateW` for wildcard names with type filter
- Unmarshal certificate credential usernames to thumbprints
- Include `cert.pfx` locally instead of referencing `win_credential`
- Use inline C# with unique namespace to avoid type conflicts
- Revert `win_credential.ps1` to keep inline C#
- Resolve pslint warnings in `win_credential_info`
- Alphabetize choices in PS argspec to match Python docs
- Add `notsecret` annotation for gitleaks false positive
