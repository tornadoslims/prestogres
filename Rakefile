require 'bundler'
Bundler::GemHelper.install_tasks

require 'rake/extensiontask'

spec = eval File.read("presto-pggw.gemspec")
Rake::ExtensionTask.new('presto-pggw', spec) do |ext|
  ext.cross_compile = true
  ext.lib_dir = File.join(*['lib', 'presto-pggw', ENV['FAT_DIR']].compact)
  #ext.cross_platform = 'i386-mswin32'
end

task :default => [:build]