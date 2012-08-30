require "coyote/rake"
require 'rb-fsevent'

multitask :watch => ['js:watch']
multitask :watchprod => ['js_min:watch']

namespace :js do
  coyote do |config|
    config.input = "js/application.coffee"
    config.output = "js/application.js"
    config.options = { :quiet => true }
  end
end

namespace :js_min do
  coyote do |config|
    config.input = "js/application.coffee"
    config.output = "js/application.js"
    config.options = { :quiet => false, :compress => true }
  end
end

# namespace :css do
#   input = "css/screen.less"
#   output = "css/screen.css"
# 
#   coyote do |config|
#     config.input = input
#     config.output = output
#   end
# 
# end
# 
# namespace :css_min do
#   input = "css/screen.less"
#   output = "css/screen.css"
#   coyote do |config|
#     config.options = { :quiet => false, :compress => true }
#     config.input = input
#     config.output = output
#   end

# end