---
description: Spécifie si un décodeur AAC utilise des équations downmix stéréo MPEG-2/MPEG-4 standard ou utilise un downmix non standard.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propriété AVDecAACDownmixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514727"
---
# <a name="avdecaacdownmixmode-property"></a>Propriété AVDecAACDownmixMode

Spécifie si un décodeur AAC utilise des équations downmix stéréo MPEG-2/MPEG-4 standard ou utilise un downmix non standard.

Un exemple de downmix non standard est celui défini par ARIB document STD-B21 version 4,4.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

