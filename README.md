# Chingu Solo Project - Tier 3 - Weather CLI
## Notes 
- The requirements for this app is outdated. We are in the process of updating it, but feel free to use this as a project idea
- the current requirement for a tier 3 project can be found [here](https://github.com/chingu-voyages/Handbook/blob/main/docs/guides/soloproject/soloproject.md#1-choose-your-tier-1%EF%B8%8F%E2%83%A3-2%EF%B8%8F%E2%83%A3-3%EF%B8%8F%E2%83%A3) 
```
  Developers should have the following skills & expertise:
- Intermediate or Advanced HTML/CSS/JavaScript/PHP/Python/Ruby/etc. and experience in a framework/library like React, Vue, Angular, etc.
- Understand how to create and use API's with REST or GraphQL API
- Understand how to create backend servers which implement an API of your own design using packages such as Express
- Your Solo Project must implement an FE which accesses a BE server that implements an API of your own design. Optionally uses a database such as a NoSQL DBMS like MongoDB or a SQL DBMS like PostgreSQL
```

## Overview

This project is a great way to practice using JavaScript outside of the browser, utilizing the Node.js runtime.
You will create a package that will take in at least two arguments through the command line, and return a summary of the weather
for the region defined by the argument. It will also write the summary to a file in your
local file system, adding to the end of the file with each call to create a weather record.

*Example*
*Calling the app with the argument `-f` (terse argument for farhenheit) **OR** `-fahrenheit` (verbose argument) would return:*
```
$ node app.js bucharest -f
Current temperature in București, Bucureşti, Romania is 32.41F.
Conditions are currently: Mostly Cloudy.
What you should expect: Partly cloudy throughout the day.

Weather was added to your weather tracking file, weather.txt
$
```

You'll get comfortable with importing and exporting functions, using npm modules, initiating and consuming APIs on
the server side, and hopefuly even more as you explore Node.js. If you already have a lot of experience with Node.js, this will be a great opportunity to show it off and to bring your project to an even higher level by tackling the optional features.

## About Chingu

If you aren’t yet a member of Chingu we invite you to join us. We help our 
members transform what they’ve learned in courses & tutorials into the 
practical experience employers need and want.

Our remote team projects let you refine your technical skills and put them 
into practice while gaining new “soft” skills like communication, 
collaboration, and Agile project management. The types of skills that 
help real-world teams get things done!

You can learn more and join us at [chingu.io](https://chingu.io).

## Instructions & Considerations

This project was designed with Node.js in mind. That being said, if you would like to use a different server-side tool,
please feel free to do so (python, php, etc.). There are **many** ways to complete this project. Here's what to take into
consideration as you plan:

- [ ] You need to make two different API calls. Take a look at the [https module](https://nodejs.org/dist/latest-v12.x/docs/api/https.html) that is built into node. Another great resource is the [request npm package](https://www.npmjs.com/package/request).
- [ ] Great apis to use are [OpenWeather](https://openweathermap.org/api) for actual weather information, and the [geocoding section of
the Mapbox api](https://docs.mapbox.com/api/search/#forward-geocoding) for obtaining coordinates. You will need to obtain a *free* API Key for each service.
- [ ] Remember, API keys are private. Keep them private. Place them in an `.env` file and use them via `process.env`. Here is a 
[*great* article by John Papa](https://medium.com/the-node-js-collection/making-your-node-js-work-everywhere-with-environment-variables-2da8cdf6e786) if you need help!
- [ ] You need to parse your arguments out of the command line. Here's some information about [process.argv](https://nodejs.org/docs/latest/api/process.html#process_process_argv) to help.
- [ ] To accomodate flexibility in your arguments, consider usings an argv parser such as [yargs](https://www.npmjs.com/package/yargs).
- [ ] You will need to require the `fs` module in node, [read this section of the docs for information.](https://nodejs.org/api/fs.html#fs_file_system)

**Requirements**

The following are required to finish the project.

- [ ] A user should be able to type in `node app.js bucharest` and have the current weather printed to the console with the temperature listed in farhenheit and celsius; the same information should be appended to a `weather.txt` file to keep a record of the weather calls made.
- [ ] Your program must accept at least one addition argument in both terse and verbose forms; `-f` or `-farhenheit` and `-c` or `-celsius`
- [ ] Weather needs to include location, the temperature in the requested units, current conditions, and future conditions.
- [ ] Make sure that you handle errors! Account for an API not responding, etc.
- [ ] Your API Keys should NOT be on GitHub, put them in an `.env` file. 
- [ ] Your project files should all be in a GitHub repository with clear instructions on how to set up a local environment.
- [ ] Make sure that your `.env` and `node_modules` are in your `.gitignore` instead of on GitHub.
- [ ] You must have a robust README.md file. 
- [ ] You must submit an image of your command line with the command and the resulting console.log

**Extras**

The following are optional ways to expand on the project should you desire to do so.

- [ ] Use some color in the console.log to help make it more visually appealing.
- [ ] Accept more arguments based on which parts of the weather you want to make accessible.
- [ ] Write your own argument parser instead of creating a dependency on a third-party library. 

**Reference**

Please reach out in the Discord `#ask-cohort-n-code-questions` channel if you have ANY questions at all. We are more than happy to help. In addition,
general instructions for all Pre-Work Projects can also be found in the Chingu Voyage Handbook 
(URL posted in the #read-me-first channel on Discord).
