# access_control-ACL

============================================================================

https://travis-ci.com/Alwynblake/401n12-lab14

### Author: Alistair Blake

### Links and Resources
repo https://github.com/Alwynblake/401n12-lab14
https://travis-ci.com/Alwynblake/401n12-lab14
back-end
front-end https://lab4-401n12.herokuapp.com/
## Canvas Submission
* Link to the README.md in your lab repo
* **Code Sandbox Submissions**
  * Create a folder called `docs` (under `/public` for React apps)
  * Upload your README.md and any supportive images to this folder.
  * Submit a link to your `/docs/README.md` for your canvas submission
  
## Overview
Implement Role Based Authentication

## Feature Tasks – Server
Create a new router that contains a few new routes that we can protect using our authentication model.
Protect your New Routes with the proper permissions based on user capability
router.get('/public-stuff') should be visible by anyone
router.get('/hidden-stuff') should require only a valid login
router.get('/something-to-read') should require the read capability
router.post('/create-a-thing) should require the create capability
router.put('/update) should require the update capability
router.patch('/jp) should require the update capability
router.delete('/bye-bye) should require the delete capability
router.get('/everything') should require the superuser capability
You will need to restrict based on the given permission via middleware
Implementation of the ACL itself should be completed as a separate model populated virtually (not as a hard-coded table within the User Model as done in the demo)
Hint: This might impact the .can() function and how you build out the token
You will need to create, allocate, and identify roles and capabilities permissions in a new collection called ‘roles’ in your mongoose database

## Deployment - Server Based Labs
 * Your server must be deployed at Heroku
 * If it requires a database, provision it
 * For APIs, your endpoints should all be testable remotely using httpie or postman
 * For Web Servers, your website must be reachable

## Testing
 * Write a complete set of tests for all data models, independent of the server
 * For testing the server and routes, use `supertest` to do end-to-end testing
   * What we're testing is not whether express works, but whether your routes are doing the correct things.
 * Your tests must be running green on travis.com
 
