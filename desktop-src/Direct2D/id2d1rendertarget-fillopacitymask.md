---
title: Méthodes ID2D1RenderTarget FillOpacityMask
description: Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Méthodes FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542458"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>ID2D1RenderTarget :: FillOpacityMask, méthodes

Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                          | Description                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 le \_ contenu du masque d’opacité \_ \_ , D2D \_ rect \_ f&, D2D \_ rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu. <br/> |
| [**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 le \_ contenu du masque d’opacité \_ \_ , D2D \_ rect \_ f \* , D2D \_ rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Applique le masque d’opacité décrit par l’image bitmap spécifiée à un pinceau et utilise ce pinceau pour peindre une région de la cible de rendu. <br/> |



## <a name="remarks"></a>Notes

Pour que cette méthode fonctionne correctement, la cible de rendu doit utiliser le mode d’anticrénelage [**\_ \_ \_ alias d2d1 mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) anticrénelage. Vous pouvez définir le mode d’anticrénelage en appelant la méthode [**ID2D1RenderTarget :: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .

Cette méthode ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **FillOpacityMask**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

