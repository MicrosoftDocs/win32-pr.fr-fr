---
title: Constantes WINBIO_SENSOR_MODE ( \_ types WINBIO. h)
description: Définissez le mode d’adaptateur de capteur.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8f0cb4592931629e6feec4fff4a6ac3e5986d3b199afee719dd8dae67a9580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909327"
---
# <a name="winbio_sensor_mode-constants"></a>\_Constantes du mode de capteur WINBIO \_

Les valeurs suivantes sont utilisées dans la fonction [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) pour définir le mode d’adaptateur de capteur.



| Constante                                                                                                                                                                                                        | Description                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**\_capteur WINBIO \_ \_ mode inconnu**</dt> </dl>          | Le mode d’opération n’est pas connu.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**WINBIO \_ - \_ mode de base du capteur \_**</dt> </dl>                | Faire fonctionner le capteur en mode de base. Le capteur agit uniquement comme un appareil de capture. Les capacités de traitement ou de stockage intégrées qui existent ne sont pas utilisées.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**\_ \_ mode avancé du capteur WINBIO \_**</dt> </dl>       | Faire fonctionner le capteur en mode avancé. Le capteur peut capturer des exemples et effectuer des fonctions de correspondance et de stockage.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**\_mode de \_ navigation du capteur WINBIO \_**</dt> </dl> | Faire fonctionner le capteur comme un tapis de souris. Cela n’est actuellement pas pris en charge.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**\_ \_ mode veille du capteur WINBIO \_**</dt> </dl>                | Faire fonctionner le capteur en mode veille.<br/>                                                                                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





