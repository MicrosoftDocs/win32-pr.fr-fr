---
description: Spécifie le nombre de frames après le frame actuel que le codec évaluera avant d’encoder le frame actuel.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236069"
---
# <a name="mfpkey_lookahead-property"></a>\_Propriété de préanalyse MFPKEY

Spécifie le nombre de frames après le frame actuel que le codec évaluera avant d’encoder le frame actuel.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCLookAhead g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Lorsque le codec utilise la préanalyse, il peut encoder la vidéo plus efficacement.

l’objet writer de Windows Media Format SDK s’attend à ce que le codec encode chaque exemple immédiatement. par conséquent, cette fonctionnalité ne fonctionne pas correctement dans les logiciels qui utilisent l’objet writer (y compris Windows encodeur multimédia et Lecteur Windows Media). Toutes les extensions d’unité de données associées aux images vidéo sont attachées à une trame de sortie incorrecte. Le nombre de frames par lequel les extensions d’unité de données sont mal placées est égal au nombre de trames de la préanalyse utilisées.

Les valeurs de préanalyse valides sont comprises entre 0 et 16 frames. La valeur recommandée est 16.

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

 

 




