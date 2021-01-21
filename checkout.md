[< back to contents](./readme.md)

# git checkout

**git checkout *[branchname]*** - Переключение между ветками или восстановление файлов из рабочего каталога


Вызов ветки по хэшу коммита
```bash
git checkout <hash>
```

Возвращение на последнюю версию ветки master
```bash
git checkout master
```

Отмена изменений до коммита
```bash
git checkout [filename]
```

Откат проиндексированного нежелательного изменения:

```bash
git add [file] #индексация файла
git restore [file] #откат проиндексированного файла
git checkout [file] #Изменение нежелательного изменения в рабочей папке
```

```bash
git revert HEAD #Отменяет изменения в последнем нежелательном коммите
git revert <hash> #отменяет изменения внесенные коммитом с хэшем
```

Shortcut for `git branch <branchname>` following `git checkout <branchname>` 
```bash
git checkout -b <branchname>
```

[<Previous](./aliases.md) ... [Next>](.)