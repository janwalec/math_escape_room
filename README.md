# math_escape_room

Developed with Unreal Engine 5

## Git flow
- Issue  
    Stwórz issue `my issue (#45)`.  
    Tytuł - po angielsku  
    Opis - po polsku  
    Numer po `#` powinien być **o jeden większy** niż poprzednie Issue.  
- Branch  
    Stwórz brancha o tej samej nazwie `moje-issue-(#45)`
- Changes  
    Przełącz się na **swojego brancha**, którego stworzyłeś. Rób zmiany.
- Commit  
    Pierwszego commita nazwij `Closes (#45)`.  
    Jeśli masz kolejne commity to zrób im **squash**.  
    ```
    $ git add .
    $ git commit -m "nowy commit"
    $ git rebase -i HEAD~2
    ```
    
    pojawi się:
    ```
    pick 52740b7 Closes (#1)
    pick 375f03b nowa zmiana
    ```
    zmień na:
    ```
    pick 52740b7 Closes (#1)
    s 375f03b nowa zmiana
    ```
    Zapisz.  

    pojawi się:
    ```
    # This is a combination of 2 commits.
    # This is the 1st commit message:

    Closes (#1)

    # This is the commit message #2:

    nowa zmiana
    ```

    Usuń dodatkową wiadomość
    ```
    # This is a combination of 2 commits.
    # This is the 1st commit message:

    Closes (#1)

    # This is the commit message #2:
    ```

    Na końcu:
    ```
    $ git push --force-with-lease 
    ```

Floww