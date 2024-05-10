# <span style="color: lightblue"> Defining the Basic Directory Structure of our MERN Application and Initializing the Basic Set-Up of Frontend and Backend both the Directories: </span> 


1. Create your new project's directory. 


2. Inside that root directory create ``` "Frontend/" ``` and ``` "Backend/" ``` directory. 


3. In "Frontend" directory initialize a vite react app using this command: 
    > - __Command:__ ``` npm create vite@latest . ```
    > - Choose "react" and "javascript" based template for your Frontend 


4. Now just organize the vite react app's directory structure: 
    > - Delete the .gitignore file and "public/" directory 
    > - Delete default code of "App.jsx" and Remove default .svg images 
    > - Segregate "css" and "components" into different directories inside the "src/" directory 
    > - Only keep one main component "Main.jsx" in the "src/" directory 


5. Now go to the root directory of your project and create "package.json" file there for backend. 
    > - __Command:__ ``` npm init ```
    > - Fill all the package.json file details properly 
    > - Set the ``` "test" ``` script to be ``` "nodemon App.js" ```

  ## * Note:  
  > --> We're not creating the backend's package.json file inside the "Backend/" directory, we're creating it inside the root directory of our project so that it stays easy for us to deploy our frontend and backend together in the end 


6. Download nodemon as a dev dependency for backend 
    - __Command:__ ``` npm i --save-dev nodemon ``` [OR] ``` npm i -D nodemon ```


7. Rename the entry point of package.json as "App.js" and create a App.js file in "Backend/" directory 
 

8. Write a basic server code in App.js: 

<span style="color: lightgreen"> @ My Sample Code: </span>

```
const express = require('express'); 

const app = express(); 
const port = 5000; 

app.listen(port, (err) => {
    if(err){
        console.log(err); 
    } 
    else{
        console.log('Server started successfully.'); 
        console.log(`Listening on port ${port}`); 
        console.log(`Press ctrl and click me: http://localhost:${port}`); 
    }
})
```


9. Now just download express also from npm for your basic backend code to run. 
    - __Command:__ ``` npm i express ```


10. Go to "src/" directory inside the "Frontend/" directory and then download all the basic frontend dependencies which are already mentioned in the Frontend's package.json file by vite 
    - __Command:__ ``` npm i ```


11. Add .gitignore in the root directory of your project and add ``` node_modules ``` name in the ``` .gitignore ``` file. 


12. Initialize a .git repository in your root directory and then create a remote repository on your GitHub account, add the remote to the local .git repo and then do initial commits for the set-up that we have done until now, and then push these commits to the remote repository on GitHub 

<span style="color: lightgreen"> @ Sample Initial Commits: </span> 

```
commit 1c424f904de824303615ba546b438fcc0091a665 (HEAD -> master, origin/master)
Author: Aryan Tomar <aryantomar5000@gmail.com>
Date:   Fri May 10 15:17:37 2024 +0530

    Added .gitignore File for Ignoring node_modules

commit 65c8902e67b5372232d83e2b65035c56fb9c40a2
Author: Aryan Tomar <aryantomar5000@gmail.com>
Date:   Fri May 10 15:13:11 2024 +0530

    Done with Initial Set Up of Frontend directory

commit 1c1870a9d7642fbaf8269068acb1f258d1b37b36
Author: Aryan Tomar <aryantomar5000@gmail.com>
Date:   Fri May 10 15:12:37 2024 +0530

    Done with Initial Set Up of Backend directory
```


13. If you haven't until now, then just open your project's root directory inside the VS Code 
    - Split your code space and terminal space between the frontend and backend directory for better coding experience 


14. For running the backend, run this command inside the terminal which you have opened in the "Backend/" directory: 
    - __Command:__ ``` npm run test ``` [OR] ``` nodemon App.js ``` 


15. For running the frontend, run this command inside the terminal which you have opened in the "src/" directory of "Frontend/" directory: 
    - __Command:__ ``` npm run dev ``` 



