```bash
.
├── config                  # App configuration files
│   ├── index.js            
│   ├── sequelize.js        # Sequelize config
│   ├── serviceOne.js       # ServiceOne config
│   └── ...                 # Other configurations
├── servers					    # Or server without sub folder for "serverType" if only one server
│   ├── web
│	  │   ├── api					# doc swagger.yaml, etc
│	  │   ├── routes
│	  │	  │	  ├── controllers     # Request managers
│	  │	  │	  ├── middlewares     # Request middlewares
│	  │	  │	  └── routes.js       # Define routes and middlewares here    		
│	  │   └── index.js            # Server config loading
│   ├── mobile
│	  │   ├── api					# doc swagger.yaml, etc
│	  │   ├── routes
│	  │ 	│ 	├── controllers     # Request managers
│	  │	  │	  ├── middlewares     # Request middlewares
│	  │	  │	  └── routes.js       # Define routes and middlewares here    		
│	  │   └── index.js            # Server config loading
│   ├── ...						  # Other server, (partner,  private, etc)
├── services                   
│   ├── internal			  # Business logic implementation 
│   │   ├── handlers		# Listeners/handlers for async tasks
│   │   └── ... 
│   ├── external			  # External services implementation - (related with API, controllers)
|   ├── workers         # If multi procces - workers' scripts
│   └── ...             # other logic implementation
├── store                   # Data access stuff  
│   ├── models              # Models - table/collection schema
│   ├── migrations          # Migration scripts
│   ├── seeds               # Seeds	- (preloading data)
│   └── index.js           	# Init - (Sequelize, mongoose, ORM)
├── libs                    # Customized clients libs and specific class object implementation
│   ├── mqtt
│   ├── logger
│   ├── extError
│   ├── monitor              
│   └── ...                 
├── utils                   # Util/tools libs (methods as formats, validation, helpers, etc)
├── tests                   # Testing - setup
├── package.json           
└── app.js                  # App starting point

```

the issue about long path like require('../../../<folder>/<service>') can be handle with the "module-alias" package

There is no "best one" architecture design, the choice depends on the project.

learn more architecture design patterns here: 
- https://blog.risingstack.com/node-hero-node-js-project-structure-tutorial/#the5fundamentalrulesofanodejsprojectstructure
- https://blog.codeship.com/advanced-node-js-project-structure-tutorial/
- https://overflowjs.com/posts/Structure-Nodejs-App-Fractal-Pattern.html
- https://blog.logrocket.com/the-perfect-architecture-flow-for-your-next-node-js-project/
- https://medium.com/codebase/structure-of-a-nodejs-api-project-cdecb46ef3f8
- https://softwareontheroad.com/ideal-nodejs-project-structure/
- https://github.com/talyssonoc/node-api-boilerplate/wiki/Folder-structure
- https://www.npmjs.com/package/module-alias
