### Puppet Module tests
This is a collection of tests that can be used to make sure that when you write puppet modules, you do a good
job. It should be included in your Puppet module/project via a specially crafted URL using the secret gitlab token since
git submodules are not properly supported by gitlab's ci at this time. 

## Tests

* puppet-lint
*Runs the puppet-lint script against all .pp files in the project*
* erb-syntax
*Does a Ruby Syntax check against all .erb files withing the project*
* puppet-validate
*Runs puppet parser validate against all .pp files in the project*
* puppet-missing-files [module]
*Attempts to figure out if you reference any files that are not included in the project. It is unable to check filenames that include variables.*
*if you pass the optional argument module, it will assume the test is being run against a project that is a single module*
* puppetfile-test
*Run a R10K parse check on Puppetfile*
