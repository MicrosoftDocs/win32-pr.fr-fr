---
description: Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin de après le décodage d’un fichier.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1722c4c8457035f082b069f46f1758d7caf4a4f3b8f500ebd4462e334778e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690357"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_Propriété MaxNumPCMSamplesWithPaddedSilence du décodeur MFPKEY \_

Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin de après le décodage d’un fichier.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

2 048

## <a name="remarks"></a>Remarques

Cette propriété peut être utilisée pour estimer le silence artificiel qui est inséré entre les chansons au fur et à mesure qu’elles sont chargées dans le décodeur l’une après l’autre.

pour les décodeurs Windows Media Audio 10 Professional et Windows Media Audio 9 sans perte, cette propriété est toujours égale à 0.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
