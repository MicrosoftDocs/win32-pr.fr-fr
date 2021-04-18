---
title: gluSphere, fonction (Glu. h)
description: La fonction gluSphere dessine une sphère.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere fonction OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466174"
---
# <a name="glusphere-function"></a><span data-ttu-id="f6b0f-104">gluSphere fonction)</span><span class="sxs-lookup"><span data-stu-id="f6b0f-104">gluSphere function</span></span>

<span data-ttu-id="f6b0f-105">La fonction **gluSphere** dessine une sphère.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b0f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6b0f-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="f6b0f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6b0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b0f-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="f6b0f-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="f6b0f-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="f6b0f-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f6b0f-110">*service*</span><span class="sxs-lookup"><span data-stu-id="f6b0f-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="f6b0f-111">Rayon de la sphère.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="f6b0f-112">*fraction*</span><span class="sxs-lookup"><span data-stu-id="f6b0f-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="f6b0f-113">Nombre de sous-divisions autour de l’axe des z (comme les lignes de longitude).</span><span class="sxs-lookup"><span data-stu-id="f6b0f-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="f6b0f-114">*piles*</span><span class="sxs-lookup"><span data-stu-id="f6b0f-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="f6b0f-115">Nombre de sous-divisions le long de l’axe z (comme les lignes de latitude).</span><span class="sxs-lookup"><span data-stu-id="f6b0f-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6b0f-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f6b0f-116">Return value</span></span>

<span data-ttu-id="f6b0f-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6b0f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f6b0f-118">Remarks</span></span>

<span data-ttu-id="f6b0f-119">La fonction **gluSphere** dessine une sphère du rayon donné centrée autour de l’origine.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="f6b0f-120">La sphère est divisée autour de l’axe z en tranches et le long de l’axe z en piles (comme les lignes de longitude et de latitude).</span><span class="sxs-lookup"><span data-stu-id="f6b0f-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="f6b0f-121">Si l’orientation est définie sur GLU \_ en dehors de (avec **gluQuadricOrientation**), les normales générées pointent à partir du centre de la sphère.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="f6b0f-122">Dans le cas contraire, ils pointent vers le centre de la sphère.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="f6b0f-123">Si la texturation est activée (avec **gluQuadricTexture**) : des coordonnées de texture sont générées afin que *t* s’étende de 0,0 à *z* =-*RADIUS* à 1,0 au   =  *rayon* z (*t* augmente de façon linéaire sur les lignes longitudinales); et *s* vont de 0,0 sur l’axe des y positif, à 0,25 à l’axe des x positif, à 0,5 à l’axe y négatif, à 0,75 à l’axe des x négatif et à la valeur 1,0 sur l’axe des y positif.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b0f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6b0f-124">Requirements</span></span>



| <span data-ttu-id="f6b0f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6b0f-125">Requirement</span></span> | <span data-ttu-id="f6b0f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6b0f-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b0f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6b0f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b0f-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6b0f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f6b0f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6b0f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b0f-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6b0f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6b0f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6b0f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6b0f-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6b0f-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f6b0f-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f6b0f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6b0f-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6b0f-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f6b0f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f6b0f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6b0f-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6b0f-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b0f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6b0f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b0f-138">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-139">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-141">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





