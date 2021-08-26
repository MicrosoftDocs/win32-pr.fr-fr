---
description: Spécifie le nombre de trames vidéo encodées par le codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e836f2177311a2ffc13065187a1affce93c6dbe74ff9ff4c99ef78a6f492b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954729"
---
# <a name="mfpkey_codedframes-property"></a>MFPKEY \_ propriété CODEDFRAMES

Spécifie le nombre de trames vidéo encodées par le codec.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCCodedFrames g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Remarques

Cette valeur est égale à [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) moins les images qui ont été supprimées en raison de contraintes de vitesse de transmission. Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.

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

 

 




