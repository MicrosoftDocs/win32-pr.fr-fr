---
description: Spécifie la valeur de l’indicateur de frame de dépôt dans l’en-tête groupe d’images (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propriété AVEncVideoHeaderDropFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111630"
---
# <a name="avencvideoheaderdropframe-property"></a>Propriété AVEncVideoHeaderDropFrame

Spécifie la valeur de l’indicateur de frame de dépôt dans l’en-tête groupe d’images (GOP).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoHeaderDropFrame**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété peut être 0 ou 1.

## <a name="remarks"></a>Notes

Le mode de trame déroulant est utilisé dans la vidéo NTSC pour corriger l’écart entre la vidéo, 29,97 images par seconde, et l’affichage du code de temps, qui est de 30 images par seconde. En mode Drop Frame, les numéros de trame 00 et 01 sont ignorés au début de chaque minute, à l’exception des minutes, même les multiples de dix (00, 10, 20, etc.). Seuls les numéros de frame dans le code d’heure sont supprimés. aucun frame réel n’est supprimé.

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

 

 




