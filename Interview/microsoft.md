# Microsoft





## Questions

1. introduce your self

2. descript your current job

3. please explain the architecture (draw it down please)

4. how you do the authentication or authorization for the façade?

5. how to resolve if any high workload problem?

6. what's the achievement of the job

7. how you learn new technologies?

8. how to manage the project with a team

9. if conflict, how to resolve the conflict?

10. how you start for the system

11. do you know DI? how do you use it? why it is important in tests?

12. do you know IDispose?

13. 程式題

    " Given an array of string, write a function to find the longest common prefix of this array.

    Example input - 
    ["microsoft","mice","mitigate"]

    Example output - "mi"

    

    

    ## 回答

    第3題


    User service (lambda)	Device service 		Product service 
    	worker (docker)		worker (docker)		worker (docker)
    	/////////////////////////////////////////////////////////////////////////	
    					AWS IoT core with MQTT 
    	/////////////////////////////////////////////////////////////////////////
    					Mediator pattern
    				AWS Lambda	+	Dynamo DB 
    					
    			Facad service	+	API-Gateway
    						
    				1. X.509 for APP + oAuth
    	/////////////////////////////////////////////////////////////////////////
    		iOS APP 		Android App		Air device

​    程式題
​    

```c#

public static  string takeLogest(List<string> input)
{
    //["microsoft","mice","mitigate"]
    //{abc,ade,ty}
    string target = string.Empty;

    for (int i = 0; i < input[0].Length; i++)
    {
        target += input[0][i];
        //a
        for (int j = 0; j < input.Count; j++)
        {
            if (input[j].StartsWith(target))
                continue;
            else
                return target;
        }
    }

    return target;
}
```

