---
title: Méthodes ID2D1RenderTarget FillEllipse (D2d1. h)
description: Peint l’intérieur de l’ellipse spécifiée.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Méthodes FillEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7ee6624e5f557bb82924b4fa0f77d88a9cec35775a72009608120e8b8f2bd063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874169"
---
# <a name="id2d1rendertargetfillellipse-methods"></a>ID2D1RenderTarget :: FillEllipse, méthodes

Peint l’intérieur de l’ellipse spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                             | Description                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| [**FillEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))  | Peint l’intérieur de l’ellipse spécifiée. <br/> |
| [**FillEllipse (D2D1 \_ ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) | Peint l’intérieur de l’ellipse spécifiée. <br/> |



## <a name="remarks"></a>Remarques

Cette méthode ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **FillEllipse**) a échoué, vérifiez les résultats retournés par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [Comment dessiner et remplir une forme de base](how-to-draw-an-ellipse.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Comment dessiner et remplir une forme de base](how-to-draw-an-ellipse.md)
</dt> </dl>

�

�
