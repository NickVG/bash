ps -ef > ps ax
ps -ef ~ ps aux
ps auxw - раширить поле вывода
ps auxww - не ограничивать вывод
f - добаить дерево процессов
-o определить формат вывода
-L - вывести треды(threads)

pstree (это программы по умолчанию нет)

strace

в дополнение к ***screen*** или ***tmux*** можно исопльзовать ***nohup***

fork bomb: :(){ :|:& };:

/lib64/ld-2.16.so /bin/ls

nsenter  войти в другой namespace
unshare - запустить процесс в изолированном namespace
