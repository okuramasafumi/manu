# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Ruby gem project called "manu" in its initial development state. The gem follows standard Ruby gem conventions using Bundler and includes:

- Main module: `Manu` with version management
- Test framework: Minitest
- Code quality: RuboCop
- Type definitions: RBS signatures in `sig/`

## Development Commands

**Setup and Dependencies:**
```bash
bin/setup                    # Install dependencies and setup environment
bundle install              # Install gem dependencies
```

**Testing:**
```bash
rake test                    # Run all tests with Minitest
bundle exec rake test        # Run tests via bundle exec
```

**Code Quality:**
```bash
rubocop                      # Run RuboCop linting
bundle exec rubocop          # Run RuboCop via bundle exec
rake rubocop                 # Run RuboCop via Rake task
```

**Development Workflow:**
```bash
bin/console                  # Start interactive console with gem loaded
rake                         # Run default task (test + rubocop)
bundle exec rake install     # Install gem locally for testing
```

**Gem Management:**
```bash
bundle exec rake release     # Release new version (update version.rb first)
```

## Code Architecture

**Core Structure:**
- `lib/manu.rb` - Main entry point defining the `Manu` module
- `lib/manu/version.rb` - Version constant management
- `sig/manu.rbs` - RBS type signatures for the module

**Testing:**
- `test/test_helper.rb` - Test configuration and setup
- `test/test_manu.rb` - Main test file using Minitest::Test

**Configuration:**
- `manu.gemspec` - Gem specification with metadata and dependencies
- `Gemfile` - Development dependencies (irb, rake, minitest, rubocop)
- `Rakefile` - Task definitions with default task running tests and rubocop

The project requires Ruby >= 3.1.0 and follows frozen string literal convention throughout.
