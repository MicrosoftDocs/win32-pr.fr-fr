---
description: La catégorie de l' \_ Analyseur de catégorie de capteur \_ contient des capteurs qui fournissent des informations obtenues par analyse.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951068"
---
# <a name="sensor_category_scanner"></a>\_scanneur de catégorie de capteur \_

La catégorie de l' \_ Analyseur de catégorie de capteur \_ contient des capteurs qui fournissent des informations obtenues par analyse.

**Types de capteurs définis par la plateforme**

Cette catégorie comprend les types de capteurs définis par la plateforme suivants.



| Type de capteur                                                                                                                                                                                                                                                                                           | Description                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <dt>**Capteur \_ TAPEZ le \_ \_ scanneur de codes-barres**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt> </dl> | Capteurs qui utilisent l’analyse optique pour lire les codes-barres.<br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <dt>**Capteur \_ TAPEZ \_ le \_ scanneur RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt> </dl>          | Capteurs d’analyse d’ID de fréquence radio.<br/>                 |



**Champs de données définis par la plateforme**

Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le \_ \_ GUID du scanneur du type de données du capteur \_ \_ :

{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}

Cette catégorie comprend les champs de données définis par la plateforme suivants.



| Nom du champ de données et PID                                                                                                                                                                                                                                                                     | Description                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <dt>**Capteur \_ TYPE de données \_ \_ \_ étiquette RFID \_ 40 \_ bit**</dt> <dt>(PID = 2)</dt> </dl> | **\_UI8 VT**<br/> valeur de la balise d’ID de fréquence radio 40 bits.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 

 




