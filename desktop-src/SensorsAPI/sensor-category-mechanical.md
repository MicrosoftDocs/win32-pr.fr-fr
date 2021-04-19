---
description: La catégorie \_ mécanique de catégorie de capteur \_ contient des capteurs qui fournissent des informations relatives aux appareils mécaniques et aux mesures.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2446559820141b65a70bc75d25680da79563388c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544216"
---
# <a name="sensor_category_mechanical"></a>catégorie de capteur \_ \_ mécanique

La catégorie \_ mécanique de catégorie de capteur \_ contient des capteurs qui fournissent des informations relatives aux appareils mécaniques et aux mesures.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                                           | Description                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**Capteur \_ TAPEZ \_ le \_ commutateur booléen**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | Commutateurs à deux États (activé ou désactivé).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**Capteur \_ TAPEZ \_ un \_ \_ tableau de commutateur booléen**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | Tableau de commutateurs à deux États (activé ou désactivé).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**Capteur \_ TAPEZ \_ force**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | Capteurs de force.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**Capteur \_ ENTRER le \_ \_ commutateur à valeurs multiples**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Commutateurs à positions multiples.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**Capteur \_ \_Pression de type**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Capteurs de pression.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**Capteur \_ Mise \_**</dt> à l’échelle de type <dt>{C06DD92C-7FEB-438e-9BF6-82207FFF5BB8}</dt> </dl>                                                | Capteurs de poids.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**Capteur \_ \_Délimitation de type**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Capteurs de dépression.<br/>                          |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ \_ GUID mécanique :

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                                         | Description                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**Capteur \_ TYPE de données de \_ \_ \_ pression absolue \_ Pascal**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Pression absolue, en pascals.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**Capteur \_ Type de données \_ \_ État du \_ \_ tableau \_ de commutateurs booléens**</dt> <dt>(PID = 10)</dt> </dl> | **VT \_ UI4**<br/> Champs d’État pour un tableau de commutateurs booléens.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**Capteur \_ \_État du \_ \_ commutateur booléen \_ du type de données**</dt> <dt>(PID = 2)</dt> </dl>                       | **VT \_ bool**<br/> Champ d’État pour le \_ commutateur booléen du type de capteur \_ \_ .<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**Capteur \_ Types de données en \_ \_ \_ newtons de type de données**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Force, en Newtons.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**Capteur \_ Pression de jauge de type de données \_ \_ \_ \_ Pascal**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Pression relative à la jauge, en pascals.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**Capteur \_ \_État du \_ commutateur à \_ valeurs \_ multiples du type de données**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Champ d’État du \_ commutateur à valeurs multiples du type de capteur \_ \_ .<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**Capteur \_ \_ \_**</dt> Déchargement du type <dt> de données (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Limités.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ poids \_ kilogrammes**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Poids, en kilogrammes.<br/>                             |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




