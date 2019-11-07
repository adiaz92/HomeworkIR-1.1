# HomeworkIR-1.1

Test of Basic commands for github

##

We make a clone of the new repository.
```
git clone https://github.com/adiaz92/HomeworkIR-1.1.git

Clonando en 'HomeworkIR-1.1'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Desempaquetando objetos: 100% (3/3), listo.
```
Then we create the file "txtfile1.txt" and add it to the repository, also we make a commit for explain what we are doing.
```
~$ cd HomeworkIR-1.1/
~/HomeworkIR-1.1$ git add txtfile1.txt
~/HomeworkIR-1.1$ git commit -a -m "Adding txtfile1 for test"
[master e598359] Adding txtfile1 for test
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 txtfile1.txt
```
After that we make a push to upload the changes.
```
~/HomeworkIR-1.1$ git push origin master 
Username for 'https://github.com': adiaz92
Password for 'https://adiaz92@github.com': 

Contando objetos: 3, listo.
Delta compression using up to 12 threads.
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 283 bytes | 283.00 KiB/s, listo.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/adiaz92/HomeworkIR-1.1.git
   93610ea..e598359  master -> master
```
We are going to modify the file "txtfile1.txt" in the github web and use the pull command update the changes in our computer.
```
~/HomeworkIR-1.1$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Desempaquetando objetos: 100% (3/3), listo.
Desde https://github.com/adiaz92/HomeworkIR-1.1
   e598359..ed805a3  master     -> origin/master
Actualizando e598359..ed805a3
Fast-forward
 txtfile1.txt | 1 +
 1 file changed, 1 insertion(+)
```
Now, we create a branch of this project and modify the file in order to check that the changes are make only in the branch.
```
~/HomeworkIR-1.1$ git checkout -b newbranchtest
Cambiado a nueva rama 'newbranchtest'

~/HomeworkIR-1.1$ git commit -a -m "Adding a new line on txtfile1 for a new branch test"
[newbranchtest e90b103] Adding a new line on txtfile1 for a new branch test
 1 file changed, 2 insertions(+)

~/HomeworkIR-1.1$ git push origin newbranchtest 
Contando objetos: 3, listo.
Delta compression using up to 12 threads.
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 363 bytes | 363.00 KiB/s, listo.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'newbranchtest' on GitHub by visiting:
remote:      https://github.com/adiaz92/HomeworkIR-1.1/pull/new/newbranchtest
remote: 
To https://github.com/adiaz92/HomeworkIR-1.1.git
 * [new branch]      newbranchtest -> newbranchtest
```
After we check that the changes has been uploaded only in the branch, we are going to merge the branch with the master.
```

~/HomeworkIR-1.1$ git merge newbranchtest 
Actualizando ed805a3..e90b103
Fast-forward
 txtfile1.txt | 2 ++
 1 file changed, 2 insertions(+)

~/HomeworkIR-1.1$ git push origin master
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/adiaz92/HomeworkIR-1.1.git
   ed805a3..e90b103  master -> master
```
Also we eliminate the branch and see in which status is.
```
~/HomeworkIR-1.1$ git branch -d newbranchtest 
Eliminada la rama newbranchtest (era e90b103)..

~/HomeworkIR-1.1$ git status
En la rama master
Tu rama está actualizada con 'origin/master'.

nada para hacer commit, el árbol de trabajo esta limpio

```
