---
description: Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propriété AVEncMPVDefaultBPictureCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033521"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Propriété AVEncMPVDefaultBPictureCount

Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Notes

Avant Windows 8, cette propriété s’applique aux encodeurs vidéo MPEG. À compter de Windows 8, cette propriété est utilisée par les encodeurs vidéo MPEG, WMV et H. 264.

Si l’encodeur prend en charge cette propriété, il peut être utilisé pour contrôler la structure du groupe d’images (GOP).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




