# webpack-init-

##### Initializing an application using webpack. 
# These are steps to add from start to finish

# In terminal, first initialize node package manager (npm) by typing
npm init

# Then install webpack and webpack command-line-interface (cli)
npm -install webpack webpack-cli --save-dev

# Create  two folders that are namde src and dist, src is the path of our files that we edit and dist is the final folder where webpack generates for us
mkdir dist
mkdir src

# Then we create our webpack config file that has file type of .config.js
ni webpack.config.js

# We will also add a gitignore file that will ignore the node_modules
ni .gitignore

# install the necessary loader for the application
https://webpack.js.org/guides/asset-management/
# for installing CSS, install the required loader
npm install css-loader style-loader --save-dev
# Then, go to webpack config file and setup configuration for css loader
module.exports = {
        module: {
            rules: [
                { 
                   test: /\.(png|jpg|jpeg|svg|gif)$/i,
                   use: ['style-loader', 'css-loader']
            } 
         ]
    }
}

# For auto html generation, using htmlwebpackplugin
https://webpack.js.org/guides/output-management/

# For server and file change listener
https://webpack.js.org/guides/development/
