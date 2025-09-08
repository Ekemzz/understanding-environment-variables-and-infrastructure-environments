# understanding-environment-variables-and-infrastructure-environments

SUMMARY
Positional arguments in shell scripting are special variables like $1, $2, $3, etc., that represent values passed to a script when it is executed, with $0 being the script name and $@ or $* representing all arguments. They are useful for making scripts dynamic and reusable, since the same script can behave differently depending on the input provided at runtime. When combined with environment variables, positional arguments allow you to pass configuration values—like environment (local, testing, production), file paths, or resource names—without hardcoding them in the script, which is especially important in DevOps automation for flexible and environment-specific deployments.







1. Create an aws cloud manager script file.
   <img width="794" height="452" alt="image" src="https://github.com/user-attachments/assets/04c98e10-7646-43c0-b494-972e7d36ae38" />
2. Code input to the script file.
   <img width="901" height="487" alt="image" src="https://github.com/user-attachments/assets/51145103-5b3f-4c5d-8a06-b2647da2267b" />
3. executable permission were modified into the script.
   <img width="823" height="473" alt="image" src="https://github.com/user-attachments/assets/126cbf7a-7050-4516-9f60-d0f9607c6262" />

without running the script, the script takes arguments from the script. the environment varibale takes on the value of the argument. if the value is local, the script is ran on the local environment. this applies to production, testing environments and if none of the values tally with the above, a statement is echoed to show that no environment was specified.

4. On exporting the production environment, we have this below
   <img width="826" height="476" alt="image" src="https://github.com/user-attachments/assets/23ce399f-a46e-4e06-afd1-cc2e18e4e371" />

   Hard coding the testing environment, we have
   <img width="802" height="470" alt="image" src="https://github.com/user-attachments/assets/92a5d6a9-e56a-429d-b93a-d19ebd630a5f" />
   <img width="804" height="452" alt="image" src="https://github.com/user-attachments/assets/2ab91976-4e05-4968-84b3-77c558079713" />
   The script ignores the Export environment variable and takes on the hard coded testing environment value.

5. Positional parameters
   the bash script is edited to take on the first 1st positional variable.
   <img width="801" height="456" alt="image" src="https://github.com/user-attachments/assets/bc9a8b59-1a3b-481a-9e4f-98d3835cc0db" />
   position variables are ran with the script for local, testing and production as shown in the image below
   <img width="794" height="452" alt="image" src="https://github.com/user-attachments/assets/4aaa8f0c-7524-41aa-a296-faad53f26584" />


