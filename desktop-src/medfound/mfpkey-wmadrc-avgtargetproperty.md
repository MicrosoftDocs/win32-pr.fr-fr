---
description: Spécifie le niveau de volume moyen souhaité de contenu audio de sortie.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530665"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>MFPKEY \_ WMADRC \_ AVGTARGET, propriété

Spécifie le niveau de volume moyen souhaité de contenu audio de sortie.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMADRCAverageTarget g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Consultez la section Notes.

## <a name="remarks"></a>Notes

Vous pouvez définir cette valeur sur le décodeur à des fins de contrôle de plage dynamique, mais il n’aura d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.

> [!Note]  
> La définition de la valeur cible moyenne n’est pas recommandée. L’ajustement de la valeur moyenne n’affecte pas la différence entre les sons forts et logiciels. Au lieu de cela, il réduit ou augmente le volume moyen total, ce qui peut entraîner une déformation indésirable pendant la lecture.

 

Si vous demandez un contrôle de plage dynamique à partir du décodeur lorsque cette propriété n’est pas définie, le codec calcule une valeur par défaut.

Utilisez les propriétés [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) et [MFPKEY \_ WMADRC \_ ](mfpkey-wmadrc-peakrefproperty.md) PEAKREF pour calculer les valeurs appropriées pour cette propriété.

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

 

 




