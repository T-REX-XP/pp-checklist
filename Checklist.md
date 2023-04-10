# Checklist
Some suggestions in that document will be related to the general rules of the pull recuest validation as well.

1. ## Customization
	- Create the customization in `English`, then add necessary localization
	Just follow simple rule, do not mixing the localization during creation the customization.
    - When Optionset added to the solution:
		i. Check that `solution.xml` contains `rootComponent` attribute 
		ii. Check that `Optionsets` folder contains file with name of the optionset
	- When Lookup added:
		i. Check `Other/Relationships.xml`
		ii. Check `Other/Relationships/{EntityName}.xml`
    - When view was not deployed, just check that `Entity.xml` file contains the following attribute: <SavedQueries />
		
2. ## Canvas Apps:
	- Avoid hardcoded messages, always use `Resx` files


3. ## JavaScript/Typescript:
    - Always use namespaces in JS
    - Avoid leave debugger in the production code/. 
	- Avoid hardcoded messages, always use `Resx` files
	- Avoid using eval,aler
	- Avoid using remove CDN for JS libraries
	
4. ## Flows:
   - All connection references should be added to the deployment setting file.
	- Use Scoups inside the flows to handle not only happy path
	- Use Application Insides to catch the logs
	- Divide the complex flows to the several simple flows and reuse the functionality.
		

15. ## PCF Controls
    - Avoid hardcoded messages, always use `Resx` files
	- Always add empty list placeholder
	- Always support disabled mode
	- Always use empty field placesholder: `---`

# ALM
   - Use CI/CD 
   - Minimization of the JS/TS code 
   - PR validation
   - Single source of the truth: The only git repo can be a source of truth
   - Implement Unit/Integration tests

## Basic rules
   - Avoid exposing endpoint without authorization
   - Do not preprocess postprocess hure responsec on the low code side (Canvas app,Flow), it should be implemented in the another layer on the integraiton