---
description: La \_ catégorie d’alimentation catégorie de capteur contient des \_ capteurs qui fournissent des informations sur les systèmes électriques.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516849"
---
# <a name="sensor_category_electrical"></a>catégorie de capteur \_ \_ électrique

La \_ catégorie d’alimentation catégorie de capteur contient des \_ capteurs qui fournissent des informations sur les systèmes électriques.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                              | Description                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**Capteur \_ \_Capacité de type**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Capteurs de capacité.<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**Capteur \_ TYPE \_ actuel**</dt> <dt>{5ADC9FCE-15A0-4BBE-A1AD-2D38A9AE831C}</dt> </dl>                             | Capteurs de courant électrique.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**Capteur \_ TAPER \_ \_ alimentation électrique**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | Capteurs d’alimentation électrique.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**Capteur \_ \_Fréquence de type**</dt> <dt>{8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | Capteur de fréquence électrique.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**Capteur \_ \_Inductance de type**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | Capteurs d’inductance.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**Capteur \_ \_Potentiomètre de type**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | Potentiomètres.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**Capteur \_ \_Résistance de type**</dt> <dt>{9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | Capteurs de résistance.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**Capteur \_ TYPE \_ voltage**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Capteurs de tension.<br/>             |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ GUID électrique :

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                                         | Description                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ Capacity \_ Farad**</dt> <dt> (PID = 4)</dt> </dl>                                | **VT \_ R8**<br/> Capacitance dans farads.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**Capteur \_ \_ \_ \_ Ampères actuels du type de données**</dt> <dt>(PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> Actuel en ampères.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**Capteur \_ TYPE de données de la \_ \_ \_ fréquence électrique \_ Hertz**</dt> <dt>(PID = 9)</dt> </dl>     | **VT \_ R8**<br/> Fréquence électrique en Hertz.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**Capteur \_ \_Type \_ de données \_ pourcentage électrique de la \_ \_ plage**</dt> <dt>(PID = 8)</dt> </dl> | **VT \_ R8**<br/> Le potentiomètre lit en pourcentage de la plage possible.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ alimentation électrique \_ watts**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> Alimentation électrique en watts.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ inductance \_ Henry**</dt> <dt>(PID = 6)</dt> </dl>                                    | **VT \_ R8**<br/> Inductance dans Henries.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**Capteur \_ Résistance du type de données- \_ \_ \_ ohms**</dt> <dt>(PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Résistance en ohms.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ tension \_ volts**</dt> <dt>(PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> Potentiel électrique en volts.<br/>                               |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




