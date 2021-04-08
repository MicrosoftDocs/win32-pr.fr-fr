---
description: La \_ catégorie capteur \_ Light contient des capteurs qui fournissent des informations sur les caractéristiques de Light.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862262"
---
# <a name="sensor_category_light"></a>catégorie de capteur \_ \_ Light

La \_ catégorie capteur \_ Light contient des capteurs qui fournissent des informations sur les caractéristiques de Light.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                     | Description                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <dt>**Capteur \_ TAPEZ \_ \_ lumière ambiante**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt> </dl> | Capteurs de lumière ambiante.<br/> |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ GUID clair :

{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <dt> **Type de données de capteur \_ \_ \_ Light \_ CHROMACITY**</dt> <dt>(PID = 4)</dt> </dl>                     | **VT \_ UI1 VT Vector \| \_**<br/> La chromatique est un tableau compté de valeurs float.<br/> Les données des types vectoriels sont toujours sérialisées en tant que **VT \_ UI1** (un tableau de caractères non signés, de 1 octet). Ce champ de données contient en fait chaque valeur en tant que valeur réelle IEEE de 4 octets (**VT \_ R4**).<br/> Pour plus d’informations sur l’utilisation des tableaux, consultez [récupération des types de vecteurs](retrieving-vector-types.md).<br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <dt>**Capteur \_ TYPE de données de \_ \_ niveau de lumière \_ \_ Lux**</dt> <dt> (PID = 2)</dt> </dl>                            | **VT \_ R4**<br/> Niveau d’éclairage, en lux.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <dt>**Capteur \_ TYPE de données- \_ \_ \_ température \_ légère**</dt> <dt> (PID = 3)</dt> </dl> | **VT \_ R4**<br/> Température de couleur, en degrés Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




