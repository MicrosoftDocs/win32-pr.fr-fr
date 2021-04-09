---
title: fonction glGenTextures (GL. h)
description: La fonction glGenTextures génère des noms de texture.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures fonction OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942740"
---
# <a name="glgentextures-function"></a><span data-ttu-id="181e4-104">glGenTextures fonction)</span><span class="sxs-lookup"><span data-stu-id="181e4-104">glGenTextures function</span></span>

<span data-ttu-id="181e4-105">La fonction **glGenTextures** génère des noms de texture.</span><span class="sxs-lookup"><span data-stu-id="181e4-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="181e4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="181e4-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="181e4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="181e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="181e4-108">*n*</span><span class="sxs-lookup"><span data-stu-id="181e4-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="181e4-109">Nombre de noms de texture à générer.</span><span class="sxs-lookup"><span data-stu-id="181e4-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="181e4-110">*texture*</span><span class="sxs-lookup"><span data-stu-id="181e4-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="181e4-111">Pointeur vers le premier élément d’un tableau dans lequel les noms de texture générés sont stockés.</span><span class="sxs-lookup"><span data-stu-id="181e4-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="181e4-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="181e4-112">Return value</span></span>

<span data-ttu-id="181e4-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="181e4-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="181e4-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="181e4-114">Error codes</span></span>

<span data-ttu-id="181e4-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="181e4-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="181e4-116">Nom</span><span class="sxs-lookup"><span data-stu-id="181e4-116">Name</span></span>                                                                                                  | <span data-ttu-id="181e4-117">Signification</span><span class="sxs-lookup"><span data-stu-id="181e4-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="181e4-118"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="181e4-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="181e4-119">*n* était une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="181e4-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="181e4-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="181e4-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="181e4-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="181e4-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="181e4-122">Notes</span><span class="sxs-lookup"><span data-stu-id="181e4-122">Remarks</span></span>

<span data-ttu-id="181e4-123">La fonction **glGenTextures** retourne *n* noms de texture dans le paramètre *textures* .</span><span class="sxs-lookup"><span data-stu-id="181e4-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="181e4-124">Toutefois, les noms de texture ne sont pas nécessairement un ensemble contigu d’entiers. Toutefois, aucun des noms retournés ne peut être en cours d’utilisation juste avant l’appel de la fonction **glGenTextures** .</span><span class="sxs-lookup"><span data-stu-id="181e4-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="181e4-125">Les textures générées supposent la dimensionnalité de la cible de texture à laquelle elles sont liées pour la première fois avec la fonction [**glBindTexture**](glbindtexture.md) .</span><span class="sxs-lookup"><span data-stu-id="181e4-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="181e4-126">Les noms de texture retournés par **glGenTextures** ne sont pas retournés par les appels suivants à **glGenTextures** , sauf s’ils sont d’abord supprimés en appelant [**glDeleteTextures**](gldeletetextures.md).</span><span class="sxs-lookup"><span data-stu-id="181e4-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="181e4-127">Vous ne pouvez pas inclure des **glGenTextures** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="181e4-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="181e4-128">La fonction **glGenTextures** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="181e4-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="181e4-129">La fonction suivante récupère des informations relatives à **glGenTextures**:</span><span class="sxs-lookup"><span data-stu-id="181e4-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="181e4-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="181e4-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="181e4-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181e4-131">Requirements</span></span>



| <span data-ttu-id="181e4-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181e4-132">Requirement</span></span> | <span data-ttu-id="181e4-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="181e4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="181e4-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181e4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="181e4-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181e4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="181e4-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181e4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="181e4-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181e4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="181e4-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="181e4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="181e4-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="181e4-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="181e4-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="181e4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="181e4-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="181e4-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="181e4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="181e4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="181e4-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="181e4-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181e4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181e4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181e4-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="181e4-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="181e4-146">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="181e4-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="181e4-147">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="181e4-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="181e4-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="181e4-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="181e4-149">**glGet**</span><span class="sxs-lookup"><span data-stu-id="181e4-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="181e4-150">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="181e4-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="181e4-151">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="181e4-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="181e4-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="181e4-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="181e4-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="181e4-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="181e4-154">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="181e4-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





