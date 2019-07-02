## Fixing Swagger Docs

### Existing Validation Error

Overall, everything seemed to be good.  I think the first issue you were seeing is that some calls like /clients/id ( PUT ) were under the /clients path.  

### Some Other Suggestions

**Parameters**

I also defined the overall parameters that you are using in the swagger in the PARAMETERS section.  I made sure they were used from that dropdown list in the parameters of each operation.  I did notice that some of the existing parameters were different types like INT-32 or INT64 or Number-Double.  I probably suggest on one global type that fits all scenarios like INTEGER.  

**Assembly Invoke**

I did not see any reference to point to the endpoint in the assembly.  I put in a properties placeholder for the endpoint to be proxied against the microservice. So when this is published, it will directly take your path and map it against the service. 

**Base Path**

I added a base path to each service swagger.. when all these are apart of one product, it will allow the api connect gateway to differentiate between each api.  This will allow each swagger to have some of the same paths if they want otherwise, the gateway will not know how to determine which path belongs to which api.  


If you have any questions, please let me know