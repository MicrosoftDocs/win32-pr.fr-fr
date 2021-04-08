---
title: fonction glPrioritizeTextures (GL. h)
description: La fonction glPrioritizeTextures définit la priorité de résidence des textures.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glPrioritizeTextures fonction OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740645"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="478c1-104">glPrioritizeTextures fonction)</span><span class="sxs-lookup"><span data-stu-id="478c1-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="478c1-105">La fonction **glPrioritizeTextures** définit la priorité de résidence des textures.</span><span class="sxs-lookup"><span data-stu-id="478c1-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="478c1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="478c1-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="478c1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="478c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="478c1-108">*n*</span><span class="sxs-lookup"><span data-stu-id="478c1-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="478c1-109">Nombre de textures à classer par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="478c1-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="478c1-110">*texture*</span><span class="sxs-lookup"><span data-stu-id="478c1-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="478c1-111">Pointeur vers le premier élément d’un tableau contenant les noms des textures à classer par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="478c1-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="478c1-112">*priorité*</span><span class="sxs-lookup"><span data-stu-id="478c1-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="478c1-113">Pointeur vers le premier élément d’un tableau contenant les priorités de texture.</span><span class="sxs-lookup"><span data-stu-id="478c1-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="478c1-114">Une priorité donnée dans un élément *du paramètre* Priorities s’applique à la texture nommée par l’élément correspondant du paramètre *textures* .</span><span class="sxs-lookup"><span data-stu-id="478c1-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="478c1-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="478c1-115">Return value</span></span>

<span data-ttu-id="478c1-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="478c1-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="478c1-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="478c1-117">Error codes</span></span>

<span data-ttu-id="478c1-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="478c1-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="478c1-119">Nom</span><span class="sxs-lookup"><span data-stu-id="478c1-119">Name</span></span>                                                                                                  | <span data-ttu-id="478c1-120">Signification</span><span class="sxs-lookup"><span data-stu-id="478c1-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="478c1-121"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="478c1-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="478c1-122">*n* était une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="478c1-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="478c1-123"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="478c1-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="478c1-124">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="478c1-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="478c1-125">Notes</span><span class="sxs-lookup"><span data-stu-id="478c1-125">Remarks</span></span>

<span data-ttu-id="478c1-126">La fonction **glPrioritizeTextures** affecte *les n textures de texture* spécifiées dans le paramètre *priorités* aux *n* textures nommées dans le paramètre *textures* .</span><span class="sxs-lookup"><span data-stu-id="478c1-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="478c1-127">Sur les ordinateurs avec une quantité limitée de mémoire de texture, OpenGL établit une « plage de travail » de textures résidant dans la mémoire de texture.</span><span class="sxs-lookup"><span data-stu-id="478c1-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="478c1-128">Ces textures peuvent être liées à une cible de texture bien plus efficacement que les textures qui ne résident pas.</span><span class="sxs-lookup"><span data-stu-id="478c1-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="478c1-129">En spécifiant une priorité pour chaque texture, la fonction **glPrioritizeTextures** vous permet de déterminer les textures qui doivent résider.</span><span class="sxs-lookup"><span data-stu-id="478c1-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="478c1-130">Les éléments de priorité de texture des *priorités* sont bloqués à la plage \[ 0,0, 1,0 \] avant d’être attribués.</span><span class="sxs-lookup"><span data-stu-id="478c1-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="478c1-131">Zéro indique la priorité la plus faible ; par conséquent, les textures avec la priorité zéro sont les moins susceptibles d’être résidentes.</span><span class="sxs-lookup"><span data-stu-id="478c1-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="478c1-132">La valeur 1,0 indique la priorité la plus élevée ; par conséquent, les textures avec la priorité 1,0 sont très probablement résidentes.</span><span class="sxs-lookup"><span data-stu-id="478c1-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="478c1-133">Toutefois, il n’est pas garanti que les textures résident tant qu’elles ne sont pas liées.</span><span class="sxs-lookup"><span data-stu-id="478c1-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="478c1-134">La fonction **glPrioritizeTextures** ignore les tentatives de hiérarchisation de texture 0, ou tout nom de texture qui ne correspond pas à une texture existante.</span><span class="sxs-lookup"><span data-stu-id="478c1-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="478c1-135">Aucune des fonctions nommées par le paramètre *textures* ne doit être liée à une cible de texture.</span><span class="sxs-lookup"><span data-stu-id="478c1-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="478c1-136">Si une texture est actuellement liée, vous pouvez également utiliser la fonction [**glTexParameter**](gltexparameter-functions.md) pour définir sa priorité.</span><span class="sxs-lookup"><span data-stu-id="478c1-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="478c1-137">Il s’agit de la seule façon de définir la priorité d’une texture par défaut.</span><span class="sxs-lookup"><span data-stu-id="478c1-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="478c1-138">Vous pouvez inclure des **glPrioritizeTextures** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="478c1-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="478c1-139">La fonction suivante récupère la priorité d’une texture actuellement liée à **glPrioritizeTextures**:</span><span class="sxs-lookup"><span data-stu-id="478c1-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="478c1-140">[**glGetTexParameter**](glgettexparameter.md) avec le nom de paramètre \_ priorité de texture GL \_</span><span class="sxs-lookup"><span data-stu-id="478c1-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="478c1-141">La fonction **glPrioritizeTextures** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="478c1-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="478c1-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="478c1-142">Requirements</span></span>



| <span data-ttu-id="478c1-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="478c1-143">Requirement</span></span> | <span data-ttu-id="478c1-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="478c1-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="478c1-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="478c1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="478c1-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="478c1-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="478c1-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="478c1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="478c1-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="478c1-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="478c1-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="478c1-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="478c1-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="478c1-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="478c1-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="478c1-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="478c1-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="478c1-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="478c1-153">DLL</span><span class="sxs-lookup"><span data-stu-id="478c1-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="478c1-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="478c1-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="478c1-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="478c1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478c1-156">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="478c1-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="478c1-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="478c1-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="478c1-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="478c1-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="478c1-159">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="478c1-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="478c1-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="478c1-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="478c1-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="478c1-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="478c1-162">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="478c1-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





