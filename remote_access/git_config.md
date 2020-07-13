 [на главную](/readme.md)

## Описание файла .gitconfig

В состав Git входит утилита **git config**, которая позволяет просматривать и настраивать параметры, контролирующие все аспекты работы Git, а также его внешний вид. Эти параметры могут быть сохранены в трёх местах:

Файл */etc/gitconfig* содержит значения, общие для всех пользователей системы и для всех их репозиториев. Если при запуске git config указать параметр --system, то параметры будут читаться и сохраняться именно в этот файл.

Файл *~/.gitconfig* или *~/.config/git/config* хранит настройки конкретного пользователя. Этот файл используется при указании параметра **--global.**

Файл **config** в каталоге Git (т.е. .git/config) репозитория, который вы используете в данный момент, хранит настройки конкретного репозитория.

Настройки на каждом следующем уровне подменяют настройки из предыдущих уровней, то есть значения в .**git/config** перекрывают соответствующие значения в **/etc/gitconfig**.

Пример файла:

    [core]
        quotepath = false
        pager = less -r
        abbrev = 8
        editor = nano -ixO -r72
    [format]
        pretty = Commit: %h%d%nAuthor: %an <%ae> %nDate:   %ad%C(reset)%n%n%w(72,2,2)%s%n%n%w(0,2,2)%-b%n
    [user]
        name = <Firstname> <Surname>
        email = <username@email.com>
        signingkey = <key>
    [push]
        default = simple
    [color "branch"]
        current = 207 bold
        local = 40 bold
        remote = 203 bold
    [color "diff"]
        meta = 207 bold
        frag = 207 bold
        old = 203 bold
        new = 40 bold
        whitespace = 40 reverse
    [color "status"]
        added = 40 bold
        changed = 207 bold
        untracked = 203 bold