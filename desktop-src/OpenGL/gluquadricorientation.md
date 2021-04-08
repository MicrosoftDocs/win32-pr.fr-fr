---
title: gluQuadricOrientation, fonction (Glu. h)
description: La fonction gluQuadricOrientation spécifie l’orientation à l’intérieur ou à l’extérieur pour Quadrics.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluQuadricOrientation fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739789"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="4828f-104">gluQuadricOrientation fonction)</span><span class="sxs-lookup"><span data-stu-id="4828f-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="4828f-105">La fonction **gluQuadricOrientation** spécifie l’orientation à l’intérieur ou à l’extérieur pour Quadrics.</span><span class="sxs-lookup"><span data-stu-id="4828f-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="4828f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4828f-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="4828f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4828f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4828f-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="4828f-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="4828f-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="4828f-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4828f-110">*orientation*</span><span class="sxs-lookup"><span data-stu-id="4828f-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="4828f-111">Orientation souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4828f-111">The desired orientation.</span></span> <span data-ttu-id="4828f-112">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="4828f-112">The following values are valid.</span></span>



| <span data-ttu-id="4828f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4828f-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="4828f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="4828f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="4828f-115"><dt>**GLU \_ en dehors**</dt></span><span class="sxs-lookup"><span data-stu-id="4828f-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="4828f-116">Dessinez des Quadrics avec des normales pointant vers l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="4828f-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="4828f-117">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4828f-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="4828f-118"><dt>**GLU \_ dans**</dt></span><span class="sxs-lookup"><span data-stu-id="4828f-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="4828f-119">Dessinez des Quadrics avec des normales pointant vers l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="4828f-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4828f-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4828f-120">Return value</span></span>

<span data-ttu-id="4828f-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4828f-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4828f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4828f-122">Remarks</span></span>

<span data-ttu-id="4828f-123">La fonction **gluQuadricOrientation** spécifie le type d’orientation souhaité pour Quadrics rendu avec **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="4828f-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="4828f-124">L’interprétation de l’extérieur et de l’intérieur dépend de l’quadric dessiné.</span><span class="sxs-lookup"><span data-stu-id="4828f-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="4828f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4828f-125">Requirements</span></span>



| <span data-ttu-id="4828f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4828f-126">Requirement</span></span> | <span data-ttu-id="4828f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4828f-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4828f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4828f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4828f-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4828f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4828f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4828f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4828f-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4828f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4828f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4828f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4828f-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4828f-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4828f-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4828f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4828f-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4828f-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4828f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4828f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4828f-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4828f-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4828f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4828f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4828f-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="4828f-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="4828f-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="4828f-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="4828f-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="4828f-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="4828f-142">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="4828f-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





