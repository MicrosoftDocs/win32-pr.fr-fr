---
title: fonction glGetTexImage (GL. h)
description: La fonction glGetTexImage retourne une image de texture.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512202"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="9ccfc-104">glGetTexImage fonction)</span><span class="sxs-lookup"><span data-stu-id="9ccfc-104">glGetTexImage function</span></span>

<span data-ttu-id="9ccfc-105">La fonction **glGetTexImage** retourne une image de texture.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ccfc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ccfc-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="9ccfc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ccfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ccfc-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="9ccfc-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="9ccfc-109">Spécifie la texture à obtenir.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="9ccfc-110">La \_ texture GL \_ 1D et la \_ texture GL \_ 2D sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfc-111">*level*</span><span class="sxs-lookup"><span data-stu-id="9ccfc-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="9ccfc-112">Numéro de niveau de détail de l’image souhaitée.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="9ccfc-113">Le niveau 0 est le niveau d’image de base.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-113">Level 0 is the base image level.</span></span> <span data-ttu-id="9ccfc-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfc-115">*format*</span><span class="sxs-lookup"><span data-stu-id="9ccfc-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="9ccfc-116">Format de pixel pour les données retournées.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-116">A pixel format for the returned data.</span></span> <span data-ttu-id="9ccfc-117">Les formats pris en charge sont GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ luminance, GL \_ BGR \_ ext, GL \_ BGRA \_ ext et GL \_ luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfc-118">*type*</span><span class="sxs-lookup"><span data-stu-id="9ccfc-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="9ccfc-119">Type de pixel pour les données retournées.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-119">A pixel type for the returned data.</span></span> <span data-ttu-id="9ccfc-120">Les types pris en charge sont \_ octets non signés GL \_ , \_ octet GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfc-121">*pixels*</span><span class="sxs-lookup"><span data-stu-id="9ccfc-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="9ccfc-122">Retourne l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-122">Returns the texture image.</span></span> <span data-ttu-id="9ccfc-123">Doit être un pointeur vers un tableau du type spécifié par *type*.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ccfc-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ccfc-124">Return value</span></span>

<span data-ttu-id="9ccfc-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9ccfc-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9ccfc-126">Error codes</span></span>

<span data-ttu-id="9ccfc-127">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9ccfc-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9ccfc-128">Nom</span><span class="sxs-lookup"><span data-stu-id="9ccfc-128">Name</span></span>                                                                                                  | <span data-ttu-id="9ccfc-129">Signification</span><span class="sxs-lookup"><span data-stu-id="9ccfc-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ccfc-130"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ccfc-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9ccfc-131">la *cible*, le *format* ou le *type* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="9ccfc-132"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ccfc-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9ccfc-133">le *niveau* est inférieur à zéro ou supérieur au *Journal* 2 (*Max*), où *Max* est la valeur retournée de la taille de \_ texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9ccfc-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="9ccfc-134"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ccfc-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9ccfc-135">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="9ccfc-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9ccfc-136">Notes</span><span class="sxs-lookup"><span data-stu-id="9ccfc-136">Remarks</span></span>

<span data-ttu-id="9ccfc-137">La fonction **glGetTexImage** retourne une image de texture en *pixels*.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="9ccfc-138">Le *paramètre Target* spécifie si l’image de texture souhaitée est spécifiée par [**glTexImage1D**](glteximage1d.md)**(** texture GL \_ \_ 1D **)** ou par [**glTexImage2D**](glteximage2d.md)**(** texture GL \_ \_ 2D **)**.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="9ccfc-139">Le paramètre *Level* spécifie le numéro de niveau de détail de l’image souhaitée.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="9ccfc-140">Les paramètres de *type* et de *format* spécifient le format et le type du tableau d’images souhaité.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="9ccfc-141">Pour obtenir une description des valeurs acceptables pour les paramètres de *type* et de *format* , consultez **glTexImage1D** et [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="9ccfc-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="9ccfc-142">L’opération de **glGetTexImage** est mieux comprise en considérant que l’image de texture à quatre composants interne sélectionnée est une mémoire tampon RVBA de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="9ccfc-143">La sémantique des **glGetTexImage** est alors identique à celle de [**glReadPixels**](glreadpixels.md) appelée avec le même *format* et le même *type*, *si x* et *y* ont la valeur zéro, la *largeur* est égale à la largeur de l’image de texture (y compris la bordure si elle a été spécifiée) et la *hauteur* est définie sur une pour les images 1D, ou à la hauteur de l’image de texture (y compris la bordure, si elle a été spécifiée) pour les images 2D.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="9ccfc-144">Étant donné que l’image de texture interne est une image RVBA, les formats de pixels de l' \_ index de couleur GL \_ , de l’index de \_ stencils GL \_ et de la profondeur du GL ne \_ \_ sont pas acceptés, et le type de pixel de la \_ bitmap GL n’est pas accepté.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="9ccfc-145">Si l’image de texture sélectionnée ne contient pas quatre composants, les mappages suivants sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="9ccfc-146">Les textures à un seul composant sont traitées comme des tampons RVBA avec la couleur rouge définie sur la valeur à composant unique, et les valeurs vert, bleu et alpha définies sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="9ccfc-147">Les textures à deux composants sont traitées comme des tampons RVBA, avec le rouge défini sur la valeur du composant zéro, alpha défini sur la valeur du composant 1 et le vert et le bleu définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="9ccfc-148">Enfin, les textures à trois composants sont traitées comme des tampons RVBA avec le rouge défini sur le composant zéro, le vert défini sur le composant 1, le bleu défini sur le deuxième composant et alpha défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="9ccfc-149">Pour déterminer la taille requise des *pixels*, utilisez [**glGetTexLevelParameter**](glgettexlevelparameter.md) pour déterminer les dimensions de l’image de texture interne, puis mettez à l’échelle le nombre requis de pixels par le stockage requis pour chaque pixel, en fonction du *format* et du *type*.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="9ccfc-150">Veillez à prendre en compte les paramètres de stockage en pixels, en particulier l' \_ alignement du Pack GL \_ .</span><span class="sxs-lookup"><span data-stu-id="9ccfc-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="9ccfc-151">Si une erreur est générée, aucune modification n’est apportée au contenu des *pixels*.</span><span class="sxs-lookup"><span data-stu-id="9ccfc-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="9ccfc-152">Les fonctions suivantes récupèrent les informations relatives à **glGetTexImage**:</span><span class="sxs-lookup"><span data-stu-id="9ccfc-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="9ccfc-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument with GL \_ Pack \_ alignment et autres</span><span class="sxs-lookup"><span data-stu-id="9ccfc-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="9ccfc-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) avec l’argument \_ largeur de la texture GL \_</span><span class="sxs-lookup"><span data-stu-id="9ccfc-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="9ccfc-155">**glGetTexLevelParameter** avec argument \_ taille de texture de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="9ccfc-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="9ccfc-156">**glGetTexLevelParameter** avec argument GL \_ texture \_ Border</span><span class="sxs-lookup"><span data-stu-id="9ccfc-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="9ccfc-157">**glGetTexLevelParameter** avec les \_ composants de texture GL d’argument \_</span><span class="sxs-lookup"><span data-stu-id="9ccfc-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="9ccfc-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ccfc-158">Requirements</span></span>



| <span data-ttu-id="9ccfc-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ccfc-159">Requirement</span></span> | <span data-ttu-id="9ccfc-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ccfc-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccfc-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ccfc-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9ccfc-162">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ccfc-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9ccfc-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ccfc-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9ccfc-164">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ccfc-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ccfc-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ccfc-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ccfc-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ccfc-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9ccfc-167">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ccfc-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ccfc-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ccfc-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ccfc-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9ccfc-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ccfc-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ccfc-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ccfc-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ccfc-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ccfc-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9ccfc-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="9ccfc-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9ccfc-175">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="9ccfc-176">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="9ccfc-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="9ccfc-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="9ccfc-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





