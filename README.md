# Open Lab website template

For use in all your Open Lab projects - simple to set up and serve. Just fill in your project info. 

## Initialise

``` bash
# clone the repo
git clone https://github.com/xynosis/oltemplate.git

# install pug and sass
npm install -D sass-loader node-sass pug

# install other dependencies
npm install
```

To view your site locally:

``` bash
npm run dev
```

This will allow the site to hot-reload, meaning that it changes as you edit your code and save.

## Add your project's details

1. Navigate to: 
    ``` 
    oltemplate
    |-- index.html
    ```

    Locate 'change me to project name' and do so.

2. Navigate to:
    ```
    oltemplate
    |-- assets
        |-- style.sass
    ```

    Change the hex codes after ```$dark```, ```$base``` and ```$light``` to colours of your choice. Generally, the light colour should be quite bright, and the dark colour should only be a little darker than the base.

    https://pigment.shapefactory.co/ is good for identifying complementary colour combinations.

3.  Using the hex codes of your ```$dark``` and ```$light``` colours, navigate to this URL:
    https://duotone.shapefactory.co/?f=insertdarkhere&t=insertlighthere, e.g. 
    https://duotone.shapefactory.co/?f=2B3948&t=6AAAAE. Select an appropriate picture or upload one of your own, then download it (this seems to only work properly on Google Chrome).
    
    Navigate to your assets folder and delete home.png. Copy the downloaded file in as home.png. 

    ```
    oltemplate
    |-- assets
        |-- home.png
    ```

4. Navigate to:
    ```
    oltemplate
    |-- src
        |-- App.vue
    ```

    Change the name of the project in the ```script``` section to the name of your project.

5. Navigate to:
    ```
    oltemplate
    |-- src
        |-- components
            |-- Home.vue
    ```

    Fill in the relevant information or delete as appropriate.

6. Navigate to:
    ```
    oltemplate
    |-- src
        |-- components
            |-- About.vue
    ```

    Fill in the relevant information or delete as appropriate.

7. Navigate to:
    ```
    oltemplate
    |-- src
        |-- components
            |-- Info.vue
    ```

    Fill in the relevant information or delete as appropriate.

8. If your project does not have any 'actions' you would like users of the site to perform, navigate to:
    ```
    oltemplate
    |-- src
        |-- App.vue
    ```
     and remove lines 16, 17 and 22 (lines concerning the action button).
    
## Serve the site

1. Build the site: 

    ``` bash
    npm run build
    ```

2. Find an appropriate web host. If this is a simple project, try GitHub pages. There are tutorials for how to host on GitHub pages elsewhere on the web, or ask someone in the lab (including me!).

3. Copy the contents of the following folder to your host:

    ```
    oltemplate
    |--dist
    ```

    This should be a folder called ```static``` and an ```index.html``` file. 

4. Next steps will depend on your web host, but if you've copied to GitHub pages your site should now be live at either: 
    - http://_username_.github.io
    or
    - http://_username_.github.io/_projectname_

## Known issues

- Logos bunch up in mobile view.
- Open Lab map is cut off screen in mobile view.