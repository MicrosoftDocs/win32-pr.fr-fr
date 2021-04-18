---
title: gluEndPolygon, fonction (Glu. h)
description: Les fonctions gluBeginPolygon et gluEndPolygon délimitent une description de polygone. | gluEndPolygon, fonction (Glu. h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- gluEndPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106536234"
---
# <a name="gluendpolygon-function"></a><span data-ttu-id="bb2d1-105">gluEndPolygon fonction)</span><span class="sxs-lookup"><span data-stu-id="bb2d1-105">gluEndPolygon function</span></span>

<span data-ttu-id="bb2d1-106">\[La fonction **gluEndPolygon** est obsolète et n’est fournie qu’à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-106">\[The **gluEndPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="bb2d1-107">La fonction **gluEndPolygon** est mappée à **GluTessEndPolygon** suivie de **gluTessEndContour**.\]</span><span class="sxs-lookup"><span data-stu-id="bb2d1-107">The **gluEndPolygon** function is mapped to **gluTessEndPolygon** followed by **gluTessEndContour**.\]</span></span>

<span data-ttu-id="bb2d1-108">Les fonctions [**gluBeginPolygon**](glubeginpolygon.md) et **gluEndPolygon** délimitent une description de polygone.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-108">The [**gluBeginPolygon**](glubeginpolygon.md) and **gluEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2d1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb2d1-109">Syntax</span></span>


```C++
void gluEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="bb2d1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb2d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb2d1-111">*tess*</span><span class="sxs-lookup"><span data-stu-id="bb2d1-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="bb2d1-112">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="bb2d1-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb2d1-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb2d1-113">Return value</span></span>

<span data-ttu-id="bb2d1-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2d1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bb2d1-115">Remarks</span></span>

<span data-ttu-id="bb2d1-116">Utilisez [**gluBeginPolygon**](glubeginpolygon.md) et **gluEndPolygon** pour délimiter la définition d’un polygone qui n’est pas convexe.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-116">Use [**gluBeginPolygon**](glubeginpolygon.md) and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="bb2d1-117">Appelez **gluBeginPolygon**.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="bb2d1-118">Définissez les contournements du polygone en appelant [**gluTessVertex**](glutessvertex.md) pour chaque vertex et [**gluNextContour**](glunextcontour.md) pour démarrer chaque nouveau contour.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="bb2d1-119">Appelez **gluEndPolygon** pour signaler la fin de la définition.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="bb2d1-120">Une fois **gluEndPolygon** appelé, le polygone est fractionné et les triangles résultants sont décrits par le biais de rappels.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="bb2d1-121">Pour obtenir une description des fonctions de rappel, consultez [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="bb2d1-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bb2d1-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="bb2d1-122">Examples</span></span>

<span data-ttu-id="bb2d1-123">L’exemple suivant décrit un quadrilatère avec un trou triangulaire :</span><span class="sxs-lookup"><span data-stu-id="bb2d1-123">The following example describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="bb2d1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb2d1-124">Requirements</span></span>



| <span data-ttu-id="bb2d1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb2d1-125">Requirement</span></span> | <span data-ttu-id="bb2d1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb2d1-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2d1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb2d1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2d1-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb2d1-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bb2d1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb2d1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2d1-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb2d1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bb2d1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb2d1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb2d1-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb2d1-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="bb2d1-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb2d1-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb2d1-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb2d1-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb2d1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bb2d1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb2d1-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb2d1-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2d1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb2d1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2d1-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="bb2d1-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="bb2d1-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="bb2d1-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="bb2d1-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="bb2d1-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="bb2d1-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





