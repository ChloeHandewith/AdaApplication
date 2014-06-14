Technical Reading Responses
=================


1. The Command “bundle gem foodie” creates a scaffold directory for the gem and allows you to commit files to github. While generating several files in the directory such as, “Gemfile”, “Rakefile”, “foodie.gemspec”, etc.

2. The tests are stored in the file called “spec”. If a gem has more facets to it the file would be “spec/facet” as a sub directory.

3. To add the active support dependency you need to write in the “Gem: :Specification” file the line, spec.add_dependency “activesupport”, “4.0.0” adding the comma quote 4.0.0 tells it to specifically use the version 4.0.0

4. To write a generator you need to start with a CLI (command line interface, also doesn’t have to be titled CLI), to do that you need to define the lib/foodie/cli.rb file, which could be done with a short command. In the technical reading they build off of the Thor gem to create it by telling it to require ‘thor’ but that isn’t enough you need to add spec.add_dependency “thor” then have the new dependency installed to the bundle. 
After having the entirety of Foodie: :CLI set up you can define a generator class similarly,  you just having to add in the end for it require ‘foodie/generators/recipe” so that it may generate the file scaffold recipe, creating, lib/foodie/generators/recipe.rb
then you must define groups, copy recipe template and have a template set up to be copied.

    And remember, Friendship is Magic
