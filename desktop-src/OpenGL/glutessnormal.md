---
title: gluTessNormal, fonction (Glu. h)
description: La fonction gluTessNormal spécifie un normal pour un polygone.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942735"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="0045d-104">gluTessNormal fonction)</span><span class="sxs-lookup"><span data-stu-id="0045d-104">gluTessNormal function</span></span>

<span data-ttu-id="0045d-105">La fonction **gluTessNormal** spécifie un normal pour un polygone.</span><span class="sxs-lookup"><span data-stu-id="0045d-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="0045d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0045d-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="0045d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0045d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0045d-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="0045d-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="0045d-109">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="0045d-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0045d-110">*x*</span><span class="sxs-lookup"><span data-stu-id="0045d-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="0045d-111">Composant de coordonnée x d’un normal.</span><span class="sxs-lookup"><span data-stu-id="0045d-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="0045d-112">*y*</span><span class="sxs-lookup"><span data-stu-id="0045d-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="0045d-113">Composant de coordonnée y d’un normal.</span><span class="sxs-lookup"><span data-stu-id="0045d-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="0045d-114">*z*</span><span class="sxs-lookup"><span data-stu-id="0045d-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="0045d-115">Composant de coordonnée z d’un normal.</span><span class="sxs-lookup"><span data-stu-id="0045d-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0045d-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0045d-116">Return value</span></span>

<span data-ttu-id="0045d-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0045d-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0045d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0045d-118">Remarks</span></span>

<span data-ttu-id="0045d-119">La fonction **gluTessNormal** décrit un normal pour un polygone que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="0045d-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="0045d-120">Toutes les données d’entrée sont projetées sur un plan perpendiculaire à l’un des trois axes de coordonnées avant la polygonalisation, et tous les triangles de sortie sont orientés vers le sens inverse des aiguilles d’une dépassement en respectant la normale.</span><span class="sxs-lookup"><span data-stu-id="0045d-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="0045d-121">(Pour obtenir l’orientation dans le sens des aiguilles d’une montre, inversez le signe de la normale fournie).</span><span class="sxs-lookup"><span data-stu-id="0045d-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="0045d-122">Par exemple, si vous savez que tous les polygones se trouvent dans le plan x-y, appelez **gluTessNormal**(tess, 0,0, 0,0, 1,0) avant de restituer des polygones.</span><span class="sxs-lookup"><span data-stu-id="0045d-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="0045d-123">Si la normale fournie est (0,0, 0,0, 0,0) (valeur par défaut), la normale est déterminée comme suit :</span><span class="sxs-lookup"><span data-stu-id="0045d-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="0045d-124">La direction de la normale, jusqu’à son signe, est trouvée en raccordant un plan aux sommets, sans tenir compte de la façon dont les sommets sont connectés.</span><span class="sxs-lookup"><span data-stu-id="0045d-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="0045d-125">Il est prévu que les données d’entrée se trouvent approximativement dans le plan ; dans le cas contraire, la projection perpendiculaire à l’un des trois axes de coordonnées peut modifier la géométrie de manière substantielle.</span><span class="sxs-lookup"><span data-stu-id="0045d-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="0045d-126">Le signe de la normale est choisi afin que la somme des zones signées de toutes les contournements d’entrée soit non négative (où un contour à gauche a une zone positive).</span><span class="sxs-lookup"><span data-stu-id="0045d-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="0045d-127">Le normal fourni persiste jusqu’à ce qu’un autre appel à **gluTessNormal** le modifie.</span><span class="sxs-lookup"><span data-stu-id="0045d-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="0045d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0045d-128">Requirements</span></span>



| <span data-ttu-id="0045d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0045d-129">Requirement</span></span> | <span data-ttu-id="0045d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0045d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0045d-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0045d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0045d-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0045d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0045d-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0045d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0045d-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0045d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0045d-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="0045d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0045d-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="0045d-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0045d-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0045d-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="0045d-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0045d-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0045d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0045d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0045d-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0045d-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0045d-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0045d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0045d-142">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="0045d-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="0045d-143">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="0045d-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="0045d-144">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="0045d-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





