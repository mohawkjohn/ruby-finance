# Look in the tasks/setup.rb file for the various options that can be
# configured in this Rakefile. The .rake files in the tasks directory
# are where the options are used.

begin
  require 'bones'
  Bones.setup
rescue LoadError
  begin
    load 'tasks/setup.rb'
  rescue LoadError
    raise RuntimeError, '### please install the "bones" gem ###'
  end
end

ensure_in_path 'lib'
require 'finance'

task :default => 'spec:run'

PROJ.name = 'finance'
PROJ.authors = 'Steve Walker'
PROJ.email = 'swalker@walkertek.com'
PROJ.url = 'http://www.stephenwalker.com'
PROJ.version = Finance::VERSION
PROJ.rubyforge.name = 'finance'

PROJ.spec.opts << '--color'

# EOF
