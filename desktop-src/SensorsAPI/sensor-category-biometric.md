---
description: La \_ catégorie biométrique de catégorie de capteur \_ contient des capteurs qui fournissent des informations sur les êtres vivants.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112630"
---
# <a name="sensor_category_biometric"></a>biométrique de catégorie de capteur \_ \_

La \_ catégorie biométrique de catégorie de capteur \_ contient des capteurs qui fournissent des informations sur les êtres vivants.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                           | Description                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**Capteur \_ TAPEZ \_ \_ présence humaine**</dt> <dt>{C138C12B-AD52-451c-9375-87F518FF10C6}</dt> </dl>    | Capteurs détectant la présence humaine.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**Capteur \_ TAPEZ \_ \_ proximité humaine**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Capteurs détectant la proximité humaine.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**Capteur \_ TAPEZ \_ Touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Capteurs tactiles.<br/>                       |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ GUID biométrique \_ :

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                                         | Description                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**Capteur \_ \_Type de \_ données \_ présence humaine**</dt> <dt>(PID = 2)</dt> </dl>                          | **VT \_ bool**<br/> **True** lorsqu’un humain utilise l’ordinateur.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ \_ compteurs de proximité humains**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Distance entre un homme et l’ordinateur, en mètres.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**Capteur \_ \_ \_ \_ État tactile du type de données**</dt> <dt>(PID = 4)</dt> </dl>                                   | **VT \_ bool**<br/> **True** lorsque le capteur tactile est touché ; Sinon, **false**.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




