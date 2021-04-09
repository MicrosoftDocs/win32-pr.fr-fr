---
title: gluEndTrim, fonction (Glu. h)
description: Les fonctions gluBeginTrim et gluEndTrim délimitent une définition de boucle de découpage NURBS B-spline (NURBS) non uniforme. | gluEndTrim, fonction (Glu. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- gluEndTrim fonction OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043022"
---
# <a name="gluendtrim-function"></a><span data-ttu-id="dd095-105">gluEndTrim fonction)</span><span class="sxs-lookup"><span data-stu-id="dd095-105">gluEndTrim function</span></span>

<span data-ttu-id="dd095-106">Les fonctions [**gluBeginTrim**](glubegintrim.md) et **gluEndTrim** délimitent une définition de boucle de découpage [NURBS](using-nurbs-curves-and-surfaces.md)B-spline (NURBS) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="dd095-106">The [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd095-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd095-107">Syntax</span></span>


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="dd095-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd095-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="dd095-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="dd095-110">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="dd095-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd095-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd095-111">Return value</span></span>

<span data-ttu-id="dd095-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dd095-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd095-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dd095-113">Remarks</span></span>

<span data-ttu-id="dd095-114">Utilisez [**gluBeginTrim**](glubegintrim.md) pour marquer le début d’une boucle de suppression et **gluEndTrim** pour marquer la fin d’une boucle de suppression.</span><span class="sxs-lookup"><span data-stu-id="dd095-114">Use [**gluBeginTrim**](glubegintrim.md) to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="dd095-115">Une boucle de rognage est un ensemble de segments de courbe orientés (formant une courbe fermée) qui définissent les limites d’une surface NURBS.</span><span class="sxs-lookup"><span data-stu-id="dd095-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="dd095-116">Vous incluez ces boucles de suppression dans la définition d’une surface NURBS, entre les appels à [**gluBeginSurface**](glubeginsurface.md) et [**gluEndSurface**](gluendsurface.md).</span><span class="sxs-lookup"><span data-stu-id="dd095-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="dd095-117">La définition d’une surface NURBS peut contenir de nombreuses boucles de découpage.</span><span class="sxs-lookup"><span data-stu-id="dd095-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="dd095-118">Par exemple, si vous écrivez une définition pour une surface NURBS qui ressemble à un rectangle avec un trou perforé, la définition contient deux boucles de découpage.</span><span class="sxs-lookup"><span data-stu-id="dd095-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="dd095-119">Une boucle définit le bord extérieur du rectangle ; l’autre définit le trou perforé.</span><span class="sxs-lookup"><span data-stu-id="dd095-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="dd095-120">Les définitions de chacune de ces boucles de suppression sont placées entre parenthèses par une paire [**gluBeginTrim**](glubegintrim.md)  /  **gluEndTrim** .</span><span class="sxs-lookup"><span data-stu-id="dd095-120">The definitions of each of these trimming loops would be bracketed by a [**gluBeginTrim**](glubegintrim.md) / **gluEndTrim** pair.</span></span>

<span data-ttu-id="dd095-121">La définition d’une boucle de rognage fermée unique peut se composer de plusieurs segments de courbe, chacun décrit comme une série de segments de ligne formant une courbe linéaire (consultez [**gluPwlCurve**](glupwlcurve.md)), comme une courbe NURBS unique (voir [**gluNurbsCurve**](glunurbscurve.md)) ou comme une combinaison des deux dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="dd095-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="dd095-122">Les seuls appels de bibliothèque qui peuvent apparaître dans une définition de boucle de suppression (entre les appels à [**gluBeginTrim**](glubegintrim.md) et **GluEndTrim**) sont **gluPwlCurve** et **gluNurbsCurve**.</span><span class="sxs-lookup"><span data-stu-id="dd095-122">The only library calls that can appear in a trimming-loop definition (between the calls to [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="dd095-123">La zone affichée de la surface NURBS correspond à la région dans le domaine située à gauche de la courbe de rognage à mesure que le paramètre Curve augmente.</span><span class="sxs-lookup"><span data-stu-id="dd095-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="dd095-124">Par conséquent, la région conservée de la surface NURBS est à l’intérieur d’une boucle de suppression dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="dd095-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="dd095-125">Pour le rectangle mentionné précédemment, la boucle de rognage pour le bord extérieur du rectangle s’exécute dans le sens inverse des aiguilles d’une montre, tandis que la boucle de rognage pour le trou perforé s’exécute dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="dd095-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="dd095-126">Si vous utilisez plusieurs courbes pour définir une seule boucle de rognage, les segments de courbe doivent former une boucle fermée (autrement dit, le point de terminaison de chaque courbe doit être le point de départ de la courbe suivante et le point de terminaison de la courbe finale doit être le point de départ de la première courbe).</span><span class="sxs-lookup"><span data-stu-id="dd095-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="dd095-127">Si les points de terminaison de la courbe sont suffisamment proches les uns des autres, mais ne coïncident pas exactement, ils sont forcés de correspondre.</span><span class="sxs-lookup"><span data-stu-id="dd095-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="dd095-128">Si les points de terminaison ne sont pas suffisamment proches, une erreur se produit (consultez [*gluNurbsCallback*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="dd095-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="dd095-129">Si une définition de boucle de rognage contient plusieurs courbes, la direction des courbes doit être cohérente (c’est-à-dire que l’intérieur doit être à gauche de toutes les courbes).</span><span class="sxs-lookup"><span data-stu-id="dd095-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="dd095-130">Vous pouvez utiliser des boucles de découpage imbriquées tant que les orientations de courbe alternent correctement.</span><span class="sxs-lookup"><span data-stu-id="dd095-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="dd095-131">Les courbes de rognage ne peuvent pas se croiser et ne peuvent pas se croiser les unes avec les autres (ou un résultat d’erreur).</span><span class="sxs-lookup"><span data-stu-id="dd095-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="dd095-132">Si aucune information de rognage n’est donnée pour une surface NURBS, la surface entière est dessinée.</span><span class="sxs-lookup"><span data-stu-id="dd095-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="dd095-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="dd095-133">Examples</span></span>

<span data-ttu-id="dd095-134">Ce fragment de code définit une boucle de rognage qui se compose d’une courbe linéaire par morceaux et de deux courbes NURBS :</span><span class="sxs-lookup"><span data-stu-id="dd095-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="dd095-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd095-135">Requirements</span></span>



| <span data-ttu-id="dd095-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd095-136">Requirement</span></span> | <span data-ttu-id="dd095-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd095-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd095-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd095-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dd095-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd095-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dd095-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd095-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dd095-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd095-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd095-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd095-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd095-143"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd095-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dd095-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd095-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd095-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd095-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd095-146">DLL</span><span class="sxs-lookup"><span data-stu-id="dd095-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd095-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd095-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd095-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd095-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd095-149">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="dd095-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="dd095-150">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="dd095-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="dd095-151">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="dd095-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="dd095-152">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="dd095-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="dd095-153">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="dd095-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="dd095-154">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="dd095-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





