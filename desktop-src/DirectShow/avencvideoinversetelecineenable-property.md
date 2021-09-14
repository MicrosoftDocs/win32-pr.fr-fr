---
description: Spécifie si l’encodeur effectue un télécinéma inverse.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propriété AVEncVideoInverseTelecineEnable (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111586"
---
# <a name="avencvideoinversetelecineenable-property"></a>Propriété AVEncVideoInverseTelecineEnable

Spécifie si l’encodeur effectue un télécinéma inverse.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoInverseTelecineEnable**

## <a name="remarks"></a>Notes

Si la valeur est **\_ true**, l’encodeur effectue un télécinéma inverse. Si vous n’avez pas besoin de télécinéma inverse, affectez la valeur **\_ false** à cette propriété. Pour effectuer un télécinéma inverse en dehors de l’encodeur, affectez la valeur **\_ false** à cette propriété et affectez à la propriété [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) la valeur eAVEncVideoOutputScan \_ SameAsInput.

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

 

 




