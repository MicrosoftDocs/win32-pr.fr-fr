---
title: gluNextContour, fonction (Glu. h)
description: La fonction gluNextContour marque le début d’un autre contour.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour fonction OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384251"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="f8bc0-104">gluNextContour fonction)</span><span class="sxs-lookup"><span data-stu-id="f8bc0-104">gluNextContour function</span></span>

<span data-ttu-id="f8bc0-105">\[La fonction **gluNextContour** est obsolète et n’est fournie qu’à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="f8bc0-106">La fonction **gluNextContour** est mappée à [**GluTessEndContour**](glutessendcontour.md) suivie de [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="f8bc0-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="f8bc0-107">La fonction **gluNextContour** marque le début d’un autre contour.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bc0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8bc0-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="f8bc0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8bc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8bc0-110">*tess*</span><span class="sxs-lookup"><span data-stu-id="f8bc0-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="f8bc0-111">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="f8bc0-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f8bc0-112">*type*</span><span class="sxs-lookup"><span data-stu-id="f8bc0-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f8bc0-113">Type du contour en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-113">The type of the contour being defined.</span></span> <span data-ttu-id="f8bc0-114">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-114">The following values are valid.</span></span>



| <span data-ttu-id="f8bc0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8bc0-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="f8bc0-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f8bc0-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="f8bc0-117"><dt>**\_extérieur Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="f8bc0-118">Un contour extérieur définit une frontière extérieure du polygone.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="f8bc0-119"><dt>**GLU \_ intérieur**</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="f8bc0-120">Un contour intérieur définit une limite intérieure du polygone (par exemple, un trou).</span><span class="sxs-lookup"><span data-stu-id="f8bc0-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="f8bc0-121"><dt>**GLU \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="f8bc0-122">Un contour inconnu est analysé par la bibliothèque pour déterminer s’il se trouve à l’intérieur ou à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="f8bc0-123"><dt>**GLU \_ CCW, Glu \_ CW**</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="f8bc0-124">Le premier GLU \_ CCW ou Glu \_ CW défini est considéré comme extérieur.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="f8bc0-125">Tous les autres contours sont considérés comme extérieurs s’ils sont orientés dans la même direction (dans le sens horaire ou dans le sens inverse des aiguilles d’une montre) que le premier contour et dans l’intérieur s’ils ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="f8bc0-126">Si un profil est de type GLU \_ CCW ou Glu \_ CW, tous les contours doivent être du même type (si ce n’est pas le cas, tous les contours Glu \_ CCW et Glu \_ CW seront remplacés par Glu \_ inconnu).</span><span class="sxs-lookup"><span data-stu-id="f8bc0-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="f8bc0-127">Notez qu’il n’y a pas de différence réelle entre les \_ types de contour Glu CCW et Glu \_ CW.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8bc0-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8bc0-128">Return value</span></span>

<span data-ttu-id="f8bc0-129">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8bc0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="f8bc0-130">Remarks</span></span>

<span data-ttu-id="f8bc0-131">Utilisez la fonction **gluNextContour** pour décrire les polygones avec plusieurs contournements.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="f8bc0-132">Une fois que vous avez décrit le premier profil à travers une série d’appels [**gluTessVertex**](glutessvertex.md) , un appel **gluNextContour** indique que le contour précédent est terminé et que le contour suivant va commencer.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="f8bc0-133">Effectuez une autre série d’appels **gluTessVertex** pour décrire le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="f8bc0-134">Répétez ce processus jusqu’à ce que tous les profils aient été décrits.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="f8bc0-135">Le paramètre de *type* définit le type de contour suivant.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="f8bc0-136">Pour définir le type du premier contour, vous pouvez appeler **gluNextContour** avant de décrire le premier contour.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="f8bc0-137">Si vous n’appelez pas **gluNextContour** avant le premier contour, le premier contour est marqué Glu \_ extérieur.</span><span class="sxs-lookup"><span data-stu-id="f8bc0-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="f8bc0-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="f8bc0-138">Examples</span></span>

<span data-ttu-id="f8bc0-139">Vous pouvez décrire un quadrilatère avec un trou triangulaire dans celui-ci, comme suit :</span><span class="sxs-lookup"><span data-stu-id="f8bc0-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="f8bc0-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8bc0-140">Requirements</span></span>



| <span data-ttu-id="f8bc0-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8bc0-141">Requirement</span></span> | <span data-ttu-id="f8bc0-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8bc0-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8bc0-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8bc0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f8bc0-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8bc0-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8bc0-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8bc0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f8bc0-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8bc0-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8bc0-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8bc0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8bc0-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f8bc0-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8bc0-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8bc0-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8bc0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f8bc0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8bc0-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8bc0-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8bc0-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8bc0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8bc0-154">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f8bc0-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="f8bc0-155">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="f8bc0-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="f8bc0-156">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f8bc0-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="f8bc0-157">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="f8bc0-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="f8bc0-158">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="f8bc0-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="f8bc0-159">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="f8bc0-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





