---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Décrit les composants rouge, vert, bleu et alpha d’une couleur. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538288"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="9c6b9-105">D2D1 \_ couleur \_ F</span><span class="sxs-lookup"><span data-stu-id="9c6b9-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="9c6b9-106">Décrit les composants rouge, vert, bleu et alpha d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="9c6b9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9c6b9-107">Remarks</span></span>

<span data-ttu-id="9c6b9-108">**D2d1 \_ La couleur \_ f** est un typedef pour la [**couleur D2D ( \_ \_ f**](d2d-color-f.md)), qui est lui-même un typedef pour [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="9c6b9-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="9c6b9-109">Pour plus d’informations sur les membres fournis par **d2d1 \_ Color \_ F**, consultez [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="9c6b9-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="9c6b9-110">La classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) fournit un ensemble de couleurs prédéfinies et de fonctions d’assistance pour définir des couleurs.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="9c6b9-111">Pour plus d’informations, consultez la référence [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="9c6b9-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="9c6b9-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="9c6b9-112">Examples</span></span>

<span data-ttu-id="9c6b9-113">L’exemple suivant utilise la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) pour spécifier une couleur prédéfinie (noire) lors de la création d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="9c6b9-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="9c6b9-114">L’exemple suivant utilise la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) pour spécifier une couleur à l’aide des valeurs rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="9c6b9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c6b9-115">Requirements</span></span>



| <span data-ttu-id="9c6b9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c6b9-116">Requirement</span></span> | <span data-ttu-id="9c6b9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c6b9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6b9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c6b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6b9-119">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="9c6b9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c6b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6b9-121">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="9c6b9-122">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c6b9-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="9c6b9-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="9c6b9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c6b9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c6b9-125"><dt>D2DBaseTypes. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c6b9-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9c6b9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c6b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6b9-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="9c6b9-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="9c6b9-128">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

