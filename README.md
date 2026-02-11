# Assignment1_itcs6190_v4.0

What the stack does (2–3 sentences)
The stack first creates a postgres container and initializes a trips table. Then it starts a container and connects to the database using service DNS. It computes the Total number of trips, Average fare per city, and Top N trips by duration and prints the results to stdout and writes the results to out/summary.json

• Exact commands to run/stop
The command to run is: docker compose up --build
The command to stop is: docker compose down -v

• Example output (copy/paste)
app-1  | === Summary ===
app-1  | {
app-1  |   "total_trips": 6,                                                                                                                                                                                               
app-1  |   "avg_fare_by_city": [                                                                                                                                                                                           
app-1  |     {                                                                                                                                                                                                             
app-1  |       "city": "Charlotte",
app-1  |       "avg_fare": 16.25                                                                                                                                                                                           
app-1  |     },
app-1  |     {                                                                                                                                                                                                             
app-1  |       "city": "New York",
app-1  |       "avg_fare": 19.0                                                                                                                                                                                            
app-1  |     },                                                                                                                                                                                                            
app-1  |     {
app-1  |       "city": "San Francisco",                                                                                                                                                                                    
app-1  |       "avg_fare": 20.25                                                                                                                                                                                           
app-1  |     }
app-1  |   ],                                                                                                                                                                                                              
app-1  |   "top_by_minutes": [                                                                                                                                                                                             
app-1  |     {                                                                                                                                                                                                             
app-1  |       "city": "San Francisco",
app-1  |       "minutes": 28,                                                                                                                                                                                              
app-1  |       "fare": 29.3                                                                                                                                                                                                
app-1  |     },
app-1  |     {                                                                                                                                                                                                             
app-1  |       "city": "New York",                                                                                                                                                                                         
app-1  |       "minutes": 26,
app-1  |       "fare": 27.1                                                                                                                                                                                                
app-1  |     },                                                                                                                                                                                                            
app-1  |     {
app-1  |       "city": "Charlotte",                                                                                                                                                                                        
app-1  |       "minutes": 21,                                                                                                                                                                                              
app-1  |       "fare": 20.0
app-1  |     },                                                                                                                                                                                                            
app-1  |     {                                                                                                                                                                                                             
app-1  |       "city": "Charlotte",                                                                                                                                                                                        
app-1  |       "minutes": 12,                                                                                                                                                                                              
app-1  |       "fare": 12.5
app-1  |     },                                                                                                                                                                                           app-1  |     },
app-1  |     {
app-1  |       "city": "Charlotte",
app-1  |       "minutes": 21,
app-1  |       "fare": 20.0
app-1  |     },
app-1  |     {
app-1  |       "city": "Charlotte",
app-1  |       "minutes": 12,
app-1  |       "fare": 12.5
app-1  |     },
app-1  |     {
app-1  |       "city": "San Francisco",
app-1  |       "minutes": 11,
app-1  |       "fare": 11.2
app-1  |     },
app-1  |     {
app-1  |       "city": "New York",
app-1  |       "minutes": 9,
app-1  |       "fare": 10.9
app-1  |     }
app-1  |   ]
app-1  | }
app-1 exited with code 0

• Where outputs are written
The outputs are written to out/summary.json

• Troubleshooting (DB not ready, permission on out/, etc.)
I did not have too many issues. The largest issue I had was indentation and changing the configurations of the compose.yml file to match the file directory since the image in the instructions showed it differently.
