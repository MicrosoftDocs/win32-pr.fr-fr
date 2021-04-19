---
title: gluTessBeginContour, fonction (Glu. h)
description: Les fonctions gluTessBeginContour et gluTessEndContour délimitent une description du contour. | gluTessBeginContour, fonction (Glu. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- gluTessBeginContour fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523144"
---
# <a name="glutessbegincontour-function"></a><span data-ttu-id="ea1d2-105">gluTessBeginContour fonction)</span><span class="sxs-lookup"><span data-stu-id="ea1d2-105">gluTessBeginContour function</span></span>

<span data-ttu-id="ea1d2-106">Les fonctions **gluTessBeginContour** et [**gluTessEndContour**](glutessendcontour.md) délimitent une description du contour.</span><span class="sxs-lookup"><span data-stu-id="ea1d2-106">The **gluTessBeginContour** and [**gluTessEndContour**](glutessendcontour.md) functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea1d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea1d2-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="ea1d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea1d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea1d2-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="ea1d2-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="ea1d2-110">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="ea1d2-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea1d2-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ea1d2-111">Return value</span></span>

<span data-ttu-id="ea1d2-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ea1d2-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1d2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ea1d2-113">Remarks</span></span>

<span data-ttu-id="ea1d2-114">Les fonctions **gluTessBeginContour** et [**gluTessEndPolygon**](glutessendpolygon.md) délimitent la définition d’un contour de polygone.</span><span class="sxs-lookup"><span data-stu-id="ea1d2-114">The **gluTessBeginContour** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="ea1d2-115">Au sein de chaque paire **gluTessBeginContour** / **gluTessEndPolygon** , il peut y avoir zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="ea1d2-115">Within each **gluTessBeginContour**/**gluTessEndPolygon** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="ea1d2-116">Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier).</span><span class="sxs-lookup"><span data-stu-id="ea1d2-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="ea1d2-117">Vous pouvez appeler **gluTessBeginContour** uniquement entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) et **gluTessEndPolygon**.</span><span class="sxs-lookup"><span data-stu-id="ea1d2-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1d2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea1d2-118">Requirements</span></span>



| <span data-ttu-id="ea1d2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea1d2-119">Requirement</span></span> | <span data-ttu-id="ea1d2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea1d2-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1d2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea1d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1d2-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea1d2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ea1d2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea1d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1d2-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea1d2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea1d2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea1d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1d2-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1d2-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ea1d2-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea1d2-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea1d2-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea1d2-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea1d2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ea1d2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea1d2-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea1d2-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1d2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea1d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1d2-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="ea1d2-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="ea1d2-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="ea1d2-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="ea1d2-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="ea1d2-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="ea1d2-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="ea1d2-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="ea1d2-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="ea1d2-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="ea1d2-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="ea1d2-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="ea1d2-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="ea1d2-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





