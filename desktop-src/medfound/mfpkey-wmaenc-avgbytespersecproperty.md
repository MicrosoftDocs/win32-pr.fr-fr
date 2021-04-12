---
description: Spécifie le nombre moyen d’octets par seconde dans un flux audio VBR (variable-bit-rate) basé sur la qualité.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: MFPKEY_WMAENC_AVGBYTESPERSEC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef88b9ea0cf46829a33cb7b9901c7c9f844c1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527957"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>MFPKEY \_ WMAENC \_ AVGBYTESPERSEC, propriété

Spécifie le nombre moyen d’octets par seconde dans un flux audio VBR (variable-bit-rate) basé sur la qualité.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACAvgBytesPerSecond g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Vous pouvez récupérer cette valeur à partir du décodeur après l’encodage du flux.

Cette valeur est requise par le décodeur audio pour décompresser correctement le contenu.

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

 

 




