# Pugin
Pugin is a component-based pattern design library that holds all of the reusable partials, styles and scripts for elements of Parliamentary Digital Service microservices. It is named after the designer [Augustus Welby Northmore  Pugin](https://en.wikipedia.org/wiki/Augustus_Pugin), who provided designs for the interior of the Palace of Westminster.

## Installation
Instead of releasing Pugin on RubyGems.org and versioning twice, at Parliamentary Digital Service we use Pugin as a git submodule to keep versioning in once place.

To install:

1. `cd` into your consuming application directory
2. On your command line, run: `git submodule add https://github.com/ukpds/pugin.git pugin`. This will version a subfolder called _pugin_ in your consuming application directory.
3. Add the following into your Gemfile: `gem 'pugin', path: './pugin'`
4. On your command line, run: `bundle`
5. You're setup!

## Usage
The Pattern library engine works through a simple request that can be called from within your Rails applications. Dependant on the data that you wish to pass with your requests, there are two methods that can be used. 

### Requests

PUGIN.get_component_by_model(template name, data to be passed)

PUGIN.get_component_by_single(template name, data to be passed)

### Data Requirements

**get_component_by_model:** data passed as objects

**get_component_by_single:** data passed as singular hashes

*NOTE: Both methods accept empty data inputs*

### Example Requests 

PUGIN.get_component_by_model('modules/profile-card', @person)

PUGIN.get_component_by_single('modules/profile-card', {member_name: "Jane Ivy"})

## Contributing
To contribute to Pugin, please fork this repository and create a branch in your fork. When installing, specify the submodule repository to your fork to allow you to test whatever you build.

Following writing your code, please create a pull request into the Pugin repository. It will be reviewed by a member of the internal Parliamentary Digital Service team.

## Licence
The gem is available under the [Open Parliament Licence](http://www.parliament.uk/site-information/copyright/open-parliament-licence/).
