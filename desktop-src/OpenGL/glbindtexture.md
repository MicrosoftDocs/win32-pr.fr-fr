---
title: fonction glBindTexture (GL. h)
description: La fonction glBindTexture permet la création d’une texture nommée qui est liée à une cible de texture.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture fonction OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384828"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="fe98d-104">glBindTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="fe98d-104">glBindTexture function</span></span>

<span data-ttu-id="fe98d-105">La fonction **glBindTexture** permet la création d’une texture nommée qui est liée à une cible de texture.</span><span class="sxs-lookup"><span data-stu-id="fe98d-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe98d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe98d-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="fe98d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe98d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe98d-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="fe98d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98d-109">Cible à laquelle la texture est liée.</span><span class="sxs-lookup"><span data-stu-id="fe98d-109">The target to which the texture is bound.</span></span> <span data-ttu-id="fe98d-110">Doit avoir la texture GL \_ valeur \_ 1D ou la \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="fe98d-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="fe98d-111">*motif*</span><span class="sxs-lookup"><span data-stu-id="fe98d-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98d-112">Nom d’une texture ; le nom de la texture ne peut pas être actuellement utilisé.</span><span class="sxs-lookup"><span data-stu-id="fe98d-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe98d-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fe98d-113">Return value</span></span>

<span data-ttu-id="fe98d-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fe98d-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe98d-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fe98d-115">Error codes</span></span>

<span data-ttu-id="fe98d-116">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fe98d-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fe98d-117">Nom</span><span class="sxs-lookup"><span data-stu-id="fe98d-117">Name</span></span>                                                                                                  | <span data-ttu-id="fe98d-118">Signification</span><span class="sxs-lookup"><span data-stu-id="fe98d-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe98d-119"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe98d-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fe98d-120">La *cible* du paramètre n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="fe98d-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="fe98d-121"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe98d-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fe98d-122">La *texture* de paramètre n’a pas la même dimensionnalité que la *cible*, ou la fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fe98d-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fe98d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="fe98d-123">Remarks</span></span>

<span data-ttu-id="fe98d-124">La fonction **glBindTexture** vous permet de créer une texture nommée.</span><span class="sxs-lookup"><span data-stu-id="fe98d-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="fe98d-125">L’appel de **glBindTexture** avec *target* défini sur la texture GL \_ \_ 1J ou GL \_ texture \_ 2D, et *texture* définie sur le nom de la nouvelle texture que vous avez créée lie le nom de la texture à la cible de texture appropriée.</span><span class="sxs-lookup"><span data-stu-id="fe98d-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="fe98d-126">Quand une texture est liée à une cible, la liaison précédente pour cette cible n’est plus appliquée.</span><span class="sxs-lookup"><span data-stu-id="fe98d-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="fe98d-127">Les noms de texture sont des entiers non signés dont la valeur zéro est réservée pour représenter la texture par défaut de chaque cible de texture.</span><span class="sxs-lookup"><span data-stu-id="fe98d-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="fe98d-128">Les noms de texture et le contenu de texture correspondant sont locaux à l’espace de liste d’affichage partagé du contexte de rendu OpenGL actuel ; deux contextes de rendu partagent des noms de texture uniquement s’ils partagent également des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fe98d-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="fe98d-129">Vous pouvez générer un ensemble de nouveaux noms de texture à l’aide de [**glGenTextures**](glgentextures.md).</span><span class="sxs-lookup"><span data-stu-id="fe98d-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="fe98d-130">Lorsqu’une texture est liée pour la première fois, elle suppose la dimensionnalité de sa cible de texture ; une texture liée à une \_ texture GL \_ 1D devient unidimensionnelle et une texture liée à la \_ texture GL \_ 2D devient à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="fe98d-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="fe98d-131">Les opérations que vous effectuez sur une cible de texture affectent également une texture liée à la cible.</span><span class="sxs-lookup"><span data-stu-id="fe98d-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="fe98d-132">Lorsque vous interrogez une cible de texture, la valeur de retour est l’état de la texture qui lui est liée.</span><span class="sxs-lookup"><span data-stu-id="fe98d-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="fe98d-133">Les cibles de texture deviennent des alias des textures actuellement liées.</span><span class="sxs-lookup"><span data-stu-id="fe98d-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="fe98d-134">Lorsque vous liez une texture à **glBindTexture**, la liaison reste active jusqu’à ce qu’une texture différente soit liée à la même cible ou que vous supprimiez la texture liée avec la fonction [**glDeleteTextures**](gldeletetextures.md) .</span><span class="sxs-lookup"><span data-stu-id="fe98d-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="fe98d-135">Une fois que vous avez créé une texture nommée, vous pouvez la lier à une cible de texture qui a la même dimensionnalité que le plus souvent nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fe98d-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="fe98d-136">Il est généralement beaucoup plus rapide d’utiliser **glBindTexture** pour lier une texture nommée existante à l’une des cibles de texture que de recharger l’image de texture à l’aide de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="fe98d-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="fe98d-137">Pour contrôler davantage les performances de la texturation, utilisez [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="fe98d-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="fe98d-138">Vous pouvez inclure des appels à **glBindTexture** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fe98d-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="fe98d-139">La fonction **glBindTexture** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fe98d-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="fe98d-140">Les fonctions suivantes récupèrent les informations relatives à **glBindTexture**:</span><span class="sxs-lookup"><span data-stu-id="fe98d-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="fe98d-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ Binding GL texture \_ 1D \_</span><span class="sxs-lookup"><span data-stu-id="fe98d-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="fe98d-142">**glGet** avec argument GL \_ texture \_ 2D \_ liaison</span><span class="sxs-lookup"><span data-stu-id="fe98d-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="fe98d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe98d-143">Requirements</span></span>



| <span data-ttu-id="fe98d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe98d-144">Requirement</span></span> | <span data-ttu-id="fe98d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe98d-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe98d-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe98d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fe98d-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe98d-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fe98d-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe98d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fe98d-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe98d-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe98d-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe98d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe98d-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe98d-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fe98d-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe98d-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe98d-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe98d-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe98d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="fe98d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe98d-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe98d-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe98d-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe98d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe98d-157">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="fe98d-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="fe98d-158">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="fe98d-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="fe98d-159">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="fe98d-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="fe98d-160">**glGet**</span><span class="sxs-lookup"><span data-stu-id="fe98d-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="fe98d-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fe98d-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="fe98d-162">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="fe98d-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="fe98d-163">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="fe98d-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="fe98d-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fe98d-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fe98d-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="fe98d-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="fe98d-166">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fe98d-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





