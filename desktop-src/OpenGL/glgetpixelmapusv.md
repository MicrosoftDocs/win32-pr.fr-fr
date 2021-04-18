---
title: fonction glGetPixelMapusv (GL. h)
description: Les fonctions glGetPixelMapfv, glGetPixelMapuiv et glGetPixelMapusv retournent la carte de pixels spécifiée. | fonction glGetPixelMapusv (GL. h)
ms.assetid: 68b71f9b-5666-4183-aeb8-4c9f09bc5d9c
keywords:
- glGetPixelMapusv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91d7784288c7a98b82814cdaadb352e7ff5b5c3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520269"
---
# <a name="glgetpixelmapusv-function"></a><span data-ttu-id="a9083-105">glGetPixelMapusv fonction)</span><span class="sxs-lookup"><span data-stu-id="a9083-105">glGetPixelMapusv function</span></span>

<span data-ttu-id="a9083-106">Les fonctions [**glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md)et **glGetPixelMapusv** retournent la carte de pixels spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a9083-106">The [**glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md), and **glGetPixelMapusv** functions return the specified pixel map.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9083-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9083-107">Syntax</span></span>


```C++
void WINAPI glGetPixelMapusv(
   GLenum   map,
   GLushort *values
);
```



## <a name="parameters"></a><span data-ttu-id="a9083-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9083-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9083-109">*map*</span><span class="sxs-lookup"><span data-stu-id="a9083-109">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="a9083-110">Nom de la carte de pixels à retourner.</span><span class="sxs-lookup"><span data-stu-id="a9083-110">The name of the pixel map to return.</span></span> <span data-ttu-id="a9083-111">Les valeurs acceptées sont \_ les \_ cartes \_ de pixels GL i \_ à \_ i, les \_ \_ cartes de pixels GL \_ s \_ à \_ s, GL \_ pixel \_ Map \_ i \_ à \_ R, GL \_ pixel \_ Map \_ i \_ à \_ g, GL \_ Pixel Map \_ i à b, GL Pixel Map i à a, GL Pixel Map \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ R \_ to R, GL pixel \_ \_ \_ mapper \_ G \_ à \_ g, GL \_ Pixel Map \_ \_ b \_ to \_ b et GL \_ pixel \_ Map \_ A \_ sur \_ A.</span><span class="sxs-lookup"><span data-stu-id="a9083-111">Accepted values are GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, GL\_PIXEL\_MAP\_I\_TO\_A, GL\_PIXEL\_MAP\_R\_TO\_R, GL\_PIXEL\_MAP\_G\_TO\_G, GL\_PIXEL\_MAP\_B\_TO\_B, and GL\_PIXEL\_MAP\_A\_TO\_A.</span></span>

</dd> <dt>

<span data-ttu-id="a9083-112">*valeurs*</span><span class="sxs-lookup"><span data-stu-id="a9083-112">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="a9083-113">Retourne le contenu de la carte de pixels.</span><span class="sxs-lookup"><span data-stu-id="a9083-113">Returns the pixel map contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9083-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9083-114">Return value</span></span>

<span data-ttu-id="a9083-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a9083-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9083-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a9083-116">Error codes</span></span>

<span data-ttu-id="a9083-117">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a9083-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a9083-118">Nom</span><span class="sxs-lookup"><span data-stu-id="a9083-118">Name</span></span>                                                                                                  | <span data-ttu-id="a9083-119">Signification</span><span class="sxs-lookup"><span data-stu-id="a9083-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9083-120"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9083-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a9083-121">le *mappage* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="a9083-121">*map* was not an accepted value.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="a9083-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9083-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a9083-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a9083-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a9083-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a9083-124">Remarks</span></span>

<span data-ttu-id="a9083-125">Consultez [**glPixelMap**](glpixelmap.md) pour obtenir une description des valeurs acceptables pour le paramètre *Map* .</span><span class="sxs-lookup"><span data-stu-id="a9083-125">See [**glPixelMap**](glpixelmap.md) for a description of the acceptable values for the *map* parameter.</span></span> <span data-ttu-id="a9083-126">La fonction **glGetPixelMap** retourne dans les *valeurs* le contenu de la carte de pixels spécifiée dans *Map*.</span><span class="sxs-lookup"><span data-stu-id="a9083-126">The **glGetPixelMap** function returns in *values* the contents of the pixel map specified in *map*.</span></span> <span data-ttu-id="a9083-127">Utilisez des mappages de pixels pendant l’exécution de [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)et [**glTexImage2D**](glteximage2d.md) pour mapper les index de couleurs, les index de stencil, les composants de couleur et les composants de profondeur à d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="a9083-127">Use pixel maps during the execution of [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), and [**glTexImage2D**](glteximage2d.md) to map color indexes, stencil indexes, color components, and depth components to other values.</span></span>

<span data-ttu-id="a9083-128">Les valeurs entières non signées, si elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne fixe ou à virgule flottante, de sorte que 1,0 correspond à la plus grande valeur entière représentable, et 0,0 correspond à zéro.</span><span class="sxs-lookup"><span data-stu-id="a9083-128">Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero.</span></span> <span data-ttu-id="a9083-129">Les valeurs entières non signées de retour ne sont pas définies si la valeur de mappage n’est pas comprise entre \[ 0 et 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a9083-129">Return unsigned integer values are undefined if the map value was not in the range \[0,1\].</span></span>

<span data-ttu-id="a9083-130">Pour déterminer la taille requise pour *Map*, appelez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec la constante symbolique appropriée.</span><span class="sxs-lookup"><span data-stu-id="a9083-130">To determine the required size of *map*, call [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with the appropriate symbolic constant.</span></span>

<span data-ttu-id="a9083-131">Si une erreur est générée, aucune modification n’est apportée au contenu des *valeurs*.</span><span class="sxs-lookup"><span data-stu-id="a9083-131">If an error is generated, no change is made to the contents of *values*.</span></span>

<span data-ttu-id="a9083-132">Les fonctions suivantes récupèrent les informations relatives à **glGetPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="a9083-132">The following functions retrieve information related to **glGetPixelMap**:</span></span>

<span data-ttu-id="a9083-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec arguments GL \_ pixel \_ Map \_ i \_ à \_ i \_ Size</span><span class="sxs-lookup"><span data-stu-id="a9083-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="a9083-134">**glGet** avec argument GL de \_ correspondance des pixels \_ \_ \_ en \_ s \_</span><span class="sxs-lookup"><span data-stu-id="a9083-134">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="a9083-135">**glGet** avec argument GL de \_ mappage de pixel \_ \_ I \_ à \_ R \_ taille</span><span class="sxs-lookup"><span data-stu-id="a9083-135">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="a9083-136">**glGet** avec argument GL de \_ cartes de pixels \_ \_ I \_ à \_ G \_ taille</span><span class="sxs-lookup"><span data-stu-id="a9083-136">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="a9083-137">**glGet** avec argument GL \_ pixel \_ Map \_ I \_ à \_ B \_ Size</span><span class="sxs-lookup"><span data-stu-id="a9083-137">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="a9083-138">**glGet** avec argument GL \_ pixel \_ Map \_ I \_ en \_ \_ taille</span><span class="sxs-lookup"><span data-stu-id="a9083-138">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="a9083-139">**glGet** avec argument GL de \_ mappage de pixel \_ \_ r \_ à \_ \_ taille r</span><span class="sxs-lookup"><span data-stu-id="a9083-139">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="a9083-140">**glGet** avec argument GL de \_ mappage de pixel \_ \_ g \_ à \_ g \_ taille</span><span class="sxs-lookup"><span data-stu-id="a9083-140">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="a9083-141">**glGet** avec argument GL \_ pixel \_ carte \_ b \_ à \_ b \_ taille</span><span class="sxs-lookup"><span data-stu-id="a9083-141">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="a9083-142">**glGet** avec argument GL \_ pixel \_ mapper \_ a \_ à \_ une \_ taille</span><span class="sxs-lookup"><span data-stu-id="a9083-142">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="a9083-143">**glGet** avec argument table de la \_ carte de pixels max. GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9083-143">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="a9083-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9083-144">Requirements</span></span>



| <span data-ttu-id="a9083-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9083-145">Requirement</span></span> | <span data-ttu-id="a9083-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9083-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9083-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9083-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a9083-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9083-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a9083-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9083-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a9083-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9083-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9083-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9083-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9083-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9083-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a9083-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a9083-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9083-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9083-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9083-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a9083-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9083-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9083-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9083-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9083-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9083-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a9083-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a9083-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="a9083-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="a9083-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="a9083-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="a9083-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a9083-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a9083-162">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a9083-162">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a9083-163">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="a9083-163">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="a9083-164">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="a9083-164">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="a9083-165">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="a9083-165">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="a9083-166">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a9083-166">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a9083-167">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a9083-167">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





