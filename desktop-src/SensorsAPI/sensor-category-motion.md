---
description: La \_ catégorie de mouvement catégorie de capteur contient des \_ capteurs qui fournissent des informations relatives au déplacement physique.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edcb1b5f0a6d02c481774d18ee111ad4ca5e5cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542893"
---
# <a name="sensor_category_motion"></a>\_mouvement de catégorie de capteur \_

La \_ catégorie de mouvement catégorie de capteur contient des \_ capteurs qui fournissent des informations relatives au déplacement physique. Les accéléromètres mesurent l’accélération du capteur, y compris l’accélération gravitationnelle. Des détecteurs de mouvement, tels que la détection des mouvements humains dans un système de sécurité, le sens du déplacement des objets. Gyrometers sens des modifications de la vélocité angulaire. Les indicateurs de vitesse mesurent la vélocité.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                              | Description                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**Capteur \_ TAPEZ \_ accéléromètre \_ 1J**</dt> <dt>{C04D2387-7340-4CC2-991e-3B18CB8EF2F4}</dt> </dl> | Accéléromètres à un axe.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**Capteur \_ TAPEZ \_ accéléromètre \_ 2J**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Accéléromètres à deux axes.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**Capteur \_ TAPEZ \_ accéléromètre \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Accéléromètres à trois axes.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**Capteur \_ TAPEZ \_ gyromètre \_ 1J**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Gyrometers à un axe.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**Capteur \_ TAPEZ \_ gyromètre \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Gyrometers à deux axes.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**Capteur \_ TAPEZ \_ gyromètre \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Gyrometers à trois axes.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**Capteur \_ \_ \_ Détecteur de mouvement de type**</dt> <dt>{5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Des détecteurs de mouvement, tels que ceux utilisés dans les systèmes de sécurité.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**Capteur \_ \_Indicateur de type**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Capteurs de vitesse de mouvement.<br/>                                   |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le GUID de mouvement de type de données de capteur \_ \_ \_ \_ :

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                                                                                                               | Description                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**Capteur \_ Accélération de type de données \_ \_ \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accélération de l’axe X, en *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**Capteur \_ Accélération de type de données \_ \_ \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accélération de l’axe Y, en *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**Capteur \_ Accélération de type de données \_ \_ \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accélération de l’axe Z, en *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**Capteur \_ \_Accélération angulaire de type de données \_ \_ \_ X \_ degrés \_ par \_ seconde \_ carré**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Accélération de l’axe x Gyrometric, en degrés par seconde carré.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ accélération angulaire \_ Y \_ degrés \_ par \_ seconde \_ carré**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Gyrometric accélération de l’axe y, en degrés par seconde carré.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ accélération angulaire \_ Z \_ degrés \_ par \_ seconde \_ carré**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Accélération de l’axe z Gyrometric, en degrés par seconde carré.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ vélocité angulaire \_ X \_ degrés \_ par \_ seconde**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Vélocité de l’axe x Gyrometric, en degrés par seconde.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ vélocité angulaire \_ Y \_ degrés \_ par \_ seconde**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric vélocité de l’axe y, en degrés par seconde.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ vélocité angulaire \_ Z \_ degrés \_ par \_ seconde**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric vitesse de l’axe z, en degrés par seconde.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**Capteur \_ \_État de \_ mouvement \_ du type de données**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **VT \_ bool**<br/> **True** si le mouvement est détecté ; Sinon, **false**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**Capteur \_ Compteurs de vitesse de type de données \_ \_ \_ \_ par \_ seconde**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Vitesse en mètres par seconde.<br/>                                    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




