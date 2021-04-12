---
title: Constantes WINBIO_BIOMETRIC_SENSOR_SUBTYPE ( \_ types WINBIO. h)
description: Spécifiez un masque de réutiliser pour les fonctionnalités de capteur intégrées.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384379"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a>\_ \_ Constantes de sous-type de capteur BIOmétrique WINBIO \_

Les constantes suivantes peuvent être utilisées comme masque de masque pour le paramètre *Capabilities* de la structure de [**\_ \_ schéma d’unité WINBIO**](winbio-unit-schema.md) . Ils font référence aux fonctionnalités de capteur intégrées.



| Constante                                                                                                                                                                                                            | Description                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <dt>**\_sous-type de capteur WINBIO \_ \_ inconnu**</dt> </dl>     | Les sous-types de capteur ne sont pas connus.<br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <dt>**\_balayage de \_ sous-type de capteur WINBIO FP \_ \_**</dt> </dl> | Le capteur prend en charge les balayages par empreinte digitale.<br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <dt>**WINBIO \_ de \_ sous-type de capteur FP \_ \_**</dt> </dl> | Le capteur prend en charge les touches Finger.<br/>     |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> <dt>

[**\_schéma d’unité WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





