# README-Solution

There were a lot of new things I learned from this challenge and my main focus was learning more about the environment I was working in. Because this challenges was using Docker as a main technology I tried my best to figure out how it works and why it is important.
Upon my research I learned that docker can actually be quite useful for giving you a shell of the application you are working on. This shell allows you to make changes to the app you are working on without effecting other dependencies you my have in place in larger scale applications. This is how I understood it best.
I have also never used Postman before and when I spent time working on it I learned that you can create a custom API call that will help test the endpoints in your application. This could be beneficial if you are debugging a certain API endpoint within your app because it allows you to isolate the specific endpoint you are working with.

After using these technologies for the first time I can see how they are useful in larger scale environments because it can seen as a Single Responsibility concept. Docker is the shell and Postman is allowing you to test API endpoints to look for any errors.

# Environment Set up
I ran into some trouble setting up Docker in the sense that I already had Postgresql set up on my machine. There was also an issue in the docker-compose.yml file with gaining access to the postgres container as it was looking for a password. I made an edit to this and was able to get in. However; I was getting an error when I tried to access the database directly through a gui. I found that I could just bypass the error by utilizing the rails console to create new entries. I also used Postman to access API endpoints I POST in JSON. This seemed to work for me. I know there is a gui called pgcli that allows you to view the database in depth and would I use that to make things a little easier if I didn't run into any configuration issues with my machine.

#Task 1
In task one I used my past experience at Launch Academy to work through rpsec. We used rspec tests through our apps we developed on our own so I was familiar with this process. The error was occurring in the (email_address.rb) Model as the test needed to account for a proper email validation. I decided to use a (URI::MailTo::EMAIL_REGEXP) which is a shortcut to account for the parameters necessary to be a valid email address. I then used a boolean to account for the valid and invalid response.

#Task 2
I was unable to find the exact solution to this task, but I would like to explain my thought behind it. I know I would need to work in the (email_verification_controller.rb) in order to solve this. Within that controller I would need to work with a GET method in order to retrieve a limit of 10 emails at once. From that point I would have to persist the data to POST to the API endpoint. There would also have to be logic saying that if email count is less than or equal 1 & less than or equal to 10 then post to the API.

#Final Thoughts
With the configuration issues I ran into I feel that I had learn how to work around the database without having a clear way to view the data I had. This was a challenge in itself as I am not familiar with Postman and Docker. I had to rely on my experience with the rails console and experience with API integration. If there is anything else I can explain further as far as my thought process please let me know.
