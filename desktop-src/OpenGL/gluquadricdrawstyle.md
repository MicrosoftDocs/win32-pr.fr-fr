---
title: gluQuadricDrawStyle, fonction (Glu. h)
description: La fonction gluQuadricDrawStyle spécifie le style de dessin souhaité pour Quadrics.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942509"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="15782-104">gluQuadricDrawStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="15782-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="15782-105">La fonction **gluQuadricDrawStyle** spécifie le style de dessin souhaité pour Quadrics.</span><span class="sxs-lookup"><span data-stu-id="15782-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="15782-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15782-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="15782-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15782-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15782-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="15782-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="15782-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="15782-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="15782-110">*drawStyle*</span><span class="sxs-lookup"><span data-stu-id="15782-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="15782-111">Style de dessin souhaité.</span><span class="sxs-lookup"><span data-stu-id="15782-111">The desired draw style.</span></span> <span data-ttu-id="15782-112">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="15782-112">The following values are valid.</span></span>



| <span data-ttu-id="15782-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="15782-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="15782-114">Signification</span><span class="sxs-lookup"><span data-stu-id="15782-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="15782-115"><dt>**GLU \_ remplissage**</dt></span><span class="sxs-lookup"><span data-stu-id="15782-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="15782-116">Les Quadrics sont rendus avec des primitives de polygone.</span><span class="sxs-lookup"><span data-stu-id="15782-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="15782-117">Les polygones sont dessinés dans le sens inverse des aiguilles d’une déroute en ce qui concerne leurs normales (comme défini avec [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="15782-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="15782-118"><dt>**\_ligne Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="15782-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="15782-119">Les Quadrics sont rendus sous la forme d’un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="15782-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="15782-120"><dt>**\_silhouette Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="15782-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="15782-121">Les Quadrics sont rendus sous la forme d’un ensemble de lignes, sauf que les bords qui délimitent les visages coplanés ne sont pas dessinés.</span><span class="sxs-lookup"><span data-stu-id="15782-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="15782-122"><dt>**\_point Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="15782-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="15782-123">Les Quadrics sont rendus sous la forme d’un ensemble de points.</span><span class="sxs-lookup"><span data-stu-id="15782-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15782-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15782-124">Return value</span></span>

<span data-ttu-id="15782-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="15782-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15782-126">Notes</span><span class="sxs-lookup"><span data-stu-id="15782-126">Remarks</span></span>

<span data-ttu-id="15782-127">La fonction **gluQuadricDrawStyle** spécifie le style de dessin pour Quadrics rendu avec **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="15782-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15782-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15782-128">Requirements</span></span>



| <span data-ttu-id="15782-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15782-129">Requirement</span></span> | <span data-ttu-id="15782-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="15782-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15782-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15782-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15782-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15782-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="15782-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15782-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15782-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15782-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15782-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="15782-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="15782-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="15782-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="15782-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15782-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="15782-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15782-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="15782-139">DLL</span><span class="sxs-lookup"><span data-stu-id="15782-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15782-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15782-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15782-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15782-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15782-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="15782-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="15782-143">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="15782-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="15782-144">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="15782-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="15782-145">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="15782-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





