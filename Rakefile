require "rake"

begin
  require "jeweler"
  Jeweler::Tasks.new do |gem|
    gem.name = "less-rails"
    gem.summary = "Using Less CSS Framework with Rails"
    gem.email = "nicolas.merouze@gmail.com"
    gem.homepage = "http://github.com/yeastymobs/less-rails"
    gem.authors = ["Karst Hammer", "Nicolas Mérouze", "Mathieu Fosse", "Tim Harvey"]
    gem.files = Dir["*", "lib/**/*"]
    
    gem.add_dependency("less", "~> 1.2.21")
  end
  
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end