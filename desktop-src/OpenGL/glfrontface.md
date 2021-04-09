---
title: fonction glFrontFace (GL. h)
description: La fonction glFrontFace définit les polygones frontaux et de face arrière.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace fonction OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942819"
---
# <a name="glfrontface-function"></a><span data-ttu-id="0c9ff-104">glFrontFace fonction)</span><span class="sxs-lookup"><span data-stu-id="0c9ff-104">glFrontFace function</span></span>

<span data-ttu-id="0c9ff-105">La fonction **glFrontFace** définit les polygones frontaux et de face arrière.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9ff-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c9ff-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="0c9ff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c9ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c9ff-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="0c9ff-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="0c9ff-109">Orientation des polygones frontaux.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="0c9ff-110">\_Les wrappers en PV GL et GL \_ sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="0c9ff-111">La valeur par défaut est le \_ CCW GL.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c9ff-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c9ff-112">Return value</span></span>

<span data-ttu-id="0c9ff-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c9ff-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0c9ff-114">Error codes</span></span>

<span data-ttu-id="0c9ff-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0c9ff-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0c9ff-116">Nom</span><span class="sxs-lookup"><span data-stu-id="0c9ff-116">Name</span></span>                                                                                                  | <span data-ttu-id="0c9ff-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0c9ff-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c9ff-118"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ff-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0c9ff-119">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="0c9ff-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ff-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0c9ff-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0c9ff-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0c9ff-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0c9ff-122">Remarks</span></span>

<span data-ttu-id="0c9ff-123">Dans une scène composée entièrement de surfaces fermées opaques, les polygones de l’arrière-plan ne sont jamais visibles.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="0c9ff-124">L’élimination de ces polygones invisibles présente l’avantage évident de accélérer le rendu de l’image.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="0c9ff-125">Vous activez et désactivez l’élimination des polygones de type « arrière » avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) à l’aide de l’argument GL \_ Culling \_ .</span><span class="sxs-lookup"><span data-stu-id="0c9ff-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="0c9ff-126">La projection d’un polygone sur les coordonnées de la fenêtre est dite d’enroulement dans le sens des aiguilles d’une montre si un objet imaginaire suivant le chemin de son premier vertex, son deuxième vertex, etc. jusqu’au dernier vertex, et enfin vers son premier vertex, se déplace dans le sens des aiguilles d’une montre à propos de l’intérieur du polygone.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="0c9ff-127">L’enroulement du polygone est dit être placé dans le sens inverse des aiguilles d’une montre si l’objet imaginaire qui suit le même chemin se déplace dans le sens inverse des aiguilles d’une montre à l’intérieur du polygone.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="0c9ff-128">La fonction **glFrontFace** spécifie si les polygones avec un enroulement dans le sens des aiguilles d’une montre dans les coordonnées de la fenêtre ou dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="0c9ff-129">Le passage \_ du CCW du GL au *mode* sélectionne les polygones dans le sens inverse. Le \_ PV GL sélectionne les polygones dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="0c9ff-130">Par défaut, les polygones à gauche sont pris en face.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="0c9ff-131">La fonction suivante récupère des informations sur **glFrontface**:</span><span class="sxs-lookup"><span data-stu-id="0c9ff-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="0c9ff-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ frontal \_</span><span class="sxs-lookup"><span data-stu-id="0c9ff-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="0c9ff-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c9ff-133">Requirements</span></span>



| <span data-ttu-id="0c9ff-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c9ff-134">Requirement</span></span> | <span data-ttu-id="0c9ff-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c9ff-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9ff-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c9ff-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9ff-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c9ff-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0c9ff-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c9ff-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9ff-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c9ff-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c9ff-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c9ff-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c9ff-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ff-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0c9ff-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c9ff-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c9ff-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ff-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c9ff-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0c9ff-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c9ff-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ff-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c9ff-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c9ff-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9ff-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0c9ff-148">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="0c9ff-149">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="0c9ff-150">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0c9ff-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0c9ff-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="0c9ff-153">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





