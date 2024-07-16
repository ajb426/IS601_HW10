# Event Manager Company: Software QA Analyst/Developer Onboarding Assignment

## Links to Issues
https://github.com/ajb426/IS601_HW10/issues?q=is%3Aissue

## image in Dockerhub
https://hub.docker.com/repository/docker/ajb426/is601_hw10/tags

## Reflection
This project helped teach me a lot about API's function and the different layers involved in having a functional API. In this specific implementation, we had a service layer, a schema layer, and then the model layer, each responsible for different parts of processing requests.
This understanding was fundamental in resolving the issues assigned to us and providing robust and thorough solutions required that understanding. The username validation and uniqueness changes are good examples of solutions that required changes in all three layers. To require the
username to be a certain length and not contain any special characters, the user_schema must be updated to perform this validation so invalid data is checked before being sent to the table. Then to ensure the username's uniqueness I updated the user_service to do a check for duplicates on the nickname, to see if it was already in the user's table, as well as having the user model specify the nickname field as unique. Having that specified will ensure the db does not insert or update any records if the nickname field is a duplicate. Implementing these solutions across multiple layers adds a layer of redundancy and robustness to the API, ensuring users who interact with it have an error-free experience.

The other part of this project that stood out to me, was increasing the test coverage, and implementing the GitHub action workflow. Increasing the test coverage proved a challenge as a lot of the code was already covered in existing tests, and providing additional tests for the code that was not covered turned into a task of trial and error. After some time I was able to reach the 90% mark, but it was a tedious effort for the most part. Getting the Github actions workflow to publish to DockerHub successfully was also difficult, and it required some additional knowledge of setting up secrets in the .yml file and having those loaded into the dockerbuild successfully. The SMTP credentials specifically are what gave me trouble and it required some research to find out how to have those values populate correctly in a GitHub action. Now I have a better understanding of how the GitHub actions work and see their value from a CI/CD perspective.

Overall I thought this project was interesting, and I learned a lot throughout my completion of it.
