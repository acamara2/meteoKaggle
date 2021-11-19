# meteoKaggle
Ce répertoire contient l'ensemble des notebooks réalisés en vue de participer au Kaggle organisé par Meteo France

Etape 0: 
* Prise en main du projet notamment en regardant les notebooks présents dans le dossier prise en main :
      ./prise_en_main/open-mask-data.ipynb
      ./prise_en_main/open-x-forecast-3d-test.ipynb
      ./prise_en_main/open-x-forecast-3d-train.ipynb
      ./prise_en_main/open-y-and-baselines.ipynb
      ./prise_en_main/compute-baseline-obs.ipynb
      ./prise_en_main/open-x-forecast-2d-train.ipynb
      ./prise_en_main/open-x-station.ipynb
      ./prise_en_main/open-x-forecast-2d-test.ipynb
Etape 1 : 
* Travail juste avec les données X_station_train.csv et Y_station_train.csv :
    Méthodologie de représentation des données et premiers algorithmes :
    Etape 1.1 :
        Forme des données :
           La structure des données X_station_train est la suivante : 
           Pour chaque Station et pour chaque jour : pour les paramètres ff,dd,t,hu,td je calcule le min, max, mean, std au cours de la journée
                                                     pour le paramètre prediction, on regarde la quantitée de précipitation de la veille
                                                     ensuite je rajoute les paramètres géographiques et d'identité.
          ce qui donne par exemple le formatage suivant :
          numberStation_dayIndex = ['number_sta', 'ff_mean', 'ff_min', 'ff_max', 'ff_std', 't_mean',
         't_min', 't_max', 't_std', 'td_mean', 'td_min', 'td_max', 'td_std',
         'hu_mean', 'hu_min', 'hu_max', 'hu_std', 'dd_mean', 'dd_min', 'dd_max',
         'dd_std', 'Prediction', 'day_index', 'Id', 'lat', 'lon', 'height_sta',
         'month', 'day'],
       Algorithme utilisé :
        * Linear regression
        * Random Forest
        * SVM.SVR
       
       
      
    
    