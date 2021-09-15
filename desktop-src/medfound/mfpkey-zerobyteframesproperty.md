---
description: Spécifie le nombre de trames vidéo ignorées, car il s’agit de doublons de trames précédentes.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412894"
---
# <a name="mfpkey_zerobyteframes-property"></a>MFPKEY \_ propriété ZEROBYTEFRAMES

Spécifie le nombre de trames vidéo ignorées, car il s’agit de doublons de trames précédentes.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCZeroByteFrames g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Cette valeur n’est pas soustraite du nombre total de frames transmis ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) lors du calcul du nombre de frames encodés ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).

Vous pouvez empêcher le codec d’ignorer les images dupliquées en définissant [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) sur variant \_ true.

Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




