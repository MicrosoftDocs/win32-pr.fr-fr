---
title: Méthodes ID2D1RenderTarget CreateBitmapBrush
description: Crée un ID2D1BitmapBrush à partir de la bitmap spécifiée.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Méthodes CreateBitmapBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: fcd512393a3f037cd3def40d4aa55003d9fddcef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533372"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>ID2D1RenderTarget :: CreateBitmapBrush, méthodes

Crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à partir de la bitmap spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                                                               | Description                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush (ID2D1Bitmap \* , d2d1 \_ \_ Propriétés du pinceau bitmap \_&, \_ Propriétés du pinceau d2d1 \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à partir de la bitmap spécifiée.<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* , d2d1 \_ , \_ Propriétés du pinceau \_ de bitmap \* , \_ Propriétés du pinceau d2d1 \_ \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à partir de la bitmap spécifiée.<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à partir de la bitmap spécifiée. Le pinceau utilise les valeurs par défaut pour le mode étendu, le mode d’interpolation, l’opacité et la transformation.<br/> |
| [**CreateBitmapBrush (ID2D1Bitmap \* , d2d1 \_ , \_ propriétés du pinceau \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Crée un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à partir de la bitmap spécifiée. Le pinceau utilise les valeurs par défaut pour son opacité et sa transformation.<br/>                                   |



## <a name="examples"></a>Exemples

Pour obtenir un exemple illustrant comment peindre une zone avec un pinceau bitmap, consultez [How to Create a bitmap Brush](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Comment créer un pinceau bitmap](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> </dl>

 

