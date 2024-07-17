

## With Dracula theme

--defaults path/to/dracula.yaml
```
pandoc --defaults dracula/dracula.yaml --standalone test1.md -o test.epub
```

## Me

```
pandoc meta.yaml --css styles.css --highlight-style  dracula.theme --standalone test1.md -o test.epub
```



```
pandoc --toc --toc-depth=1 --epub-metadata=metadata.yaml --epub-cover-image=cover.png --css=book.css -o myebook.epub
```