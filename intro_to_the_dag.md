
- mkdir ~/Desktop/gitdag
- cd ~/Desktop/gitdag
- create a git repo in this folder.
```
$ git init
```
```
Initialized empty Git repository in /Users/davis/Desktop/gitdag/.git/
```
- Create a file called helloworld.java and insert the following
```
public class helloworld{

   public helloworld(){
      // Nothing too useful here
   }
   public static void main(String[] args){
      System.out.println("hellworld!");
   }
}
```
- Tell git to track the `helloworld.java` file

```
$ git add helloworld.java
```
- Commit your change into your repo
```
$ git commit -m "initial commit"
```
```
[master (root-commit) d1c6fcd] initial commit
1 file changed, 9 insertions(+)
create mode 100644 helloworld.java
```

- What does your git graph look like right now?

```
git log --graph --decorate --oneline --branches
```

```
* d1c6fcd (HEAD, master) initial commit
```

- It's ALWAYS a bad idea to develop a new feature on the master branch so let's create a feature branch

```
$ git branch feature
```

- Confirm with git that you indeed created this branch

```
$ git branch
```
```
  feature
* master
```

- However the start indicates that you're still in the master branch, so go ahead and checkout the feature branch

```
$ git checkout feature
```
```
Switched to branch 'feature'
```

- What does your git graph look like right now?

```
git log --graph --decorate --oneline --branches
```

```
* d1c6fcd (HEAD, master, feature) initial commit
```

-- Let's make a commit on our feature branch by adding the following to helloworld.java.

```
public void test(){
   System.out.println("look at all the testing I'm doing");
}
```
- Commit your changes
```
$ git add .
$ git commit -m "adding a testing method"
```
```
[feature 26d356a] adding a testing method
 1 file changed, 3 insertions(+)
```

- What does your git graph look like now?





























































































































































































































































































