---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Représente une matrice 3 par 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113473"
---
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ matrice \_ matrice \_ F

Représente une matrice 3 par 2.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Notes

**D2d1 \_ MATRIX \_ matrice** est un nouveau nom pour la [**structure \_ \_ matrice \_ F de la matrice D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Pour obtenir la liste des champs fournis par la matrice, consultez la [**\_ matrice D2D \_ matrice \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Pour simplifier les opérations de matrice courantes, Direct2D fournit la classe [**d2d1 :: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , qui est dérivée de la structure matrice de la [**\_ matrice \_ d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . La classe **Matrix3x2F** fournit un ensemble de méthodes d’assistance pour effectuer des tâches courantes, telles que la création d’une matrice de translation ou d’inclinaison.

## <a name="examples"></a>Exemples

L’exemple suivant utilise la méthode [**d2d1 :: Matrix3x2F :: rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) pour créer une matrice de rotation qui fait pivoter un carré dans le sens des aiguilles d’une montre à 45 degrés à propos du centre du carré et transmet la matrice à la méthode [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) de la cible de rendu (*m \_ pRenderTarget*).

L’illustration suivante montre l’effet de l’application de la transformation de rotation précédente au carré. Le carré d’origine est un contour en pointillés, et le carré pivoté est un contour Uni.

![illustration d’un carré pivoté dans le sens des aiguilles d’une montre à 45 degrés à propos du centre du carré d’origine](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



Le code a été omis de cet exemple. Pour plus d’informations sur les transformations, consultez [vue d’ensemble des transformations](direct2d-transforms-overview.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
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

[**\_Matrice matrice \_ D2D \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

