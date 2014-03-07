# .feature to JIRA comment formatter

This is a simple utility takes in a .feature file and returns a JIRA comment friendly formatted version of it via stdout, so it's great in combination with piping or redirecting.

Here's a simple .feature file example:

```Cucumber
Feature: When anyone uses this utility
  As a User
  I want to know how my .feature file will be formatted
  So that I can decide if I want to use this utility

@wip
Scenario: User successfully logs in via the login form
  Given I am on the home page
  And I show that "inline strings" can be formatted
  And I show that block strings can be formatted
  """
  This is a really, really,
  really, really, really, really,
  really, really, really, really,
  really, really, really, really,
  long string that serves no purpose
  """
  When I am done
  Then I have shown how the formatting works
```
