---
title: gluTessProperty, fonction (Glu. h)
description: La fonction gluTessProperty définit la propriété d’un objet pavage.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- gluTessProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105898"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="d0596-104">gluTessProperty fonction)</span><span class="sxs-lookup"><span data-stu-id="d0596-104">gluTessProperty function</span></span>

<span data-ttu-id="d0596-105">La fonction **gluTessProperty** définit la propriété d’un objet pavage.</span><span class="sxs-lookup"><span data-stu-id="d0596-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0596-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0596-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="d0596-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0596-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0596-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="d0596-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d0596-109">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="d0596-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d0596-110">*et*</span><span class="sxs-lookup"><span data-stu-id="d0596-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="d0596-111">Valeur de propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="d0596-111">The property value to set.</span></span> <span data-ttu-id="d0596-112">Les valeurs suivantes sont valides : \_ \_ règle d’enroulement Tess Glu \_ , limite de Glu \_ Tess \_ \_ uniquement et \_ tolérance Glu Tess \_ .</span><span class="sxs-lookup"><span data-stu-id="d0596-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="d0596-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0596-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="d0596-114">Signification</span><span class="sxs-lookup"><span data-stu-id="d0596-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="d0596-115"><dt>**\_règle d' \_ enroulement \_ Tess Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="d0596-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="d0596-116">Détermine les parties du polygone qui se trouvent à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="d0596-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="d0596-117">Le paramètre de valeur peut être défini sur l’une des valeurs suivantes : GLU Tess enroulement \_ \_ \_ impair, Glu \_ Tess \_ Winding non \_ nul, Glu \_ Tess \_ bobinage \_ positif, Glu \_ Tess \_ enroulement \_ négatif ou Glu \_ Tess \_ \_ ABS \_ GEQ \_ .</span><span class="sxs-lookup"><span data-stu-id="d0596-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="d0596-118">Pour comprendre le fonctionnement de la règle d’enroulement, envisagez d’abord que les profils d’entrée partitionnent le plan en régions.</span><span class="sxs-lookup"><span data-stu-id="d0596-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="d0596-119">La règle d’enroulement détermine laquelle de ces régions se trouve à l’intérieur du polygone.</span><span class="sxs-lookup"><span data-stu-id="d0596-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="d0596-120">Pour un seul contour C, le nombre d’enroulements d’un point x est tout simplement le nombre de tours que nous avons défini autour de x, car nous nous déplacerons une fois autour de C (où le sens inverse est positif).</span><span class="sxs-lookup"><span data-stu-id="d0596-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="d0596-121">Lorsqu’il existe plusieurs conversions, les nombres enroulements individuels sont additionnés.</span><span class="sxs-lookup"><span data-stu-id="d0596-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="d0596-122">Cette procédure associe une valeur entière signée à chaque point x dans le plan.</span><span class="sxs-lookup"><span data-stu-id="d0596-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="d0596-123">Notez que le nombre d’enroulements est le même pour tous les points d’une même région.</span><span class="sxs-lookup"><span data-stu-id="d0596-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="d0596-124">La règle d’enroulement classe une région comme « à l’intérieur » si son numéro d’enroulement appartient à la catégorie choisie (valeur impaire, différente de zéro, positive, négative ou absolue d’au moins deux).</span><span class="sxs-lookup"><span data-stu-id="d0596-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="d0596-125">Le du paveur GLU précédent (antérieur à GLU 1,2) utilisait la règle « étrange ».</span><span class="sxs-lookup"><span data-stu-id="d0596-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="d0596-126">La règle « différente de zéro » (GLU \_ Tess \_ Winding \_ non Zero) est une autre méthode courante pour définir l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="d0596-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="d0596-127">Les trois autres règles (GLU \_ Tess \_ enroulement \_ positif, Glu \_ Tess \_ enroulement \_ négatif, Glu \_ Tess \_ \_ ABS \_ GEQ \_ Two) sont utiles pour les opérations Polygon CSG lèvent.</span><span class="sxs-lookup"><span data-stu-id="d0596-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="d0596-128"><dt>**\_limite Glu \_ Tess \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="d0596-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="d0596-129">Spécifie une valeur booléenne (définissez la valeur sur GL \_ true ou GL \_ false).</span><span class="sxs-lookup"><span data-stu-id="d0596-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="d0596-130">Lorsque vous définissez la valeur sur GL \_ true, un ensemble de contours fermés séparant l’intérieur et l’extérieur du polygone est retourné à la place d’un pavage.</span><span class="sxs-lookup"><span data-stu-id="d0596-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="d0596-131">Les contournements extérieurs sont orientés vers le sens inverse de la normale. les contournements intérieurs sont orientés dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="d0596-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="d0596-132">Les \_ \_ rappels de données Begin et Glu Glu Tess Begin et \_ \_ \_ utilisent le \_ type \_ de boucle de ligne GL pour chaque contour.</span><span class="sxs-lookup"><span data-stu-id="d0596-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="d0596-133"><dt>**\_tolérance Tess \_ Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="d0596-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="d0596-134">Spécifie une tolérance pour la fusion des fonctionnalités afin de réduire la taille de la sortie.</span><span class="sxs-lookup"><span data-stu-id="d0596-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="d0596-135">Par exemple, deux sommets très proches les uns des autres peuvent être remplacés par un seul vertex.</span><span class="sxs-lookup"><span data-stu-id="d0596-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="d0596-136">La tolérance est multipliée par la plus grande amplitude de coordonnée de n’importe quel vertex d’entrée ; Cela spécifie la distance maximale qu’une fonctionnalité peut déplacer à la suite d’une opération de fusion unique.</span><span class="sxs-lookup"><span data-stu-id="d0596-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="d0596-137">Si une fonctionnalité unique participe à plusieurs opérations de fusion, la distance totale déplacée peut être supérieure.</span><span class="sxs-lookup"><span data-stu-id="d0596-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="d0596-138">La fusion de fonctionnalités est entièrement facultative ; la tolérance n’est qu’une indication.</span><span class="sxs-lookup"><span data-stu-id="d0596-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="d0596-139">L’implémentation est libre de fusionner dans certains cas et non dans d’autres, ou de ne jamais fusionner des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d0596-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="d0596-140">La tolérance par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="d0596-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="d0596-141">L’implémentation actuelle fusionne les sommets uniquement s’ils coïncident exactement, quelle que soit la tolérance actuelle.</span><span class="sxs-lookup"><span data-stu-id="d0596-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="d0596-142">Un vertex est épissé dans une arête uniquement si l’implémentation ne peut pas distinguer le côté du bord sur lequel se trouve le vertex.</span><span class="sxs-lookup"><span data-stu-id="d0596-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="d0596-143">Deux bords sont fusionnés uniquement lorsque les deux points de terminaison sont identiques.</span><span class="sxs-lookup"><span data-stu-id="d0596-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="d0596-144">*value*</span><span class="sxs-lookup"><span data-stu-id="d0596-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="d0596-145">Valeur de la propriété indiquée.</span><span class="sxs-lookup"><span data-stu-id="d0596-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0596-146">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0596-146">Return value</span></span>

<span data-ttu-id="d0596-147">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d0596-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0596-148">Notes</span><span class="sxs-lookup"><span data-stu-id="d0596-148">Remarks</span></span>

<span data-ttu-id="d0596-149">La fonction **gluTessProperty** contrôle les propriétés stockées dans un objet pavage.</span><span class="sxs-lookup"><span data-stu-id="d0596-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="d0596-150">Ces propriétés affectent la manière dont les polygones sont interprétés et rendus.</span><span class="sxs-lookup"><span data-stu-id="d0596-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0596-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0596-151">Requirements</span></span>



| <span data-ttu-id="d0596-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0596-152">Requirement</span></span> | <span data-ttu-id="d0596-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0596-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0596-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0596-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d0596-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0596-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d0596-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0596-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d0596-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0596-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0596-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0596-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0596-159"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0596-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d0596-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0596-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0596-161"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0596-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0596-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d0596-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0596-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0596-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0596-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0596-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0596-165">**gluGetTessProperty**</span><span class="sxs-lookup"><span data-stu-id="d0596-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="d0596-166">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d0596-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





