This is the System Layer of the Pokemon DDBB, it contains the interface and implements of the HTTP methods for:
- Get All Pokemons in the DDBB "/api/pokemon"
- Get the Pokemon with specified ID "/api/pokemon/ID"
- Get the Pokemons with specified type "/api/pokemon/tipo?tipo=type"
- Get the Pokemons of specified generation "/api/pokemon/generacion?gen=generation"
- Get the Pokemon with the specified name "/api/pokemon/nombre?nombre=name"
- Update the "MainType" of the specified ID Pokemon "/api/pokemon/ID/tipo1?tipo1=MainType"
- Update the "SecondaryType" of the specified ID Pokemon "/api/pokemon/ID/tipo1?tipo2=SecondaryType"
- Update the "generation" of the specified ID Pokemon "/api/pokemon/ID/generacion?gen=generation"
- Post the Pokemon with the specified "name", "MainType" ("SecondaryType" and "Gen" are optional) "/api/pokemon?nombre=name&tipo1=MainType&tipo2=SecondaryType&gen=generation"
- Delete the Pokemon with the specified ID "/api/pokemon/ID"
- Train (Patch) the specified ID Pokemon with a numeric ammount of xp "/api/pokemon/ID/entrenar?xp=xp"
- Teach (Patch) the specified ID Pokemon the specified move "/api/pokemon/ID/aprender?mov=move"
- Forget (Patch) the specified ID Pokemon the move in the positional slot (mov1 - mov4)  "/api/pokemon/ID/olvidar?move"

This is the experience layer and it serves as a filter to validate the inputs of the HTTP methods, it will throw errors when the inputs or the sql syntax is wrong so it won't make calls to inner layers, reducing the traffic and the resources consumption
