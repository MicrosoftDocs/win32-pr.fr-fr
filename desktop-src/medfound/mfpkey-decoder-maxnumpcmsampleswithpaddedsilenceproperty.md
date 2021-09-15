---
description: Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin de après le décodage d’un fichier.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523597"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_Propriété MaxNumPCMSamplesWithPaddedSilence du décodeur MFPKEY \_

Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin de après le décodage d’un fichier.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

2 048

## <a name="remarks"></a>Notes

Cette propriété peut être utilisée pour estimer le silence artificiel qui est inséré entre les chansons au fur et à mesure qu’elles sont chargées dans le décodeur l’une après l’autre.

pour les décodeurs Windows Media Audio 10 Professional et Windows Media Audio 9 sans perte, cette propriété est toujours égale à 0.

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

 

 
