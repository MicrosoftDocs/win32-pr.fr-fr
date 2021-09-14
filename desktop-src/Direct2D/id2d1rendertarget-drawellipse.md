---
title: Méthodes ID2D1RenderTarget DrawEllipse (D2d1. h)
description: Dessine le contour d’une ellipse avec les dimensions et le trait spécifiés.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Méthodes DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112762"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a>ID2D1RenderTarget ::D méthodes rawEllipse

Dessine le contour d’une ellipse avec les dimensions et le trait spécifiés.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                 | Description                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**DrawEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))  | Dessine le contour de l’ellipse spécifiée à l’aide du style de trait spécifié. <br/> |
| [**DrawEllipse (D2D1 \_ ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) | Dessine le contour de l’ellipse spécifiée à l’aide du style de trait spécifié. <br/> |



## <a name="remarks"></a>Notes

La méthode **DrawEllipse** ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **DrawEllipse**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [Comment dessiner et remplir une forme de base](how-to-draw-an-ellipse.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))
</dt> </dl>

�

�
