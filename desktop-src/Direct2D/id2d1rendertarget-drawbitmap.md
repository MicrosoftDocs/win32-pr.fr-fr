---
title: Méthodes ID2D1RenderTarget DrawBitmap
description: Dessine le ID2D1Bitmap spécifié.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Méthodes DrawBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112766"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a>ID2D1RenderTarget ::D méthodes rawBitmap

Dessine le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)spécifié.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                       | Description                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ \_ mode d’interpolation BITMAP \_ , d2d1 \_ rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))   | Dessine la bitmap spécifiée après sa mise à l’échelle à la taille du rectangle spécifié. <br/> |
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ F&, float, d2d1 \_ \_ mode d’interpolation bitmap \_ , d2d1 \_ rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))  | Dessine la bitmap spécifiée après sa mise à l’échelle à la taille du rectangle spécifié. <br/> |
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ F \* , float, d2d1 \_ \_ mode d’interpolation bitmap \_ , d2d1 \_ rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) | Dessine la bitmap spécifiée après sa mise à l’échelle à la taille du rectangle spécifié. <br/> |



## <a name="remarks"></a>Notes

Cette méthode ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **DrawBitmap**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [Comment dessiner une image bitmap](how-to-draw-a-bitmap.md). Pour obtenir un exemple illustrant le chargement d’une image bitmap à partir d’une ressource ou d’un fichier, consultez [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md) et [Comment charger une image bitmap à partir d’un fichier](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Comment dessiner une image bitmap](how-to-draw-a-bitmap.md)
</dt> <dt>

[Chargement d’une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[Chargement d’une image bitmap à partir d’un fichier](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

