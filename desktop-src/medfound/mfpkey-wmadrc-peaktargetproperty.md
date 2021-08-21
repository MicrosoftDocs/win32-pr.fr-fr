---
description: Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79f54d15978bb3f6a34c015886d2aeb2a8ec48a0069669e81ea40bbd79353902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973228"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>MFPKEY \_ WMADRC \_ PEAKTARGET, propriété

Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMADRCPeakTarget g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Consultez la section Notes.

## <a name="remarks"></a>Remarques

Vous pouvez définir cette valeur sur le décodeur à des fins de contrôle de plage dynamique, mais il n’aura d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.

Si vous demandez un contrôle de plage dynamique à partir du décodeur lorsque cette propriété n’est pas définie, le codec calcule une valeur par défaut.

Utilisez les propriétés [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) et [MFPKEY \_ WMADRC \_ ](mfpkey-wmadrc-peakrefproperty.md) PEAKREF pour calculer les valeurs appropriées pour cette propriété.

pour plus d’informations sur le contrôle de plage dynamique, consultez l’article web [Windows Media Audio Professional les fonctionnalités du Codec](/previous-versions/ms867218(v=msdn.10)).

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

 

 
