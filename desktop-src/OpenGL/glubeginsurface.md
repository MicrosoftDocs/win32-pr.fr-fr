---
title: gluBeginSurface, fonction (Glu. h)
description: Les fonctions gluBeginSurface et gluEndSurface délimitent une définition de surface de B-spline rationnelle (NURBS) non uniforme. | gluBeginSurface, fonction (Glu. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- gluBeginSurface fonction OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543011"
---
# <a name="glubeginsurface-function"></a><span data-ttu-id="54303-105">gluBeginSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="54303-105">gluBeginSurface function</span></span>

<span data-ttu-id="54303-106">Les fonctions **gluBeginSurface** et [**gluEndSurface**](gluendsurface.md) délimitent une définition de surface de B-spline rationnelle ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="54303-106">The **gluBeginSurface** and [**gluEndSurface**](gluendsurface.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="54303-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54303-107">Syntax</span></span>


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="54303-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54303-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54303-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="54303-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="54303-110">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="54303-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54303-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54303-111">Return value</span></span>

<span data-ttu-id="54303-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="54303-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54303-113">Notes</span><span class="sxs-lookup"><span data-stu-id="54303-113">Remarks</span></span>

<span data-ttu-id="54303-114">Les fonctions **gluBeginSurface** et **gluEndSurface** marquent le début et la fin des définitions de la surface NURBS, qui sont définies avec des appels à **gluNurbsSurface**.</span><span class="sxs-lookup"><span data-stu-id="54303-114">The **gluBeginSurface** and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="54303-115">Appelez **gluBeginSurface** pour marquer le début d’une définition de surface NURBS.</span><span class="sxs-lookup"><span data-stu-id="54303-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="54303-116">Effectuez un ou plusieurs appels à **gluNurbsSurface** pour définir les attributs de la surface.</span><span class="sxs-lookup"><span data-stu-id="54303-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="54303-117">Exactement l’un de ces appels à **gluNurbsSurface** doit avoir un type de surface de \_ map2 des vertex 1 \_ \_ ou GL \_ map2 \_ vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="54303-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="54303-118">Pour marquer la fin de la définition de la surface NURBS, appelez **gluEndSurface**.</span><span class="sxs-lookup"><span data-stu-id="54303-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="54303-119">Les fonctions [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)et [**gluEndTrim**](gluendtrim.md) prennent en charge la suppression des surfaces NURBS.</span><span class="sxs-lookup"><span data-stu-id="54303-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and [**gluEndTrim**](gluendtrim.md) functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="54303-120">Utilisez les évaluateurs OpenGL pour afficher la surface NURBS sous la forme d’un ensemble de polygones.</span><span class="sxs-lookup"><span data-stu-id="54303-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="54303-121">Conserver l’état de l’évaluateur lors du rendu avec [**glPushAttrib**](glpushattrib.md)( \_ bit d’évaluation GL \_ ) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="54303-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md)(GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54303-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="54303-122">Examples</span></span>

<span data-ttu-id="54303-123">Les fonctions suivantes affichent une surface NURBS texturée avec des normales ; les coordonnées de la texture et les normales sont également décrites comme des surfaces NURBS :</span><span class="sxs-lookup"><span data-stu-id="54303-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="54303-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54303-124">Requirements</span></span>



| <span data-ttu-id="54303-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54303-125">Requirement</span></span> | <span data-ttu-id="54303-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="54303-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54303-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54303-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54303-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54303-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="54303-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54303-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54303-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54303-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54303-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="54303-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54303-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="54303-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="54303-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54303-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="54303-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54303-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="54303-135">DLL</span><span class="sxs-lookup"><span data-stu-id="54303-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54303-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54303-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54303-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54303-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54303-138">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="54303-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="54303-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="54303-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="54303-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="54303-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="54303-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="54303-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="54303-142">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="54303-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="54303-143">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="54303-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





