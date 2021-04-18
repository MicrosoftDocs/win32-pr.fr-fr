---
title: Méthodes ID2D1Brush SetTransform (D2d1 \_ 1. h)
description: Définit la transformation appliquée au pinceau.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Méthodes SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529015"
---
# <a name="id2d1brushsettransform-methods"></a>ID2D1Brush :: SetTransform, méthodes

Définit la transformation appliquée au pinceau.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                       | Description                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ matrice \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Définit la transformation appliquée au pinceau.<br/> |
| [**SetTransform (D2D1 \_ Matrix \_ matrice \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Définit la transformation appliquée au pinceau.<br/> |



## <a name="remarks"></a>Notes

Quand vous peignez avec un pinceau, il peint l’espace de coordonnées de la cible de rendu. Les pinceaux ne se positionnent pas automatiquement pour s’aligner avec l’objet qui est peint ; par défaut, ils commencent à peindre à l’origine (0,0) de la cible de rendu.

Vous pouvez « déplacer » le dégradé défini par un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) vers une zone cible en définissant son point de départ et son point de terminaison. De même, vous pouvez déplacer le dégradé défini par un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en modifiant son centre et ses rayons.

Pour aligner le contenu d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sur la zone qui est peinte, vous pouvez utiliser la méthode **setTransform** pour convertir l’image bitmap à l’emplacement souhaité. Cette transformation affecte uniquement le pinceau ; elle n’affecte pas les autres contenus dessinés par la cible de rendu.

Les illustrations suivantes montrent l’effet de l’utilisation d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour remplir un rectangle situé à l’emplacement (100, 100). L’illustration de l’illustration de gauche montre le résultat du remplissage du rectangle sans transformer le pinceau : le bitmap est dessiné à l’origine de la cible de rendu. Par conséquent, seule une partie de la bitmap apparaît dans le rectangle.

L’illustration à droite montre le résultat de la transformation du [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) afin que son contenu soit décalé de 50 pixels vers la droite et de 50 pixels vers le dessous. Le bitmap remplit maintenant le rectangle.

![illustration de deux carrés, un peint avec un bitmap sans pinceau transformé et un peint avec un pinceau transformé](images/brushes-ovw-transform.png)

## <a name="examples"></a>Exemples

Les exemples de code suivants montrent comment créer la transformation affichée dans le diagramme de droite de l’illustration précédente. Tout d’abord, appliquez une translation à la [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), en déplaçant le pinceau 50 pixels vers la droite le long de l’axe x et 50 pixels vers le côté de l’axe y. Utilisez ensuite le **ID2D1BitmapBrush** pour remplir le rectangle qui a l’angle supérieur gauche à (100, 100) et le coin inférieur droit à (200, 200).


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1 \_ 1. h (inclure D2d1. h)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
