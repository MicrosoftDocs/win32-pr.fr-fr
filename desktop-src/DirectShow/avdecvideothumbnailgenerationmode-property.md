---
description: Active ou désactive le mode de génération de miniatures dans un décodeur vidéo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propriété AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112029"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Propriété AVDecVideoThumbnailGenerationMode

Active ou désactive le mode de génération de miniatures dans un décodeur vidéo.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Notes

Si la valeur est **\_ true**, le décodeur utilise un paramètre optimisé pour générer rapidement des images miniatures. (Par exemple, il peut ignorer des frames B ou P.) Dans le cas contraire, si la valeur est **\_ false**, le décodeur utilise ses paramètres de décodage normaux.

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

 

 




