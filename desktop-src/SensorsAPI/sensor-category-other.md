---
description: L' \_ \_ autre catégorie de capteur contient des capteurs qui prennent en charge la classe personnalisée dans le pilote de classe HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033918"
---
# <a name="sensor_category_other"></a>catégorie de capteur \_ \_ autre

L' \_ \_ autre catégorie de capteur contient des capteurs qui prennent en charge la classe personnalisée dans le pilote de classe HID.

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**TYPE de capteur \_ \_ personnalisé**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



Capteur personnalisé qui prend en charge la classe personnalisée dans le pilote de classe HID.


</dt> </dl> </dd> </dl>

**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ GUID personnalisé :

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                    | Description                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**Capteur \_ \_ \_ \_ Utilisation personnalisée du type de données**</dt> <dt> (PID = 5)</dt> </dl>                          | **VT \_ UI4**<br/> Utilisation HID qui peut être utilisée pour distinguer plusieurs capteurs personnalisés.<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ \_ tableau booléen personnalisé**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ UI4**<br/> Tableau de valeurs booléennes pour un capteur personnalisé donné.<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ value1 personnalisée**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> L’une des six valeurs disponibles pour un capteur personnalisé donné.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ value2 personnalisé**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> L’une des six valeurs disponibles pour un capteur personnalisé donné.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ valeur3 personnalisé**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> L’une des six valeurs disponibles pour un capteur personnalisé donné.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ VALUE4 personnalisé**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> L’une des six valeurs disponibles pour un capteur personnalisé donné.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ VALUE5 personnalisé**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> L’une des six valeurs disponibles pour un capteur personnalisé donné.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ VALUE6 personnalisé**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> L’une des six valeurs disponibles pour un capteur personnalisé donné.<br/>       |



## <a name="remarks"></a>Notes

Un capteur qui prend en charge la classe générique dans le pilote de classe HID est mappé à l’une des autres catégories définies (biométrique, électrique, environnement, etc.).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




