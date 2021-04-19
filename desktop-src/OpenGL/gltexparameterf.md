---
title: fonction glTexParameterf (GL. h)
description: Définit les paramètres de texture. | fonction glTexParameterf (GL. h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- glTexParameterf fonction OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f749513757ee32f6fe468dadbe968b8657a06f3d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522917"
---
# <a name="gltexparameterf-function"></a><span data-ttu-id="9d069-105">glTexParameterf fonction)</span><span class="sxs-lookup"><span data-stu-id="9d069-105">glTexParameterf function</span></span>

<span data-ttu-id="9d069-106">Définit les paramètres de texture.</span><span class="sxs-lookup"><span data-stu-id="9d069-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d069-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d069-107">Syntax</span></span>


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="9d069-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d069-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="9d069-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="9d069-110">Texture cible, qui doit être une texture GL \_ \_ 1D ou une \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="9d069-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="9d069-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="9d069-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="9d069-112">Nom symbolique d’un paramètre de texture à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="9d069-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="9d069-113">Les symboles suivants sont acceptés dans *pname*.</span><span class="sxs-lookup"><span data-stu-id="9d069-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="9d069-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d069-114">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="9d069-115">Signification</span><span class="sxs-lookup"><span data-stu-id="9d069-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="9d069-116"><dt>**filtre de la \_ texture GL \_ min. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="9d069-117">La fonction minimisation de la texture est utilisée chaque fois que le pixel qui est texturé est mappé à une zone supérieure à un élément de texture.</span><span class="sxs-lookup"><span data-stu-id="9d069-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="9d069-118">Il existe six fonctions minimisation définies.</span><span class="sxs-lookup"><span data-stu-id="9d069-118">There are six defined minifying functions.</span></span> <span data-ttu-id="9d069-119">Deux d’entre eux utilisent l’un des quatre éléments de texture les plus proches pour calculer la valeur de la texture.</span><span class="sxs-lookup"><span data-stu-id="9d069-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="9d069-120">Les quatre autres utilisent des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="9d069-120">The other four use mipmaps.</span></span><br/> <span data-ttu-id="9d069-121">Un mipmap est un ensemble ordonné de tableaux représentant la même image à des résolutions progressivement inférieures.</span><span class="sxs-lookup"><span data-stu-id="9d069-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="9d069-122">Si la texture contient des dimensions 2nx2<sup>m</sup> , il y a Max (n, m) + 1 des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="9d069-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="9d069-123">Le premier mipmap est la texture d’origine, avec les dimensions 2nx2<sup>m</sup>.</span><span class="sxs-lookup"><span data-stu-id="9d069-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="9d069-124">Chaque mipmap suivant a des dimensions 2<sup>k</sup>1x2<sup>l</sup>1 où 2<sup>k</sup>x2<sup>l</sup> sont les dimensions du mipmap précédent, jusqu’à k = 0 ou l = 0.</span><span class="sxs-lookup"><span data-stu-id="9d069-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="9d069-125">À ce stade, les des mipmaps suivantes comportent la dimension 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 jusqu’au mipmap final, qui a une dimension 1x1.</span><span class="sxs-lookup"><span data-stu-id="9d069-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="9d069-126">Les des mipmaps sont définis à l’aide de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) avec l’argument de niveau de détail qui indique l’ordre des des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="9d069-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="9d069-127">Le niveau 0 est la texture d’origine. le niveau gras Max (n, m) est le mipmap de la dernière version 1x1.</span><span class="sxs-lookup"><span data-stu-id="9d069-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="9d069-128"><dt>**filtre de la \_ texture GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="9d069-129">La fonction d’agrandissement de la texture est utilisée lorsque le pixel en cours de texture est mappé à une zone inférieure ou égale à un élément de texture.</span><span class="sxs-lookup"><span data-stu-id="9d069-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="9d069-130">Elle définit la fonction d’agrandissement de la texture sur la valeur GL la \_ plus proche ou le GL \_ linéaire.</span><span class="sxs-lookup"><span data-stu-id="9d069-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="9d069-131"><dt>**\_ \_ encapsuler la texture GL \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>             | <span data-ttu-id="9d069-132">Définit le paramètre de retour à la ligne pour les coordonnées de la texture sur GL \_ clamp ou GL \_ REPEAT.</span><span class="sxs-lookup"><span data-stu-id="9d069-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="9d069-133">\_La fixation du GL fait que les coordonnées s sont ancrées à la plage \[ 0, 1 \] et est utile pour empêcher l’encapsulation des artefacts lors du mappage d’une image unique sur un objet.</span><span class="sxs-lookup"><span data-stu-id="9d069-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="9d069-134">\_La répétition du GL provoque l’ignorance de la partie entière de la coordonnée s. OpenGL utilise uniquement la partie fractionnaire, créant ainsi un modèle répétitif.</span><span class="sxs-lookup"><span data-stu-id="9d069-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="9d069-135">Les éléments de texture de bordure sont accessibles uniquement si l’habillage est défini sur la \_ fixation GL.</span><span class="sxs-lookup"><span data-stu-id="9d069-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="9d069-136">Au départ, \_ \_ la \_ valeur S de la texture GL est définie sur la répétition du GL \_ .</span><span class="sxs-lookup"><span data-stu-id="9d069-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="9d069-137"><dt>**\_enveloppe de \_ la texture GL \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>             | <span data-ttu-id="9d069-138">Définit le paramètre de retour à la ligne pour la coordonnée de texture sur GL \_ clamp ou GL \_ REPEAT.</span><span class="sxs-lookup"><span data-stu-id="9d069-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="9d069-139">Consultez la discussion sous les \_ enveloppes de la texture GL \_ \_ S.</span><span class="sxs-lookup"><span data-stu-id="9d069-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="9d069-140">Initialement, \_ la texture \_ GL \_ T Wrap T est définie sur GL \_ REPEAT</span><span class="sxs-lookup"><span data-stu-id="9d069-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="9d069-141">*param*</span><span class="sxs-lookup"><span data-stu-id="9d069-141">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="9d069-142">Valeur de *pname*.</span><span class="sxs-lookup"><span data-stu-id="9d069-142">The value of *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d069-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d069-143">Return value</span></span>

<span data-ttu-id="9d069-144">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9d069-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d069-145">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9d069-145">Error codes</span></span>

<span data-ttu-id="9d069-146">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9d069-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9d069-147">Nom</span><span class="sxs-lookup"><span data-stu-id="9d069-147">Name</span></span>                                                                                                  | <span data-ttu-id="9d069-148">Signification</span><span class="sxs-lookup"><span data-stu-id="9d069-148">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d069-149"><dt>**GL \_ \_énumération non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-149"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="9d069-150">*target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque *param* aurait dû avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.</span><span class="sxs-lookup"><span data-stu-id="9d069-150">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="9d069-151"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9d069-152">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9d069-152">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="9d069-153">Notes</span><span class="sxs-lookup"><span data-stu-id="9d069-153">Remarks</span></span>

<span data-ttu-id="9d069-154">Le mappage de texture est une technique qui applique une image sur la surface d’un objet comme si l’image était un cellophane de décalque ou de réduction.</span><span class="sxs-lookup"><span data-stu-id="9d069-154">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="9d069-155">L’image est créée dans l’espace de texture, avec un système de coordonnées (*s*, *t*).</span><span class="sxs-lookup"><span data-stu-id="9d069-155">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="9d069-156">Une texture est une image à une ou deux dimensions et un ensemble de paramètres qui déterminent la façon dont les échantillons sont dérivés de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d069-156">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="9d069-157">La fonction **glTexParameter** assigne la ou les valeurs dans les paramètres au paramètre de texture spécifié comme pname.</span><span class="sxs-lookup"><span data-stu-id="9d069-157">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="9d069-158">Le paramètre Target définit la texture cible, à savoir la texture GL \_ \_ 1D ou la \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="9d069-158">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="9d069-159">À mesure que d’autres éléments de texture sont échantillonnés dans le processus de minimisation, le nombre d’artefacts d’alias est apparent.</span><span class="sxs-lookup"><span data-stu-id="9d069-159">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="9d069-160">Alors que les \_ fonctions de minimisation linéaires GL les plus proches et les plus proches \_ peuvent être plus rapides que les quatre autres, elles n’échantillonnent qu’un ou quatre éléments de texture pour déterminer la valeur de texture du pixel rendu et peuvent produire des modèles moire ou des transitions irrégulières.</span><span class="sxs-lookup"><span data-stu-id="9d069-160">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="9d069-161">La valeur par défaut du \_ filtre de la texture GL \_ min est le \_ \_ MIPMAP linéaire le plus proche \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9d069-161">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="9d069-162">Supposons que la texturation est activée (en appelant [**glEnable**](glenable.md) avec \_ l’argument la texture GL \_ 1D ou la \_ texture GL \_ 2d) et \_ \_ \_ le filtre de la texture GL min est défini sur l’une des fonctions qui requièrent un mipmap.</span><span class="sxs-lookup"><span data-stu-id="9d069-162">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="9d069-163">Si les dimensions des images de texture actuellement définies (avec des appels précédents à [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md)) ne suivent pas la séquence appropriée pour des mipmaps, ou si moins d’images de texture sont définies que nécessaire, ou si le jeu d’images de texture a des nombres différents de composants de texture, c’est comme si le mappage de texture était désactivé.</span><span class="sxs-lookup"><span data-stu-id="9d069-163">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="9d069-164">Le filtrage linéaire accède aux quatre éléments de texture les plus proches uniquement dans les textures 2D.</span><span class="sxs-lookup"><span data-stu-id="9d069-164">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="9d069-165">Dans les textures 1D, le filtrage linéaire accède aux deux éléments de texture les plus proches.</span><span class="sxs-lookup"><span data-stu-id="9d069-165">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="9d069-166">La fonction suivante récupère des informations relatives à **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** et **glTexParameteriv**.</span><span class="sxs-lookup"><span data-stu-id="9d069-166">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d069-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d069-167">Requirements</span></span>



| <span data-ttu-id="9d069-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d069-168">Requirement</span></span> | <span data-ttu-id="9d069-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d069-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d069-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d069-170">Minimum supported client</span></span><br/> | <span data-ttu-id="9d069-171">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d069-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d069-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d069-172">Minimum supported server</span></span><br/> | <span data-ttu-id="9d069-173">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d069-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d069-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d069-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d069-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9d069-176">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d069-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d069-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d069-178">DLL</span><span class="sxs-lookup"><span data-stu-id="9d069-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d069-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d069-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d069-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d069-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d069-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9d069-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9d069-182">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="9d069-182">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="9d069-183">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="9d069-183">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="9d069-184">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="9d069-184">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="9d069-185">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="9d069-185">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="9d069-186">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="9d069-186">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="9d069-187">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="9d069-187">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="9d069-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9d069-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9d069-189">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="9d069-189">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="9d069-190">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="9d069-190">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="9d069-191">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="9d069-191">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="9d069-192">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="9d069-192">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="9d069-193">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="9d069-193">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="9d069-194">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="9d069-194">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="9d069-195">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="9d069-195">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="9d069-196">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="9d069-196">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="9d069-197">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="9d069-197">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="9d069-198">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="9d069-198">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





