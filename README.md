# Project Overview


## Project Description

App that uses a brewery api to allow a user to search for local breweries in their area.  It will have a homepage with a header that is displayed on all of the pages.  It will have a main section that will allow the user to search by name or location.  Once the user makes a choice it will display the search bar.  The user then can type in the name/city and the api will display all the breweries that fit the search criteria. 

I may face some issues with the search bar and getting it to display the data. I will reference other labs and homework to help me figure out how to get the search bar to work.  I may have some issues with the CSS because I haven't been focusing as much on it with the last several assignments.  I will review older work i have done as a reference on how to work with the CSS.  I will also see if I can google if there are any specific ways i should be working with CSS and react. I may run into some problems with displaying multiple breweries at once vs just one at a time depending on what a user searches.


## Project Links

- [repo](https://github.com/hrocco25/brewery)
- [deployment](https://heatherbreweryapp2.herokuapp.com/)
- [API](https://www.openbrewerydb.org/documentation/01-listbreweries)


## Wireframes

// i need to upload new pictures

<img src="https://user-images.githubusercontent.com/49919405/71772381-6f7d9880-2f07-11ea-9d5f-458e0a8031ae.jpg" height='200' width='200'>

- [react architecture]()


#### MVP EXAMPLE
Home page with search bar to search through the api to find a brewery.  Once you hit the search button it will display all the results.  The results will include the name of the brewery, address, website link, and phone number.

#### PostMVP EXAMPLE

- Add search for specific criteria 
- Save favorite breweries 
- Search for both city and state at the same time to narrow search results
- Add pagination 

## Components
##### Writing out your components and its descriptions isn't a required part of the proposal but can be helpful.

Based on the initial logic defined in the previous sections try and breakdown the logic further into stateless/stateful components. 

| Component | Description | 
| --- | :---: |  
| App | It has React Router and links back to home page| 
| Header | This will render the header include the title of app, icon, and main img | 
| Main | This includes the main section with links to the location and name search| 
| Search | This will render the search bar | 
| Name | This updates text for Name and SearchName | 
| SearchName | It fetches the api data depending on what is typed into the search  | 
| Location | This updates text for search and SearchLocation | 
| SearchLocation | It fetches the api data depending on what is typed into the search | 
| Footer | This will render the header include the footer info | 

## Time Frames


| Component | Priority | Estimated Time | Time Invested | Actual Time |
| --- | :---: |  :---: | :---: | :---: |
| Planning | H | 3hrs| 2hrs | 2hrs |
| Working with API | H | 2 hrs| 2hrs | 2hrs |
| CSS and formating | H | 5hrs| 4hrs | 5hrs |
| App | H | 1 hrs| .5hrs | .5hrs |
| Header | H | 3 hrs| 1hrs | 1hrs |
| Main | H | 4 hrs| 1hrs | 1hrs |
| Search | H | 6 hrs| 7hrs | 7hrs |
| Footer | H | 1 hrs| .2hrs | .2hrs |
| Total | H | 31hrs| 18.7hrs | 18.7hrs |


## Code Snippet

```
handleOnInputChange = (e) => {
	const query = e.target.value
	if ( ! query ){
		this.setState( { query, results: {}} )
	} else{
		this.setState ( { query }, () =>{
		this.fetchSearchResults( query )
	} ) 
	}
}// this function is called when a user inputs text into the search bar
	
```

```
<a className='name' href= { result.website_url } target="_blank" rel="noopener noreferrer">{result.name}</a>
//I was able to get the name of the brewery to be a link 
	
```

## Issues and Resolutions
 Use this section to list of all major issues encountered and their resolution.

#### SAMPLE.....
**ERROR**: webpackHotDevClient.js:120 ./src/components/search/searchLocation.js
  Line 49:82:  Using target="_blank" without rel="noopener noreferrer" is a security risk: see https://mathiasbynens.github.io/rel-noopener  react/jsx-no-target-blank

**RESOLUTION**: Needed to add '''rel="noopener noreferrer"''' to the <a> tag

