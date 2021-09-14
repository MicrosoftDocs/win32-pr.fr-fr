---
description: Active ou désactive l’égalisation sonore dans un décodeur audio ou un processeur de signal numérique (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propriété AVDSPLoudnessEqualization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112026"
---
# <a name="avdsploudnessequalization-property"></a>Propriété AVDSPLoudnessEqualization

Active ou désactive l’égalisation sonore dans un décodeur audio ou un processeur de signal numérique (DSP).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .

## <a name="remarks"></a>Notes

L’égalisation sonore est un processus DSP qui maintient un niveau de volume cohérent lorsque le flux audio change.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




