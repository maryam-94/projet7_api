# projet7_api

To see deplyed app in heroku :
https://oc-projet7-api.herokuapp.com/

## important use these versions:
```
pip install lightgbm==2.2.3
pip install joblib==1.2.0
```
# to see pip version:
````commandline
pip show joblib
````
## to generate _"requirements.txt"_ file:
```
pipreqs --force
```

## API documentation :

1. GET http://localhost:5000/ :
   - **returns** text hello

2. GET 'http://localhost:5000/user/random'
   - **returns** random user data (with all variables)
   - returns les informations des variables (585) sur un utilisateur random

3. GET 'http://localhost:5000/user/<sk_id>'
   - avec <sk_id> est une variable à remplir lors de l'appel.
   - **Exemple** : 'http://localhost:5000/user/100001'
   - **returns** les informations des variables (585) sur l'utlisateur envoyé en paramétre

4. GET 'http://localhost:5000/optimum_threshold
   - **returns** the optimum 
   - **Exemple** retour : `{"optimum_threshold": 0.106}`


5. POST http://localhost:5000/predict
   - **body** il faut envoyer dans le body de la requéte les information du user par exemple à partir de la requéte 3 ou 2  
returns prediction avec optimum 


6. GET 'http://localhost:5000/predict/user/<sk_id>'
   - **exemple** : http://localhost:5000/predict/user/100001
   - Pas besoin de lui envoyer les 585 variables il les prends automatiquement à partir du dataframe
returns prediction avec optimum 

