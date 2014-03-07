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

This would output as:

{color:red}_Feature_{color}: When anyone uses this utility
*  {color:red}*As*{color} a User
*  {color:red}*I*{color} want to know how my .feature file will be formatted
*  {color:red}*So*{color} that I can decide if I want to use this utility

{color:blue}@wip{color}
{color:red}_Scenario_{color}: User successfully logs in via the login form
*  {color:red}*Given*{color} I am on the home page
*  {color:red}*And*{color} I show that "inline strings" can be formatted
*  {color:red}*And*{color} I show that block strings can be formatted
{quote}{color:orange}"""
This is a really, really,
really, really, really, really,
really, really, really, really,
really, really, really, really,
long string that serves no purpose
"""{color}{quote}
*  {color:red}*When*{color} I am done
*  {color:red}*Then*{color} I have shown how the formatting works
