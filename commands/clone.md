 [на главную](/readme.md)

## clone - создание копии репозитория.

Для начала работы с центральным репозиторием, следует создать копию оригинального проекта со всей его историей локально.

Клонируем репозиторий, используя протокол http:

        git clone http://user@somehost:port/~user/repository/project.git

Клонируем репозиторий с той же машины в директорию myrepo:

        git clone /home/username/project myrepo

Клонируем репозитарий, используя безопасный протокол ssh:

        git clone ssh://user@somehost:port/~user/repository

У git имеется и собственный протокол:

        git clone git://user@somehost:port/~user/repository/project.git/

Импортируем svn репозитарий, используя протокол http:

        git svn clone -s http://repo/location

где -s – понимать стандартные папки SVN (trunk, branches, tags)