---
title: gluPartialDisk, fonction (Glu. h)
description: La fonction gluPartialDisk dessine un arc de disque.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk fonction OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511923"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="ff144-104">gluPartialDisk fonction)</span><span class="sxs-lookup"><span data-stu-id="ff144-104">gluPartialDisk function</span></span>

<span data-ttu-id="ff144-105">La fonction **gluPartialDisk** dessine un arc de disque.</span><span class="sxs-lookup"><span data-stu-id="ff144-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff144-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff144-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="ff144-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff144-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff144-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="ff144-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="ff144-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ff144-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="ff144-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-111">Rayon interne du disque partiel (peut être égal à zéro).</span><span class="sxs-lookup"><span data-stu-id="ff144-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="ff144-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="ff144-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-113">Rayon externe du disque partiel.</span><span class="sxs-lookup"><span data-stu-id="ff144-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="ff144-114">*fraction*</span><span class="sxs-lookup"><span data-stu-id="ff144-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-115">Nombre de sous-divisions autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="ff144-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="ff144-116">*boucles*</span><span class="sxs-lookup"><span data-stu-id="ff144-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-117">Nombre de sonneries concentriques sur l’origine dans laquelle le disque partiel est subdivisé.</span><span class="sxs-lookup"><span data-stu-id="ff144-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="ff144-118">*startAngle*</span><span class="sxs-lookup"><span data-stu-id="ff144-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-119">Angle de départ, en degrés, de la partie disque.</span><span class="sxs-lookup"><span data-stu-id="ff144-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="ff144-120">*sweepAngle*</span><span class="sxs-lookup"><span data-stu-id="ff144-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="ff144-121">Angle de balayage, en degrés, de la partie disque.</span><span class="sxs-lookup"><span data-stu-id="ff144-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff144-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff144-122">Return value</span></span>

<span data-ttu-id="ff144-123">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ff144-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff144-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ff144-124">Remarks</span></span>

<span data-ttu-id="ff144-125">La fonction **gluPartialDisk** restitue un disque partiel sur le plan *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="ff144-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="ff144-126">Un disque partiel est similaire à un disque complet, sauf que seul le sous-ensemble du disque de *startAngle* à *startAngle*  +  *SweepAngle* est inclus (où 0 degré est le long de l’axe des y positif, 90 degrés sur l’axe x positif, 180 degrés sur l’axe y négatif et 270 degrés sur l’axe x négatif).</span><span class="sxs-lookup"><span data-stu-id="ff144-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="ff144-127">Le disque partiel a un rayon de *outerRadius* et contient un trou circulaire concentrique avec un rayon de *innerRadius*.</span><span class="sxs-lookup"><span data-stu-id="ff144-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="ff144-128">Si *innerRadius* est égal à zéro, aucun trou n’est généré.</span><span class="sxs-lookup"><span data-stu-id="ff144-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="ff144-129">Le disque partiel est divisé autour de l’axe z en tranches (comme les tranches de pizzas), ainsi que sur l’axe z dans les anneaux (comme spécifié par les *tranches* et les *boucles*, respectivement).</span><span class="sxs-lookup"><span data-stu-id="ff144-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="ff144-130">En ce qui concerne l’orientation, le côté z positif du disque partiel est considéré comme extérieur (voir [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="ff144-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="ff144-131">Cela signifie que si l’orientation est définie sur GLU \_ en dehors de, les normales sont générées le long de l’axe z positif.</span><span class="sxs-lookup"><span data-stu-id="ff144-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="ff144-132">Si vous avez activé la texturation (avec [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** génère des coordonnées de texture linéairement, où *r*  =  *outerRadius*, la valeur de *(r*, 0, 0) est (1, 0,5); à (0, *r*, 0) il est (0,5, 1); à (*r*, 0, 0) il est (0, 0,5); et à (0, *r*, 0) il est (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="ff144-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff144-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff144-133">Requirements</span></span>



| <span data-ttu-id="ff144-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff144-134">Requirement</span></span> | <span data-ttu-id="ff144-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff144-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff144-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff144-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ff144-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff144-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff144-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff144-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ff144-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff144-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff144-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff144-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff144-141"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff144-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ff144-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff144-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff144-143"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff144-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff144-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ff144-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff144-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff144-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff144-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff144-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff144-147">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="ff144-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="ff144-148">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="ff144-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="ff144-149">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="ff144-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="ff144-150">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="ff144-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="ff144-151">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="ff144-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="ff144-152">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="ff144-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





