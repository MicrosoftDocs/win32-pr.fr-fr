---
description: Spécifie le nombre de trames vidéo encodées par le codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530596"
---
# <a name="mfpkey_codedframes-property"></a>MFPKEY \_ propriété CODEDFRAMES

Spécifie le nombre de trames vidéo encodées par le codec.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCCodedFrames g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Cette valeur est égale à [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) moins les images qui ont été supprimées en raison de contraintes de vitesse de transmission. Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




