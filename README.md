# rubocop_bug_demo
Just to reproduce a rubocop issue; nothing to see here...

Using Ruby 2.3 and Rubocop 0.49.1
 * (in root directory) bundle install --path vendor/bundle
 * (in testing directory) bundle install --path vendor/bundle
 * (in root directory) bundle exec rubocop -d
 
 The output indicates 3 files are scanned but the summary is "2 files inspected, no offenses detected"
 
 ```
 [centos@test-development rubocop_test]$ bundle exec rubocop -d
For /home/centos/rubocop_test: configuration from /home/centos/rubocop_test/.rubocop.yml
Default configuration from /home/centos/rubocop_test/vendor/bundle/ruby/2.3.0/gems/rubocop-0.49.1/config/default.yml
Inheriting configuration from /home/centos/rubocop_test/vendor/bundle/ruby/2.3.0/gems/rubocop-0.49.1/config/enabled.yml
Inheriting configuration from /home/centos/rubocop_test/vendor/bundle/ruby/2.3.0/gems/rubocop-0.49.1/config/disabled.yml
Inspecting 4 files
Scanning /home/centos/rubocop_test/Gemfile
.Scanning /home/centos/rubocop_test/testing/Gemfile
.Scanning /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.irbrc
For /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0: configuration from /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop.yml
Inheriting configuration from /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop_todo.yml


2 files inspected, no offenses detected
Error: The `Style/TrailingComma` cop no longer exists. Please use `Style/TrailingCommaInLiteral` and/or `Style/TrailingCommaInArguments` instead.
(obsolete configuration found in /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop_todo.yml, please update it)
The `Style/SingleSpaceBeforeFirstArg` cop has been renamed to `Layout/SpaceBeforeFirstArg`.
(obsolete configuration found in /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop_todo.yml, please update it)
The `Layout/SpaceAfterControlKeyword` cop has been removed. Please use `Layout/SpaceAroundKeyword` instead.
(obsolete configuration found in /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop_todo.yml, please update it)
The `Style/SpaceAfterControlKeyword` cop has been removed. Please use `Layout/SpaceAroundKeyword` instead.
(obsolete configuration found in /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop_todo.yml, please update it)
The `Style/MethodCallParentheses` cop has been renamed to `Style/MethodCallWithoutArgsParentheses`.
(obsolete configuration found in /home/centos/rubocop_test/testing/vendor/bundle/ruby/2.3.0/gems/fog-digitalocean-0.3.0/.rubocop_todo.yml, please update it)
Finished in 0.5497931893914938 seconds
 ```
