# DevExtreme_Angular
Reference link:- install the angular (https://angular.io/guide/setup-local) and adding the without adding devextreme/cli
# steps of add devextreme v20.2 on Angular 11.2.5
1. create angular project using create command
      ng new devangu    //devangu is project name  
      
2. Add DevExtreme to an Angular CLI Application (https://js.devexpress.com/Documentation/20_2/Guide/Angular_Components/Getting_Started/Add_DevExtreme_to_an_Angular_CLI_Application/)
		
  Install the devextreme and devextreme-angular npm packages:
      npm install devextreme@20.2 devextreme-angular@20.2 --save --save-exact  
      
3.Then, go to the src folder, open the index.html file, and add the dx-viewport class to the <body> tag.
                        <html lang="en">
														<head>
														</head>
														<body class="dx-viewport">
																<app-root></app-root>
														</body>
												</html>
	
4. Import DevExtreme Modules
	
	Go to the NgModule in which you are going to use DevExtreme UI components and import the required DevExtreme modules.
											import { DxButtonModule } from 'devextreme-angular';     //on  app.module.ts file
											imports: [
																	DxButtonModule
  														  ],
	
	Now you can use the DevExtreme UI component in your application:
						//on	app.component.html file
													<dx-button
															text="Click me"
															(onClick)="helloWorld()">
													</dx-button>	
	
	5. Run the Application
			Run the application with the following command:
									ng serve
			Open http://localhost:4200/ to browse the application.
	
	
####--------- Add the DevExtreme Layout to an Existing Application.-----------####
	
	Reference link:- ( https://js.devexpress.com/Documentation/20_2/Guide/Common/DevExtreme_CLI/#DevExtreme_Application/Add_the_DevExtreme_Layout_to_an_Existing_Application)
	
	1. follow 5 step of add devextreme on angular
	
	2. devextreme add angular-template [--layout][--empty][--resolve-conflicts]
	
							Arguments:
									--layout
									Specifies the DevExtreme layout to add. Available values:															side-nav-outer-toolbar (default)																		side-nav-inner-toolbar																				Both layouts are illustrated in the Layouts article.																--empty																						Specifies whether to skip sample views generation (default: false).														--resolve-conflicts
	
Specifies whether to override the existing app.component or create a component with another name. Available values:
	
									createNew (default)																				override (NOTE: all changes in the overridden files will be lost)
	
	
	
