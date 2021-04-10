---
title: fonction glCullFace (GL. h)
description: La fonction glCullFace spécifie si les facettes frontales ou les faces arrière peuvent être éliminées.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace fonction OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941779"
---
# <a name="glcullface-function"></a><span data-ttu-id="3e754-104">glCullFace fonction)</span><span class="sxs-lookup"><span data-stu-id="3e754-104">glCullFace function</span></span>

<span data-ttu-id="3e754-105">La fonction **glCullFace** spécifie si les facettes frontales ou les faces arrière peuvent être éliminées.</span><span class="sxs-lookup"><span data-stu-id="3e754-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e754-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e754-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="3e754-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e754-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e754-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="3e754-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="3e754-109">Spécifie si les facettes frontales ou les faces arrière sont des candidats pour l’élimination.</span><span class="sxs-lookup"><span data-stu-id="3e754-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="3e754-110">Les constantes symboliques \_ Front-Front, GL \_ Back et GL \_ front \_ et \_ Back sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="3e754-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="3e754-111">La valeur par défaut est \_ back du GL.</span><span class="sxs-lookup"><span data-stu-id="3e754-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e754-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3e754-112">Return value</span></span>

<span data-ttu-id="3e754-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3e754-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e754-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3e754-114">Error codes</span></span>

<span data-ttu-id="3e754-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3e754-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3e754-116">Nom</span><span class="sxs-lookup"><span data-stu-id="3e754-116">Name</span></span>                                                                                                  | <span data-ttu-id="3e754-117">Signification</span><span class="sxs-lookup"><span data-stu-id="3e754-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e754-118"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e754-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3e754-119">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="3e754-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="3e754-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e754-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3e754-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3e754-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3e754-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3e754-122">Remarks</span></span>

<span data-ttu-id="3e754-123">La fonction **glCullFace** spécifie si les facettes avant ou arrière sont éliminées (comme spécifié par le *mode*) lorsque l’élimination des facettes est activée.</span><span class="sxs-lookup"><span data-stu-id="3e754-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="3e754-124">Vous activez et désactivez l’élimination des facettes à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Culling \_ .</span><span class="sxs-lookup"><span data-stu-id="3e754-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="3e754-125">Les facettes sont des triangles, des quadrilatères, des polygones et des rectangles.</span><span class="sxs-lookup"><span data-stu-id="3e754-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="3e754-126">La fonction [**glFrontFace**](glfrontface.md) spécifie les facettes dans le sens des aiguilles d’une montre et de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3e754-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="3e754-127">Si le *mode* est \_ recto- \_ \_ verso et arrière, aucune facette n’est dessinée, mais d’autres primitives, telles que des points et des lignes, sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="3e754-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="3e754-128">Les fonctions suivantes récupèrent les informations relatives à **glCullFace**:</span><span class="sxs-lookup"><span data-stu-id="3e754-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="3e754-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Culling \_ \_ en mode visage</span><span class="sxs-lookup"><span data-stu-id="3e754-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="3e754-130">[**glIsEnabled**](glisenabled.md) avec argument GL \_ élimination \_ visage</span><span class="sxs-lookup"><span data-stu-id="3e754-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="3e754-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e754-131">Requirements</span></span>



| <span data-ttu-id="3e754-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e754-132">Requirement</span></span> | <span data-ttu-id="3e754-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e754-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e754-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e754-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3e754-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e754-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3e754-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e754-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3e754-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e754-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e754-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e754-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e754-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e754-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3e754-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e754-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e754-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e754-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3e754-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3e754-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e754-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e754-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e754-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e754-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e754-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3e754-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3e754-146">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="3e754-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="3e754-147">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="3e754-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="3e754-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3e754-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3e754-149">**glFrontFace**</span><span class="sxs-lookup"><span data-stu-id="3e754-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="3e754-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3e754-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3e754-151">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="3e754-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





