---
title: D2D1_TAG (D2d1. h)
description: Valeur 64 bits définie par l’application et utilisée pour \ 160 ; marquez un ensemble d’opérations de rendu.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317206"
---
# <a name="d2d1_tag"></a>\_Balise d2d1

Valeur 64 bits définie par l’application, utilisée pour marquer un ensemble d’opérations de rendu.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Notes

Pour définir une balise avant une série d’opérations de rendu, utilisez la méthode [**ID2D1RenderTarget :: SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) . Pour récupérer la balise active, utilisez la méthode [**ID2D1RenderTarget :: GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

