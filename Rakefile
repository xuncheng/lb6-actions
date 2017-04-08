desc 'Build launchbar actions'
task :build do
  system "rm -rf build && mkdir build"

  File.new("MANIFEST", "r").read.split("\n").each do |file|
    system "/usr/bin/zip -r -q 'build/#{file}.zip' '#{file}'"
    system "mv 'build/#{file}.zip' 'build/#{file}'"
  end
end
task :default => :build
