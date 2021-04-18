---
description: Active ou désactive le remplissage de l’intervenant dans un décodeur audio ou un processeur de signal numérique (DSP).
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: Propriété AVDSPSpeakerFill (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16bcdda053439b76c9445f2f9c866ee26afb4858
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516358"
---
# <a name="avdspspeakerfill-property"></a>Propriété AVDSPSpeakerFill

Active ou désactive le remplissage de l’intervenant dans un décodeur audio ou un processeur de signal numérique (DSP).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDSPSpeakerFill**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) .

## <a name="remarks"></a>Notes

Le remplissage de l’orateur est un processus DSP qui convertit les données audio mono ou stéréo en audio multicanal.

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

 

 




