---
title: fonction glAreTexturesResident (GL. h)
description: La fonction glAreTexturesResident détermine si les objets texture spécifiés résident dans la mémoire de texture.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident fonction OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513790"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="fc151-104">glAreTexturesResident fonction)</span><span class="sxs-lookup"><span data-stu-id="fc151-104">glAreTexturesResident function</span></span>

<span data-ttu-id="fc151-105">La fonction **glAreTexturesResident** détermine si les objets texture spécifiés résident dans la mémoire de texture.</span><span class="sxs-lookup"><span data-stu-id="fc151-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc151-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc151-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="fc151-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc151-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc151-108">*n*</span><span class="sxs-lookup"><span data-stu-id="fc151-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="fc151-109">Nombre de textures à interroger.</span><span class="sxs-lookup"><span data-stu-id="fc151-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="fc151-110">*texture*</span><span class="sxs-lookup"><span data-stu-id="fc151-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="fc151-111">Adresse d’un tableau contenant les noms des textures à interroger.</span><span class="sxs-lookup"><span data-stu-id="fc151-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="fc151-112">*foyers*</span><span class="sxs-lookup"><span data-stu-id="fc151-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="fc151-113">Adresse d’un tableau dans lequel l’état de résidence de la texture est retourné.</span><span class="sxs-lookup"><span data-stu-id="fc151-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="fc151-114">L’état de résidence d’une texture nommée par un élément de *textures* est retourné dans l’élément correspondant de *résidences*.</span><span class="sxs-lookup"><span data-stu-id="fc151-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="fc151-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fc151-115">Error codes</span></span>

<span data-ttu-id="fc151-116">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fc151-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fc151-117">Nom</span><span class="sxs-lookup"><span data-stu-id="fc151-117">Name</span></span>                                                                                                  | <span data-ttu-id="fc151-118">Signification</span><span class="sxs-lookup"><span data-stu-id="fc151-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc151-119"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc151-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fc151-120">*n* était une valeur négative, un élément dans *textures* était égal à zéro, ou un élément dans les *textures* ne contenait pas d’identificateur de texture.</span><span class="sxs-lookup"><span data-stu-id="fc151-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="fc151-121"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc151-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fc151-122">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fc151-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="fc151-123">Notes</span><span class="sxs-lookup"><span data-stu-id="fc151-123">Remarks</span></span>

<span data-ttu-id="fc151-124">Sur les ordinateurs avec une quantité limitée de mémoire de texture, OpenGL établit une plage de travail de textures résidant dans la mémoire de texture.</span><span class="sxs-lookup"><span data-stu-id="fc151-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="fc151-125">Ces textures peuvent être liées à une cible de texture bien plus efficacement que les textures qui ne résident pas.</span><span class="sxs-lookup"><span data-stu-id="fc151-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="fc151-126">La fonction **glAreTexturesResident** interroge l’état de résidence des *n* textures désignées par les éléments de *textures*.</span><span class="sxs-lookup"><span data-stu-id="fc151-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="fc151-127">Si toutes les textures nommées résident, **glAreTexturesResident** retourne \_ la valeur GL true et le contenu des *résidences* n’est pas perturbé.</span><span class="sxs-lookup"><span data-stu-id="fc151-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="fc151-128">Si l’une des textures nommées n’est pas résidente, **glAreTexturesResident** retourne GL \_ false et l’état détaillé est retourné dans les *n* éléments de *résidences*.</span><span class="sxs-lookup"><span data-stu-id="fc151-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="fc151-129">Si un élément de *résidences* est \_ le GL true, la texture nommée par l’élément de *textures* correspondant réside dans la mémoire de texture.</span><span class="sxs-lookup"><span data-stu-id="fc151-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="fc151-130">Pour interroger l’état de résidence d’une texture à liaison unique, appelez [**glGetTexParameter**](glgettexparameter.md) avec le paramètre *target* défini sur la texture cible à laquelle la cible est liée et définissez le paramètre *pname* sur la texture du grand livre \_ \_ résident.</span><span class="sxs-lookup"><span data-stu-id="fc151-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="fc151-131">Vous devez utiliser cette méthode pour interroger l’État résident d’une texture par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc151-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="fc151-132">Vous ne pouvez pas inclure des **glAreTexturesResident** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fc151-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="fc151-133">La fonction **glAreTexturesResident** retourne l’état de résidence des textures au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="fc151-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="fc151-134">Cela ne garantit pas que les textures restent résidentes à tout moment.</span><span class="sxs-lookup"><span data-stu-id="fc151-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="fc151-135">Si les textures résident dans la mémoire virtuelle (il n’y a pas de mémoire de texture), elles sont considérées comme toujours résidentes.</span><span class="sxs-lookup"><span data-stu-id="fc151-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="fc151-136">La fonction **glAreTexturesResident** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fc151-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc151-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc151-137">Requirements</span></span>



| <span data-ttu-id="fc151-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc151-138">Requirement</span></span> | <span data-ttu-id="fc151-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc151-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc151-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc151-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fc151-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc151-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fc151-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc151-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fc151-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc151-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc151-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc151-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc151-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc151-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fc151-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc151-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc151-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc151-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc151-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fc151-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc151-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc151-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc151-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc151-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc151-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fc151-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fc151-152">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="fc151-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="fc151-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fc151-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fc151-154">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fc151-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="fc151-155">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="fc151-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="fc151-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fc151-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fc151-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="fc151-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





