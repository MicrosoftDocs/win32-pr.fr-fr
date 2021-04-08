---
title: fonction glColorMask (GL. h)
description: La fonction glColorMask active et désactive l’écriture des composants de couleur de mémoire tampon de trame.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask fonction OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843277"
---
# <a name="glcolormask-function"></a><span data-ttu-id="819ea-104">glColorMask fonction)</span><span class="sxs-lookup"><span data-stu-id="819ea-104">glColorMask function</span></span>

<span data-ttu-id="819ea-105">La fonction **glColorMask** active et désactive l’écriture des composants de couleur de mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="819ea-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="819ea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="819ea-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="819ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="819ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="819ea-108">*rouge*</span><span class="sxs-lookup"><span data-stu-id="819ea-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="819ea-109">Spécifiez si le rouge peut ou ne peut pas être écrit dans le trame.</span><span class="sxs-lookup"><span data-stu-id="819ea-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="819ea-110">Les valeurs par défaut sont GL \_ true, indiquant que le composant Color peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="819ea-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="819ea-111">*écologie*</span><span class="sxs-lookup"><span data-stu-id="819ea-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="819ea-112">Spécifiez si le vert peut ou ne peut pas être écrit dans le trame.</span><span class="sxs-lookup"><span data-stu-id="819ea-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="819ea-113">La valeur par défaut est GL \_ true, indiquant que le composant Color peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="819ea-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="819ea-114">*bleu*</span><span class="sxs-lookup"><span data-stu-id="819ea-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="819ea-115">Spécifiez si le bleu peut ou ne peut pas être écrit dans le trame.</span><span class="sxs-lookup"><span data-stu-id="819ea-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="819ea-116">La valeur par défaut est GL \_ true, indiquant que le composant Color peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="819ea-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="819ea-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="819ea-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="819ea-118">Spécifiez si alpha peut ou ne peut pas être écrit dans le trame.</span><span class="sxs-lookup"><span data-stu-id="819ea-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="819ea-119">La valeur par défaut est GL \_ true, indiquant que le composant Color peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="819ea-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="819ea-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="819ea-120">Return value</span></span>

<span data-ttu-id="819ea-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="819ea-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="819ea-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="819ea-122">Error codes</span></span>

<span data-ttu-id="819ea-123">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="819ea-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="819ea-124">Nom</span><span class="sxs-lookup"><span data-stu-id="819ea-124">Name</span></span>                                                                                                  | <span data-ttu-id="819ea-125">Signification</span><span class="sxs-lookup"><span data-stu-id="819ea-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="819ea-126"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="819ea-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="819ea-127">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="819ea-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="819ea-128">Notes</span><span class="sxs-lookup"><span data-stu-id="819ea-128">Remarks</span></span>

<span data-ttu-id="819ea-129">La fonction **glColorMask** spécifie si les composants de couleur individuels du trame peuvent ou ne peuvent pas être écrits.</span><span class="sxs-lookup"><span data-stu-id="819ea-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="819ea-130">Si le *rouge* est \_ défini sur GL false, par exemple, aucune modification n’est apportée au composant rouge d’un pixel dans une des mémoires tampons de couleur, quelle que soit l’opération de dessin tentée.</span><span class="sxs-lookup"><span data-stu-id="819ea-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="819ea-131">Les modifications apportées aux différents bits des composants ne peuvent pas être contrôlées.</span><span class="sxs-lookup"><span data-stu-id="819ea-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="819ea-132">Au lieu de cela, les modifications sont activées ou désactivées pour l’ensemble des composants de couleur.</span><span class="sxs-lookup"><span data-stu-id="819ea-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="819ea-133">Les fonctions suivantes récupèrent les informations relatives à **glColorMask**:</span><span class="sxs-lookup"><span data-stu-id="819ea-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="819ea-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ couleur \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="819ea-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="819ea-135">**glGet** avec argument GL \_ RVBA \_ mode</span><span class="sxs-lookup"><span data-stu-id="819ea-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="819ea-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="819ea-136">Requirements</span></span>



| <span data-ttu-id="819ea-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="819ea-137">Requirement</span></span> | <span data-ttu-id="819ea-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="819ea-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="819ea-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="819ea-139">Minimum supported client</span></span><br/> | <span data-ttu-id="819ea-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="819ea-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="819ea-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="819ea-141">Minimum supported server</span></span><br/> | <span data-ttu-id="819ea-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="819ea-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="819ea-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="819ea-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="819ea-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="819ea-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="819ea-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="819ea-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="819ea-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="819ea-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="819ea-147">DLL</span><span class="sxs-lookup"><span data-stu-id="819ea-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="819ea-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="819ea-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="819ea-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="819ea-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819ea-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="819ea-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="819ea-151">**glColor**</span><span class="sxs-lookup"><span data-stu-id="819ea-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="819ea-152">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="819ea-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="819ea-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="819ea-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="819ea-154">**glGet**</span><span class="sxs-lookup"><span data-stu-id="819ea-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="819ea-155">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="819ea-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="819ea-156">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="819ea-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="819ea-157">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="819ea-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





