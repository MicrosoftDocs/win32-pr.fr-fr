---
description: Spécifie le nombre de trames vidéo ignorées, car il s’agit de doublons de trames précédentes.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373d0e7d40b27edff8ae47c9081ef6acb55252858a677c6516877fe88bee392c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953249"
---
# <a name="mfpkey_zerobyteframes-property"></a>MFPKEY \_ propriété ZEROBYTEFRAMES

Spécifie le nombre de trames vidéo ignorées, car il s’agit de doublons de trames précédentes.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCZeroByteFrames g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Remarques

Cette valeur n’est pas soustraite du nombre total de frames transmis ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) lors du calcul du nombre de frames encodés ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).

Vous pouvez empêcher le codec d’ignorer les images dupliquées en définissant [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) sur variant \_ true.

Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




