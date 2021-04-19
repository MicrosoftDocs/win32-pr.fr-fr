---
title: gluBeginPolygon, fonction (Glu. h)
description: Les fonctions gluBeginPolygon et gluEndPolygon délimitent une description de polygone. | gluBeginPolygon, fonction (Glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- gluBeginPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532390"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="9ed2e-105">gluBeginPolygon fonction)</span><span class="sxs-lookup"><span data-stu-id="9ed2e-105">gluBeginPolygon function</span></span>

<span data-ttu-id="9ed2e-106">\[La fonction **gluBeginPolygon** est obsolète et n’est fournie qu’à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="9ed2e-107">La fonction **gluBeginPolygon** est mappée à [**GluTessBeginPolygon**](glutessbeginpolygon.md) suivie de [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="9ed2e-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="9ed2e-108">Les fonctions **gluBeginPolygon** et [**gluEndPolygon**](gluendpolygon.md) délimitent une description de polygone.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed2e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ed2e-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="9ed2e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ed2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed2e-111">*tess*</span><span class="sxs-lookup"><span data-stu-id="9ed2e-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed2e-112">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="9ed2e-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed2e-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ed2e-113">Return value</span></span>

<span data-ttu-id="9ed2e-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed2e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9ed2e-115">Remarks</span></span>

<span data-ttu-id="9ed2e-116">Utilisez **gluBeginPolygon** et **gluEndPolygon** pour délimiter la définition d’un polygone qui n’est pas convexe.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="9ed2e-117">Appelez **gluBeginPolygon**.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="9ed2e-118">Définissez les contournements du polygone en appelant [**gluTessVertex**](glutessvertex.md) pour chaque vertex et [**gluNextContour**](glunextcontour.md) pour démarrer chaque nouveau contour.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="9ed2e-119">Appelez **gluEndPolygon** pour signaler la fin de la définition.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="9ed2e-120">Une fois **gluEndPolygon** appelé, le polygone est fractionné et les triangles résultants sont décrits par le biais de rappels.</span><span class="sxs-lookup"><span data-stu-id="9ed2e-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="9ed2e-121">Pour obtenir une description des fonctions de rappel, consultez [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="9ed2e-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ed2e-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ed2e-122">Examples</span></span>

<span data-ttu-id="9ed2e-123">L’exemple suivant décrit un quadrilatère avec un trou triangulaire :</span><span class="sxs-lookup"><span data-stu-id="9ed2e-123">The following example describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="9ed2e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ed2e-124">Requirements</span></span>



| <span data-ttu-id="9ed2e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ed2e-125">Requirement</span></span> | <span data-ttu-id="9ed2e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ed2e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed2e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ed2e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed2e-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ed2e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9ed2e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ed2e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed2e-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ed2e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9ed2e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ed2e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed2e-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed2e-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9ed2e-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ed2e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ed2e-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ed2e-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ed2e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9ed2e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ed2e-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ed2e-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed2e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ed2e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed2e-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="9ed2e-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="9ed2e-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="9ed2e-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="9ed2e-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="9ed2e-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="9ed2e-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="9ed2e-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="9ed2e-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="9ed2e-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="9ed2e-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="9ed2e-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





