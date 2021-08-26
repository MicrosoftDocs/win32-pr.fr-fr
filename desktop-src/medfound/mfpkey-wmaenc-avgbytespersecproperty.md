---
description: Spécifie le nombre moyen d’octets par seconde dans un flux audio VBR (variable-bit-rate) basé sur la qualité.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: MFPKEY_WMAENC_AVGBYTESPERSEC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfadc41e9f2c9f4410bc84c6d8bf23f30c559b96c83abba80beb719e8ccb8eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953299"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>MFPKEY \_ WMAENC \_ AVGBYTESPERSEC, propriété

Spécifie le nombre moyen d’octets par seconde dans un flux audio VBR (variable-bit-rate) basé sur la qualité.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACAvgBytesPerSecond g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Remarques

Vous pouvez récupérer cette valeur à partir du décodeur après l’encodage du flux.

Cette valeur est requise par le décodeur audio pour décompresser correctement le contenu.

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

 

 




