---
title: gluCylinder, fonction (Glu. h)
description: La fonction gluCylinder dessine un cylindre.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder fonction OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531619"
---
# <a name="glucylinder-function"></a><span data-ttu-id="38526-104">gluCylinder fonction)</span><span class="sxs-lookup"><span data-stu-id="38526-104">gluCylinder function</span></span>

<span data-ttu-id="38526-105">La fonction **gluCylinder** dessine un cylindre.</span><span class="sxs-lookup"><span data-stu-id="38526-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="38526-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38526-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="38526-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38526-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38526-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="38526-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="38526-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="38526-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="38526-110">*baseRadius*</span><span class="sxs-lookup"><span data-stu-id="38526-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="38526-111">Rayon de la bouteille à *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="38526-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="38526-112">*Rayon*</span><span class="sxs-lookup"><span data-stu-id="38526-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="38526-113">Rayon de la bouteille à la   =  *hauteur* z.</span><span class="sxs-lookup"><span data-stu-id="38526-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="38526-114">*height*</span><span class="sxs-lookup"><span data-stu-id="38526-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="38526-115">Hauteur du cylindre.</span><span class="sxs-lookup"><span data-stu-id="38526-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="38526-116">*fraction*</span><span class="sxs-lookup"><span data-stu-id="38526-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="38526-117">Nombre de sous-divisions autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="38526-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="38526-118">*piles*</span><span class="sxs-lookup"><span data-stu-id="38526-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="38526-119">Nombre de sous-divisions le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="38526-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38526-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38526-120">Return value</span></span>

<span data-ttu-id="38526-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="38526-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38526-122">Notes</span><span class="sxs-lookup"><span data-stu-id="38526-122">Remarks</span></span>

<span data-ttu-id="38526-123">La fonction **gluCylinder** dessine un cylindre orienté le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="38526-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="38526-124">La base du cylindre est placée à *z* = 0 et la hauteur en haut à *z*  =  .</span><span class="sxs-lookup"><span data-stu-id="38526-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="38526-125">À l’instar d’une sphère, un cylindre est divisé autour de l’axe z en tranches et le long de l’axe z en piles.</span><span class="sxs-lookup"><span data-stu-id="38526-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="38526-126">Notez que si la valeur de la valeur de *rayon* est égale à zéro, cette routine générera un cône.</span><span class="sxs-lookup"><span data-stu-id="38526-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="38526-127">Si l’orientation est définie sur GLU \_ en dehors de (avec [**gluQuadricOrientation**](gluquadricorientation.md)), les normales générées pointent à l’extérieur de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="38526-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="38526-128">Dans le cas contraire, ils pointent vers l’axe z.</span><span class="sxs-lookup"><span data-stu-id="38526-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="38526-129">Si la texturation est activée (avec [**gluQuadricTexture**](gluquadrictexture.md)) : des coordonnées de texture sont générées de façon à ce que *t* s’étende de manière linéaire de 0,0 à *z* = 0 à 1,0 à   =  la *hauteur* z ; et *s* s’étendent de 0,0 à l’axe des y positif, à 0,25 à l’axe des x positif, à 0,5 à l’axe y négatif, à 0,75 à l’axe des x négatif, et à 1,0 à l’axe des y</span><span class="sxs-lookup"><span data-stu-id="38526-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="38526-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38526-130">Requirements</span></span>



| <span data-ttu-id="38526-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38526-131">Requirement</span></span> | <span data-ttu-id="38526-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="38526-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38526-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38526-133">Minimum supported client</span></span><br/> | <span data-ttu-id="38526-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38526-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="38526-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38526-135">Minimum supported server</span></span><br/> | <span data-ttu-id="38526-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38526-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="38526-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="38526-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="38526-138"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="38526-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="38526-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38526-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="38526-140"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38526-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="38526-141">DLL</span><span class="sxs-lookup"><span data-stu-id="38526-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38526-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38526-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38526-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38526-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38526-144">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="38526-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="38526-145">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="38526-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="38526-146">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="38526-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="38526-147">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="38526-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="38526-148">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="38526-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="38526-149">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="38526-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





