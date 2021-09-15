---
description: Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour la lecture VBR (variable-bit-rate) avec restriction à 2 passes.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412911"
---
# <a name="mfpkey_rmax-property"></a>MFPKEY \_ propriété Rmax

Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour la lecture VBR (variable-bit-rate) avec restriction à 2 passes.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMaxBitrate g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Aucune valeur par défaut.

## <a name="remarks"></a>Notes

Cette valeur représente le taux binaire de pointe pour la lecture. La valeur de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) est utilisée pour décrire la mémoire tampon en termes de vitesse de transmission ; en effet, le VBR restreint est semblable au taux binaire constant (CBR) qui utilise cette valeur comme vitesse de transmission. Toutefois, un flux VBR restreint peut être lu à une vitesse de transmission inférieure, à condition que la mémoire tampon soit augmentée.

Vous devez définir cette valeur pour l’encodage VBR à double passage restreint. Une fois que vous avez commencé le traitement des exemples, vous ne devez pas interroger cette valeur tant que vous n’avez pas terminé d’encoder le flux. L’encodeur interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.

En général, cette valeur est deux à trois fois supérieure à la valeur de [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).

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

 

 




