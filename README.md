# Configurar-React-WebPack-Babel7
Como configurar un proyecto en React utilizando webPack y Babel7

omandos
npm init -y


npm install webpack -D
npm install webpack-cli -D
npm install react react-dom --save-dev
npm install --save-dev webpack-dev-server 

npm install --save-dev  @babel/core  @babel/preset-env @babel/preset-react  babel-loader  



/*Crear un archivo llamado .babelrc* para configurar babel y colococar este codigo.
{
  "presets" : [ "@ babel / preset-env" , "@ babel / preset-react" ]  
}
Crear un archivo llamado webpack.config.js y colocar esto:

module.exports = {
    entry:'./src/app/index.js',
    output:{
        path:__dirname+'/src/public',
        filename:'bundle.js'
    },
    module: {
        rules: [
          {
            test: /\.(js|jsx)$/,
            exclude: /node_modules/,
            use: ['babel-loader']
          }
        ]
      }
  };


