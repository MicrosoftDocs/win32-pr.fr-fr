---
description: Spécifie le nombre de frames prédictifs bidirectionnels (frames B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235992"
---
# <a name="mfpkey_numbframes-property"></a>MFPKEY \_ propriété NUMBFRAMES

Spécifie le nombre de frames prédictifs bidirectionnels (frames B).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCNumBFrames g

## <a name="data-type"></a>Type de données

VT-I4

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

par défaut, Windows Media Video 9 utilise uniquement les intraframes (I-frames), également appelés images clés ou frames d’ancrage, qui sont des frames entièrement encodés, et des images prédictives (images P), qui sont encodées comme une différence par rapport au frame I précédent. Les frames B sont différents des frames P, car ils stockent à la fois les différences par rapport à l’image précédente et les différences par rapport au frame suivant.

Quand vous configurez le codec pour utiliser des frames B, il utilise le nombre spécifié d’images B entre chaque paire de frames de type I ou P.

Par exemple, si une séquence de frames sans B-frames est « IPPPPPPPPI », le même encodage de séquence avec deux frames B serait « IBBPBBPBBI ».

Pour la plupart des contenus, un ou deux frames B sont appropriés. À des débits de données supérieurs, une image B est normalement le choix optimal. Trois ou plus sont rarement utiles.

La plage de valeurs valide pour cette propriété est comprise entre 0 et 7.

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

 

 




