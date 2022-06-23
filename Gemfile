require 'yaml'
source 'https://rubygems.org'

gem 'yard'
YAML.load(File.read(__dir__ + '/gem-lists.yaml')).each do |gem_name, gem_opt|
  args = []
  kwargs = {}
  
  gem_data = gem_opt['gem']
  args.concat gem_data['version'] if gem_data.key?('version')
  kwargs.update(gem_data['source'])
  
  gem gem_name, *args, **kwargs
end
