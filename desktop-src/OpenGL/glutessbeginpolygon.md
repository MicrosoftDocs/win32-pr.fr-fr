---
title: gluTessBeginPolygon, fonction (Glu. h)
description: Les fonctions gluTessBeginPolygon et gluTessEndPolygon délimitent une description de polygone. | gluTessBeginPolygon, fonction (Glu. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- gluTessBeginPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520287"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="71c39-105">gluTessBeginPolygon fonction)</span><span class="sxs-lookup"><span data-stu-id="71c39-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="71c39-106">Les fonctions **gluTessBeginPolygon** et [**gluTessEndPolygon**](glutessendpolygon.md) délimitent une description de polygone.</span><span class="sxs-lookup"><span data-stu-id="71c39-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c39-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71c39-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="71c39-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71c39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c39-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="71c39-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="71c39-110">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="71c39-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="71c39-111">*\_données Polygon*</span><span class="sxs-lookup"><span data-stu-id="71c39-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="71c39-112">Pointeur vers une structure de données de polygone définie par le programmeur.</span><span class="sxs-lookup"><span data-stu-id="71c39-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c39-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71c39-113">Return value</span></span>

<span data-ttu-id="71c39-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="71c39-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71c39-115">Notes</span><span class="sxs-lookup"><span data-stu-id="71c39-115">Remarks</span></span>

<span data-ttu-id="71c39-116">Les fonctions **gluTessBeginPolygon** et [**gluTessEndPolygon**](glutessendpolygon.md) délimitent la définition d’un polygone qui n’est pas convexe.</span><span class="sxs-lookup"><span data-stu-id="71c39-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="71c39-117">Dans chaque paire **gluTessBeginPolygon**  /  **gluTessEndPolygon** , incluez un ou plusieurs appels à [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="71c39-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="71c39-118">Au sein de chaque profil, il y a zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="71c39-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="71c39-119">Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier).</span><span class="sxs-lookup"><span data-stu-id="71c39-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="71c39-120">Le paramètre de *\_ données Polygon* est un pointeur vers une structure de données définie par le programmeur.</span><span class="sxs-lookup"><span data-stu-id="71c39-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="71c39-121">Si les rappels appropriés sont spécifiés (voir [*gluTessCallback*](glutess.md)), ce pointeur est retourné à la fonction ou aux fonctions de rappel, ce qui en fait un moyen pratique de stocker les informations par polygone.</span><span class="sxs-lookup"><span data-stu-id="71c39-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="71c39-122">Quand vous appelez [**gluTessEndPolygon**](glutessendpolygon.md), le polygone est fractionné et les triangles résultants sont décrits par le biais de rappels.</span><span class="sxs-lookup"><span data-stu-id="71c39-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="71c39-123">Pour obtenir une description des fonctions de rappel, consultez [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="71c39-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="71c39-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="71c39-124">Examples</span></span>

<span data-ttu-id="71c39-125">Les éléments suivants décrivent un quadrilatère avec un trou triangulaire :</span><span class="sxs-lookup"><span data-stu-id="71c39-125">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="71c39-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71c39-126">Requirements</span></span>



| <span data-ttu-id="71c39-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71c39-127">Requirement</span></span> | <span data-ttu-id="71c39-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="71c39-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71c39-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c39-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71c39-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c39-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="71c39-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c39-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71c39-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c39-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="71c39-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="71c39-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="71c39-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="71c39-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="71c39-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71c39-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="71c39-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71c39-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71c39-137">DLL</span><span class="sxs-lookup"><span data-stu-id="71c39-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c39-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71c39-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c39-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71c39-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c39-140">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="71c39-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="71c39-141">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="71c39-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="71c39-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="71c39-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="71c39-143">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="71c39-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="71c39-144">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="71c39-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="71c39-145">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="71c39-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="71c39-146">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="71c39-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





