---
title: fonction glDeleteTextures (GL. h)
description: La fonction glDeleteTextures supprime les textures nommées.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- glDeleteTextures fonction OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464614"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="b9b61-104">glDeleteTextures fonction)</span><span class="sxs-lookup"><span data-stu-id="b9b61-104">glDeleteTextures function</span></span>

<span data-ttu-id="b9b61-105">La fonction **glDeleteTextures** supprime les textures nommées.</span><span class="sxs-lookup"><span data-stu-id="b9b61-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b61-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9b61-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="b9b61-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9b61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9b61-108">*n*</span><span class="sxs-lookup"><span data-stu-id="b9b61-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="b9b61-109">Nombre de textures à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b9b61-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="b9b61-110">*texture*</span><span class="sxs-lookup"><span data-stu-id="b9b61-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="b9b61-111">Tableau de textures à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b9b61-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9b61-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9b61-112">Return value</span></span>

<span data-ttu-id="b9b61-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b9b61-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9b61-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b9b61-114">Error codes</span></span>

<span data-ttu-id="b9b61-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b9b61-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b9b61-116">Nom</span><span class="sxs-lookup"><span data-stu-id="b9b61-116">Name</span></span>                                                                                                  | <span data-ttu-id="b9b61-117">Signification</span><span class="sxs-lookup"><span data-stu-id="b9b61-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9b61-118"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9b61-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b9b61-119">*n* était une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="b9b61-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="b9b61-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9b61-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b9b61-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b9b61-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9b61-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b9b61-122">Remarks</span></span>

<span data-ttu-id="b9b61-123">La fonction **glDeleteTextures** supprime *n* textures nommées par les éléments du tableau *textures*.</span><span class="sxs-lookup"><span data-stu-id="b9b61-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="b9b61-124">Une fois qu’une texture est supprimée, elle n’a pas de contenu ou de dimensionnalité, et son nom est libre en vue de sa réutilisation (par exemple, par **glGenTextures**).</span><span class="sxs-lookup"><span data-stu-id="b9b61-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="b9b61-125">La fonction **glDeleteTextures** ignore les zéros et les noms qui ne correspondent pas aux textures existantes.</span><span class="sxs-lookup"><span data-stu-id="b9b61-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="b9b61-126">Si une texture actuellement liée est supprimée, la liaison revient à zéro (texture par défaut).</span><span class="sxs-lookup"><span data-stu-id="b9b61-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="b9b61-127">Vous ne pouvez pas inclure d’appels à **glDeleteTextures** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b9b61-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="b9b61-128">La fonction **glDeleteTextures** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b9b61-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="b9b61-129">La fonction suivante récupère des informations relatives à **glDeleteTextures**:</span><span class="sxs-lookup"><span data-stu-id="b9b61-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="b9b61-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="b9b61-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="b9b61-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9b61-131">Requirements</span></span>



| <span data-ttu-id="b9b61-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9b61-132">Requirement</span></span> | <span data-ttu-id="b9b61-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9b61-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b61-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9b61-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b9b61-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9b61-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9b61-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9b61-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b9b61-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9b61-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9b61-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9b61-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9b61-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9b61-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b9b61-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9b61-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9b61-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9b61-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9b61-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b9b61-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9b61-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9b61-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9b61-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9b61-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b61-145">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="b9b61-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="b9b61-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b9b61-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b9b61-147">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="b9b61-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="b9b61-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b9b61-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b9b61-149">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="b9b61-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="b9b61-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b9b61-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b9b61-151">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="b9b61-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="b9b61-152">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="b9b61-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="b9b61-153">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="b9b61-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="b9b61-154">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="b9b61-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="b9b61-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b9b61-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b9b61-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b9b61-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b9b61-157">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="b9b61-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





