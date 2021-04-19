---
description: Spécifie si une source de périphérique matériel utilise l’heure système pour les horodatages.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: Attribut MFT_HW_TIMESTAMP_WITH_QPC_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520487"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a>\_Horodateur de la MFT HW \_ \_ avec \_ attribut d' \_ attribut QPC

Spécifie si une source de périphérique matériel utilise l’heure système pour les horodatages.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, la source de l’appareil utilise l’heure système, telle qu’elle est retournée par le **QueryPerformanceCounter**, pour les horodatages. Dans le cas contraire, la source de l’appareil utilise l’horloge de l’appareil. La valeur par défaut est **FALSE**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capturer les attributs de l’appareil](capture-device-attributes.md)
</dt> </dl>

 

 




