```bash

.
├── config                    # App configuration files
│   ├── sequalize.json        # Sequalize config
│   ├── serviceOne.json       # ServiceOne config
│   └── ...                   # Other configurations
├── servers					  # Or server without sub folder for "serverType" if only one server
│   ├── web
│	│   ├── api					# doc swagger.yaml, etc
│	│   ├── routes
│	│	│	├── controllers     # Request managers
│	│	│	├── middlewares     # Request middlewares
│	│	│	└── routes.js       # Define routes and middlewares here    		
│	│   └── index.js            # Server config loading
│   ├── mobile
│	│   ├── api					# doc swagger.yaml, etc
│	│   ├── routes
│	│	│	├── controllers     # Request managers
│	│	│	├── middlewares     # Request middlewares
│	│	│	└── routes.js       # Define routes and middlewares here    		
│	│   └── index.js            # Server config loading
│   ├── ...						# Other server, (partner,  private, etc)
├── services                   
│   ├── internal			# Business logic implementation 
│   │   ├── handlers		# Listeners/handlers for async tasks
│   │   └── ... 
│   └── external			# External services implementation - (related with API, controllers)
│   └── ...                 
├── db                      # Data access stuff  
│   ├── models              # Models
│   ├── seeds               # Seeds	- (preloading data)
│   └── index.js           	# Init - (Sequalize mostly)
├── libs                    # Customized clients libs and specific class object implementation
│   ├── mqtt         
│   ├── monitor              
│   └── ...                 
├── utils                   # Util/tools libs (methods as formats, validation, helpers, etc)
├── tests                   # Testing
├── package.json           
└── app.js                  # App starting point

```