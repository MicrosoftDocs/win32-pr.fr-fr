---
title: gluTessEndContour, fonction (Glu. h)
description: Les fonctions gluTessBeginContour et gluTessEndContour délimitent une description du contour. | gluTessEndContour, fonction (Glu. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- gluTessEndContour fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321993"
---
# <a name="glutessendcontour-function"></a><span data-ttu-id="407ee-105">gluTessEndContour fonction)</span><span class="sxs-lookup"><span data-stu-id="407ee-105">gluTessEndContour function</span></span>

<span data-ttu-id="407ee-106">Les fonctions [**gluTessBeginContour**](glutessbegincontour.md) et **gluTessEndContour** délimitent une description du contour.</span><span class="sxs-lookup"><span data-stu-id="407ee-106">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="407ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="407ee-107">Syntax</span></span>


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="407ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="407ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="407ee-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="407ee-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="407ee-110">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="407ee-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="407ee-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="407ee-111">Return value</span></span>

<span data-ttu-id="407ee-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="407ee-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="407ee-113">Notes</span><span class="sxs-lookup"><span data-stu-id="407ee-113">Remarks</span></span>

<span data-ttu-id="407ee-114">Les fonctions [**gluTessBeginContour**](glutessbegincontour.md) et **gluTessEndContour** délimitent la définition d’un contour de polygone.</span><span class="sxs-lookup"><span data-stu-id="407ee-114">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="407ee-115">Au sein de chaque paire **gluTessBeginContour** / **gluTessEndContour** , il peut y avoir zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="407ee-115">Within each **gluTessBeginContour**/**gluTessEndContour** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="407ee-116">Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier).</span><span class="sxs-lookup"><span data-stu-id="407ee-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="407ee-117">Vous pouvez appeler **gluTessBeginContour** uniquement entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) et [**gluTessEndPolygon**](glutessendpolygon.md).</span><span class="sxs-lookup"><span data-stu-id="407ee-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and [**gluTessEndPolygon**](glutessendpolygon.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="407ee-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="407ee-118">Requirements</span></span>



| <span data-ttu-id="407ee-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="407ee-119">Requirement</span></span> | <span data-ttu-id="407ee-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="407ee-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="407ee-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="407ee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="407ee-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="407ee-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="407ee-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="407ee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="407ee-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="407ee-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="407ee-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="407ee-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="407ee-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="407ee-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="407ee-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="407ee-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="407ee-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="407ee-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="407ee-129">DLL</span><span class="sxs-lookup"><span data-stu-id="407ee-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="407ee-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="407ee-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="407ee-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="407ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407ee-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="407ee-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="407ee-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="407ee-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="407ee-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="407ee-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="407ee-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="407ee-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="407ee-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="407ee-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="407ee-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="407ee-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="407ee-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="407ee-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





