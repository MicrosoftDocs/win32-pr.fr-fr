---
title: Méthodes ID2D1RenderTarget SetTransform
description: Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante. Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Méthodes SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f23ffcd8d64df02b0be2287a33eff63a6a680200c0e051a15c77958dafd81438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873959"
---
# <a name="id2d1rendertargetsettransform-methods"></a>ID2D1RenderTarget :: SetTransform, méthodes

Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante. Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                              | Description                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ matrice \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante. Toutes les opérations de dessin suivantes se produisent dans l’espace transformé. <br/> |
| [**SetTransform (D2D1 \_ Matrix \_ matrice \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Applique la transformation spécifiée à la cible de rendu, en remplaçant la transformation existante. Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.<br/>  |



## <a name="examples"></a>Exemples

L’exemple suivant utilise la méthode **setTransform** pour appliquer une rotation à la cible de rendu. Pour obtenir un exemple complet, consultez [Comment faire pivoter un objet](how-to-rotate.md).


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Pour obtenir des exemples supplémentaires montrant comment transformer une cible de rendu, consultez [Comment mettre à l’échelle un objet](how-to-scale.md), [comment incliner un](how-to-skew.md)objet et [Comment convertir un objet](how-to-translate.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Vue d’ensemble des transformations](direct2d-transforms-overview.md)
</dt> <dt>

[Comment faire pivoter un objet](how-to-rotate.md)
</dt> <dt>

[Mise à l’échelle d’un objet](how-to-scale.md)
</dt> <dt>

[Comment incliner un objet](how-to-skew.md)
</dt> <dt>

[Comment traduire un objet](how-to-translate.md)
</dt> <dt>

[Comment appliquer plusieurs transformations à un objet](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

