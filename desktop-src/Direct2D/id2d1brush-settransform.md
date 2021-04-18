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
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="1a8ed-104">ID2D1Brush :: SetTransform, méthodes</span><span class="sxs-lookup"><span data-stu-id="1a8ed-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="1a8ed-105">Définit la transformation appliquée au pinceau.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1a8ed-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="1a8ed-106">Overload list</span></span>



| <span data-ttu-id="1a8ed-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a8ed-107">Method</span></span>                                                                                       | <span data-ttu-id="1a8ed-108">Description</span><span class="sxs-lookup"><span data-stu-id="1a8ed-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="1a8ed-109">[**SetTransform (D2D1 \_ Matrix \_ matrice \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="1a8ed-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="1a8ed-110">Définit la transformation appliquée au pinceau.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="1a8ed-111">[**SetTransform (D2D1 \_ Matrix \_ matrice \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="1a8ed-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="1a8ed-112">Définit la transformation appliquée au pinceau.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1a8ed-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1a8ed-113">Remarks</span></span>

<span data-ttu-id="1a8ed-114">Quand vous peignez avec un pinceau, il peint l’espace de coordonnées de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="1a8ed-115">Les pinceaux ne se positionnent pas automatiquement pour s’aligner avec l’objet qui est peint ; par défaut, ils commencent à peindre à l’origine (0,0) de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="1a8ed-116">Vous pouvez « déplacer » le dégradé défini par un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) vers une zone cible en définissant son point de départ et son point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="1a8ed-117">De même, vous pouvez déplacer le dégradé défini par un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en modifiant son centre et ses rayons.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="1a8ed-118">Pour aligner le contenu d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sur la zone qui est peinte, vous pouvez utiliser la méthode **setTransform** pour convertir l’image bitmap à l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="1a8ed-119">Cette transformation affecte uniquement le pinceau ; elle n’affecte pas les autres contenus dessinés par la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="1a8ed-120">Les illustrations suivantes montrent l’effet de l’utilisation d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour remplir un rectangle situé à l’emplacement (100, 100).</span><span class="sxs-lookup"><span data-stu-id="1a8ed-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="1a8ed-121">L’illustration de l’illustration de gauche montre le résultat du remplissage du rectangle sans transformer le pinceau : le bitmap est dessiné à l’origine de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="1a8ed-122">Par conséquent, seule une partie de la bitmap apparaît dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="1a8ed-123">L’illustration à droite montre le résultat de la transformation du [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) afin que son contenu soit décalé de 50 pixels vers la droite et de 50 pixels vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="1a8ed-124">Le bitmap remplit maintenant le rectangle.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-124">The bitmap now fills the rectangle.</span></span>

![illustration de deux carrés, un peint avec un bitmap sans pinceau transformé et un peint avec un pinceau transformé](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="1a8ed-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="1a8ed-126">Examples</span></span>

<span data-ttu-id="1a8ed-127">Les exemples de code suivants montrent comment créer la transformation affichée dans le diagramme de droite de l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="1a8ed-128">Tout d’abord, appliquez une translation à la [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), en déplaçant le pinceau 50 pixels vers la droite le long de l’axe x et 50 pixels vers le côté de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="1a8ed-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="1a8ed-129">Utilisez ensuite le **ID2D1BitmapBrush** pour remplir le rectangle qui a l’angle supérieur gauche à (100, 100) et le coin inférieur droit à (200, 200).</span><span class="sxs-lookup"><span data-stu-id="1a8ed-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


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





## <a name="requirements"></a><span data-ttu-id="1a8ed-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a8ed-130">Requirements</span></span>



| <span data-ttu-id="1a8ed-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a8ed-131">Requirement</span></span> | <span data-ttu-id="1a8ed-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a8ed-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8ed-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a8ed-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1a8ed-134"><dt>D2d1 \_ 1. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8ed-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="1a8ed-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a8ed-135">Library</span></span><br/> | <dl> <span data-ttu-id="1a8ed-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a8ed-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1a8ed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1a8ed-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a8ed-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a8ed-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="1a8ed-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a8ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8ed-140">Vue d’ensemble des pinceaux</span><span class="sxs-lookup"><span data-stu-id="1a8ed-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="1a8ed-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="1a8ed-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="1a8ed-142">�</span><span class="sxs-lookup"><span data-stu-id="1a8ed-142">�</span></span>

<span data-ttu-id="1a8ed-143">�</span><span class="sxs-lookup"><span data-stu-id="1a8ed-143">�</span></span>
