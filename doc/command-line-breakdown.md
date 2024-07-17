
```
awk 'FNR==1 && NR!=1 {print "\n\n"}{print}' chapters/*.md | tee  | pandoc --toc --toc-depth 2 --webtex --metadata-file metadata.yml   --template templates/epub.html --epub-cover-image images/cover.png -o build/epub/book.epub
```

