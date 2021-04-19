---
title: gluBeginCurve, fonction (Glu. h)
description: Les fonctions gluBeginCurve et gluEndCurve délimitent une définition de courbe B-spline rationnelle non uniforme (NURBS). | gluBeginCurve, fonction (Glu. h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- gluBeginCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522933"
---
# <a name="glubegincurve-function"></a><span data-ttu-id="44887-105">gluBeginCurve fonction)</span><span class="sxs-lookup"><span data-stu-id="44887-105">gluBeginCurve function</span></span>

<span data-ttu-id="44887-106">Les fonctions **gluBeginCurve** et [**gluEndCurve**](gluendcurve.md) délimitent une définition de courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="44887-106">The **gluBeginCurve** and [**gluEndCurve**](gluendcurve.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="44887-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44887-107">Syntax</span></span>


```C++
void WINAPI gluBeginCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="44887-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44887-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44887-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="44887-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="44887-110">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="44887-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44887-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44887-111">Return value</span></span>

<span data-ttu-id="44887-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="44887-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44887-113">Notes</span><span class="sxs-lookup"><span data-stu-id="44887-113">Remarks</span></span>

<span data-ttu-id="44887-114">Utilisez **gluBeginCurve** pour marquer le début d’une définition de courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="44887-114">Use **gluBeginCurve** to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="44887-115">Après avoir appelé **gluBeginCurve**, effectuez un ou plusieurs appels à [**gluNurbsCurve**](glunurbscurve.md) pour définir les attributs de la courbe.</span><span class="sxs-lookup"><span data-stu-id="44887-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="44887-116">Exactement l’un des appels à **gluNurbsCurve** doit avoir un type de courbe GL \_ Map1 \_ vertex \_ 3 ou GL \_ Map1 \_ vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="44887-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="44887-117">Pour marquer la fin de la définition de courbe NURBS, appelez [**gluEndCurve**](gluendcurve.md).</span><span class="sxs-lookup"><span data-stu-id="44887-117">To mark the end of the NURBS curve definition, call [**gluEndCurve**](gluendcurve.md).</span></span>

<span data-ttu-id="44887-118">Les évaluateurs OpenGL permettent d’afficher la courbe NURBS sous la forme d’une série de segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="44887-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="44887-119">L’état de l’évaluateur est préservé pendant le rendu avec [**glPushAttrib**](glpushattrib.md) ( \_ bit d’évaluation GL \_ ) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="44887-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="44887-120">Pour plus d’informations sur l’état exact que ces appels conservent, consultez **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="44887-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="44887-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="44887-121">Examples</span></span>

<span data-ttu-id="44887-122">Les fonctions suivantes affichent une courbe NURBS texturée avec des normales ; les coordonnées de texture et les normales sont également spécifiées comme courbes NURBS :</span><span class="sxs-lookup"><span data-stu-id="44887-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="44887-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44887-123">Requirements</span></span>



| <span data-ttu-id="44887-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44887-124">Requirement</span></span> | <span data-ttu-id="44887-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="44887-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44887-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44887-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44887-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44887-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44887-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44887-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44887-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44887-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44887-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="44887-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="44887-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="44887-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="44887-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="44887-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="44887-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44887-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="44887-134">DLL</span><span class="sxs-lookup"><span data-stu-id="44887-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44887-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44887-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44887-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44887-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44887-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="44887-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="44887-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="44887-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="44887-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="44887-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="44887-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="44887-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="44887-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="44887-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





