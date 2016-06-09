# commit-watcher-rules

[Commit Watcher](https://github.com/srcclr/commit-watcher) finds interesting and potentially hazardous commits in git projects. Watch your own projects to make sure you didn't accidentally leak your AWS keys or other credentials, and watch open-source projects you use to find undisclosed security vulnerabilities and patches.

This project contains a collection of [rules](https://github.com/srcclr/commit-watcher/blob/master/config/rule_types.yml) you can use with Commit Watcher.

### Submitting Rules

To submit a rule to this project, use this commit as an example: [https://github.com/srcclr/commit-watcher/commit/3ae9e2d340f1ac4d10c9ebffae64c22b0a6ac706](https://github.com/srcclr/commit-watcher/commit/3ae9e2d340f1ac4d10c9ebffae64c22b0a6ac706)

Let's break down the rule a bit:

```
{
  name: 'markdown_file',
  rule_type_id: 1,
  value: '(?i)\.(md|markdown)\z',
  description: 'Markdown file'
}
```

There are four different values for the rule:

1. name - unique name, valid characters are alpha numeric, '-', '_', and '.'
2. rule\_type\_id - this is the ID for a rule type described above
3. value - regular expression; this example could be read as "case insensitive, starts with a '.' and is followed either by 'md' or 'markdown' and then the end of the string"
4. description - free text field for describing the rule

Any submissions made to the community rules will be Apache 2.0 licensed.
