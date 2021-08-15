---
description: Spécifie le niveau de volume moyen de contenu audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7d3575b81ca878c610aed95ca25f73fa94c292ec16f9245a72a3a9515198c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973238"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>MFPKEY \_ WMADRC \_ AVGREF, propriété

Spécifie le niveau de volume moyen de contenu audio.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMADRCAverageReference g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Remarques

Vous pouvez récupérer cette valeur à partir de l’encodeur une fois le contenu traité. Cette valeur peut également être définie sur le décodeur à des fins de contrôle de plage dynamique, mais n’a d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.

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

 

 
