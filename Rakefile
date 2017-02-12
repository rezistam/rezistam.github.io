require 'html-proofer'

desc 'rake task to test built pages'
task :default do
  sh "bundle exec jekyll build --drafts"

  options = {
    check_html: true,
    empty_alt_ignore: true
  }

  HTMLProofer.check_directory("./_site", options).run
end