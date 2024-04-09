<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=angular,spring,mysql,postman,bootstrap,vscode,idea" />
  </a>
</p>  

> [!NOTE]
> Angular + Spring Boot  
> MySQL  
> Postman
> VSCode + IntelliJ  

### API  

| REQUEST | API URL                                                      |
|  :---:  | :----------------------------------------------------------: |
| $${\color{blue}GET}$$     | https://localhost:8080/employee/all        |
| $${\color{blue}GET}$$     | https://localhost:8080/employee/find/{id}  |
| $${\color{green}POST}$$   | https://localhost:8080/employee/add        |
| $${\color{orange}PUT}$$   | https://localhost:8080/employee/update     |
| $${\color{red}DELETE}$$   | https://localhost:8080/employee/delete     |  

### CORS Policy bypass  
```
@Bean
	public CorsFilter corsFilter(){
		CorsConfiguration corsConfiguration = new CorsConfiguration();
		corsConfiguration.setAllowCredentials(true);
		corsConfiguration.setAllowedOrigins(Arrays.asList("http://localhost:4200"));
		corsConfiguration.setAllowedHeaders(Arrays.asList("Origin", "Access-Control-Allow-Origin", "Content-Type",
				"Accept", "Authorization", "Origin, Accept", "X-Requested-With",
				"Access-Control-Request-Method", "Access-Control-Request-Headers"));
		corsConfiguration.setExposedHeaders(Arrays.asList("Origin", "Content-Type", "Accept", "Authorization",
				"Access-Control-Allow-Origin", "Access-Control-Allow-Origin", "Access-Control-Allow-Credentials"));
		corsConfiguration.setAllowedMethods(Arrays.asList("GET", "POST", "PUT", "DELETE", "OPTIONS"));
		UrlBasedCorsConfigurationSource urlBasedCorsConfigurationSource = new UrlBasedCorsConfigurationSource();
		urlBasedCorsConfigurationSource.registerCorsConfiguration("/**", corsConfiguration);
		return new CorsFilter(urlBasedCorsConfigurationSource);
	}
```  

### tsconfig.json  
```
"compilerOptions": {
    "strictPropertyInitialization": false,	// variable initializer
    "strictNullChecks": false,			// nulable obj
}
```  


