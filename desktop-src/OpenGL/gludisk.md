---
title: gluDisk, fonction (Glu. h)
description: La fonction gluDisk dessine un disque.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk fonction OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032828"
---
# <a name="gludisk-function"></a><span data-ttu-id="91f58-104">gluDisk fonction)</span><span class="sxs-lookup"><span data-stu-id="91f58-104">gluDisk function</span></span>

<span data-ttu-id="91f58-105">La fonction **gluDisk** dessine un disque.</span><span class="sxs-lookup"><span data-stu-id="91f58-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91f58-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="91f58-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91f58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91f58-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="91f58-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="91f58-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="91f58-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="91f58-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="91f58-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="91f58-111">Rayon interne du disque (peut être égal à zéro).</span><span class="sxs-lookup"><span data-stu-id="91f58-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="91f58-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="91f58-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="91f58-113">Rayon externe du disque.</span><span class="sxs-lookup"><span data-stu-id="91f58-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="91f58-114">*fraction*</span><span class="sxs-lookup"><span data-stu-id="91f58-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="91f58-115">Nombre de sous-divisions autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="91f58-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="91f58-116">*boucles*</span><span class="sxs-lookup"><span data-stu-id="91f58-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="91f58-117">Nombre de sonneries concentriques sur l’origine dans laquelle le disque est subdivisé.</span><span class="sxs-lookup"><span data-stu-id="91f58-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91f58-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91f58-118">Return value</span></span>

<span data-ttu-id="91f58-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="91f58-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f58-120">Notes</span><span class="sxs-lookup"><span data-stu-id="91f58-120">Remarks</span></span>

<span data-ttu-id="91f58-121">La fonction **gluDisk** restitue un disque sur le plan *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="91f58-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="91f58-122">Le disque a un rayon de *outerRadius* et contient un trou circulaire concentrique avec un rayon de *innerRadius*.</span><span class="sxs-lookup"><span data-stu-id="91f58-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="91f58-123">Si *innerRadius* a la valeur 0, aucun trou n’est généré.</span><span class="sxs-lookup"><span data-stu-id="91f58-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="91f58-124">Le disque est divisé autour de l’axe z en tranches (comme les tranches de pizzas), ainsi que sur l’axe z dans les anneaux (comme spécifié par les *tranches* et les *boucles*, respectivement).</span><span class="sxs-lookup"><span data-stu-id="91f58-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="91f58-125">En ce qui concerne l’orientation, le côté *z* positif du disque est considéré comme *extérieur* (voir [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="91f58-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="91f58-126">Cela signifie que si l’orientation est définie sur GLU \_ en dehors de, les normales sont générées le long de l’axe z positif.</span><span class="sxs-lookup"><span data-stu-id="91f58-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="91f58-127">Si la texturation est activée (avec [**gluQuadricTexture**](gluquadrictexture.md)), des coordonnées de texture sont générées de façon linéaire, où *r*  =  *outerRadius*, la valeur de (*r*, 0, 0) est (1, 0,5); à (0, *r*, 0) il est (0,5, 1); à (-*r*, 0, 0) il est (0, 0,5); et à (0,-*r*, 0) il est (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="91f58-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="91f58-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91f58-128">Requirements</span></span>



| <span data-ttu-id="91f58-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91f58-129">Requirement</span></span> | <span data-ttu-id="91f58-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="91f58-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="91f58-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91f58-131">Minimum supported client</span></span><br/> | <span data-ttu-id="91f58-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91f58-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="91f58-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91f58-133">Minimum supported server</span></span><br/> | <span data-ttu-id="91f58-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91f58-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="91f58-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="91f58-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="91f58-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="91f58-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="91f58-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91f58-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="91f58-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91f58-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="91f58-139">DLL</span><span class="sxs-lookup"><span data-stu-id="91f58-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91f58-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91f58-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f58-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91f58-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f58-142">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="91f58-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="91f58-143">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="91f58-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="91f58-144">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="91f58-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="91f58-145">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="91f58-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="91f58-146">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="91f58-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="91f58-147">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="91f58-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





