---
description: Active ou désactive le mode de génération de miniatures dans un décodeur vidéo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propriété AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb10b4996a88c8d2e62180edcbfaba8f71b6738d7dc7e3019a0b8ee4b44462d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159990"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Propriété AVDecVideoThumbnailGenerationMode

Active ou désactive le mode de génération de miniatures dans un décodeur vidéo.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Remarques

Si la valeur est **\_ true**, le décodeur utilise un paramètre optimisé pour générer rapidement des images miniatures. (Par exemple, il peut ignorer des frames B ou P.) Dans le cas contraire, si la valeur est **\_ false**, le décodeur utilise ses paramètres de décodage normaux.

## <a name="requirements"></a>Configuration requise



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

 

 




