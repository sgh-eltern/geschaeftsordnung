file 'geschäftsordnung.css'
file 'Rakefile'

desc "Create HTML"
file 'geschäftsordnung.html' => ['geschäftsordnung.markdown', 'geschäftsordnung.css', 'Rakefile'] do |target|
  sh %(pandoc
         --from markdown
         --output #{target}
         --standalone
         --toc
         --metadata lang=de_DE
         --css geschäftsordnung.css
       geschäftsordnung.markdown).split("\n").join(" \\\n")
end

task default: ['geschäftsordnung.html']
