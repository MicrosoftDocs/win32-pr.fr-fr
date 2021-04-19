---
title: gluEndCurve, fonction (Glu. h)
description: Les fonctions gluBeginCurve et gluEndCurve délimitent une définition de courbe B-spline rationnelle non uniforme (NURBS). | gluEndCurve, fonction (Glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluEndCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106540919"
---
# <a name="gluendcurve-function"></a><span data-ttu-id="661c4-105">gluEndCurve fonction)</span><span class="sxs-lookup"><span data-stu-id="661c4-105">gluEndCurve function</span></span>

<span data-ttu-id="661c4-106">Les fonctions [**gluBeginCurve**](glubegincurve.md) et **gluEndCurve** délimitent une définition de courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="661c4-106">The [**gluBeginCurve**](glubegincurve.md) and **gluEndCurve** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="661c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="661c4-107">Syntax</span></span>


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="661c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="661c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="661c4-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="661c4-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="661c4-110">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="661c4-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="661c4-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="661c4-111">Return value</span></span>

<span data-ttu-id="661c4-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="661c4-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="661c4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="661c4-113">Remarks</span></span>

<span data-ttu-id="661c4-114">Utilisez [**gluBeginCurve**](glubegincurve.md) pour marquer le début d’une définition de courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="661c4-114">Use [**gluBeginCurve**](glubegincurve.md) to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="661c4-115">Après avoir appelé **gluBeginCurve**, effectuez un ou plusieurs appels à [**gluNurbsCurve**](glunurbscurve.md) pour définir les attributs de la courbe.</span><span class="sxs-lookup"><span data-stu-id="661c4-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="661c4-116">Exactement l’un des appels à **gluNurbsCurve** doit avoir un type de courbe GL \_ Map1 \_ vertex \_ 3 ou GL \_ Map1 \_ vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="661c4-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="661c4-117">Pour marquer la fin de la définition de courbe NURBS, appelez **gluEndCurve**.</span><span class="sxs-lookup"><span data-stu-id="661c4-117">To mark the end of the NURBS curve definition, call **gluEndCurve**.</span></span>

<span data-ttu-id="661c4-118">Les évaluateurs OpenGL permettent d’afficher la courbe NURBS sous la forme d’une série de segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="661c4-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="661c4-119">L’état de l’évaluateur est préservé pendant le rendu avec [**glPushAttrib**](glpushattrib.md) ( \_ bit d’évaluation GL \_ ) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="661c4-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT ) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="661c4-120">Pour plus d’informations sur l’état exact que ces appels conservent, consultez **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="661c4-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="661c4-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="661c4-121">Examples</span></span>

<span data-ttu-id="661c4-122">Les fonctions suivantes affichent une courbe NURBS texturée avec des normales ; les coordonnées de texture et les normales sont également spécifiées comme courbes NURBS :</span><span class="sxs-lookup"><span data-stu-id="661c4-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="661c4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="661c4-123">Requirements</span></span>



| <span data-ttu-id="661c4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="661c4-124">Requirement</span></span> | <span data-ttu-id="661c4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="661c4-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="661c4-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="661c4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="661c4-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="661c4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="661c4-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="661c4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="661c4-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="661c4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="661c4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="661c4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="661c4-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="661c4-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="661c4-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="661c4-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="661c4-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="661c4-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="661c4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="661c4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="661c4-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="661c4-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661c4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="661c4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661c4-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="661c4-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="661c4-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="661c4-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="661c4-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="661c4-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="661c4-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="661c4-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="661c4-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="661c4-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





