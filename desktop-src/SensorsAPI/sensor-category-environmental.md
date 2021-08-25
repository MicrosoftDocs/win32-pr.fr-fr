---
description: La catégorie d’environnement de catégorie de capteur \_ contient des \_ capteurs qui fournissent des informations sur l’environnement environnant ou la météo.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7cc2a6ca1d2832045a77f0a2ffa1902732e484700afaacd757719e99d667c55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126609"
---
# <a name="sensor_category_environmental"></a>\_environnement de catégorie de capteur \_

La catégorie d’environnement de catégorie de capteur \_ contient des \_ capteurs qui fournissent des informations sur l’environnement environnant ou la météo.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                                                                                     | Description               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**Capteur \_ TYPE \_ \_ \_ pression atmosphérique environnementale**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barometers.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**Capteur \_ TYPE \_ d' \_ humidité**</dt> de l’environnement <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Hygrometers.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**Capteur \_ TYPE \_ de \_ température**</dt> de l’environnement <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Des thermomètres<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**Capteur \_ SAISIR \_ la \_ \_ direction du vent environnemental**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Aubes climatiques.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**Capteur \_ TAPER \_ la \_ \_ Vitesse du vent**</dt> de l’environnement <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemometers.<br/>   |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur GUID de l' \_ \_ \_ environnement \_ :

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**Capteur \_ \_Barre de \_ \_ pression atmosphérique \_ du type de données**</dt> <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Pression atmosphérique dans les atmosphères (barres).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ température en \_ degrés Celsius**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Température en degrés Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**Capteur \_ \_Pourcentage d' \_ \_ humidité relative \_ du type de données**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Humidité relative sous forme de pourcentage.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ sens du vent \_ \_ \_ dans**</dt> le sens inverse des aiguilles d’une montre <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Direction du vent par rapport au nord magnétique, en degrés. Le nord est représenté sous la forme 0,0 (en haut de l’axe des X), avec des valeurs qui s’améliorent dans une rotation en sens inverse des aiguilles d’une montre. L’axe Z pointe vers le haut. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**Capteur \_ Compteurs de vitesse de vent des types de données \_ \_ \_ \_ \_ par \_ seconde**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Vitesse du vent en mètres par seconde.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




