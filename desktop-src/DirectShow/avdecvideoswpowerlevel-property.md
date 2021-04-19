---
description: Spécifie le niveau d’économie d’énergie d’un décodeur vidéo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propriété AVDecVideoSWPowerLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514092"
---
# <a name="avdecvideoswpowerlevel-property"></a>Propriété AVDecVideoSWPowerLevel

Spécifie le niveau d’économie d’énergie d’un décodeur vidéo.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valeur de la propriété

La plage des valeurs possibles est \[ 0.. 100 \] , inclusive, avec la signification suivante.



| Valeur | Description                 |
|-------|-----------------------------|
| 0     | Optimiser la durée de vie de la batterie.  |
| 100   | Optimisez la qualité vidéo. |



 

L’énumération [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) définit des constantes spécifiques dans cette plage.

## <a name="remarks"></a>Notes

Vous pouvez définir cette propriété lors de la lecture pour modifier le niveau d’économie d’énergie.

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

 

 




