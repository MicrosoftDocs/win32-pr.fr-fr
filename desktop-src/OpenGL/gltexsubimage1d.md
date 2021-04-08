---
title: fonction glTexSubImage1D (GL. h)
description: La fonction glTexSubImage1D spécifie une partie d’une image de texture unidimensionnelle existante. Vous ne pouvez pas définir une nouvelle texture avec glTexSubImage1D.
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- glTexSubImage1D fonction OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe5510221b738a81f428f9e982a2f9bb2c23588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740636"
---
# <a name="gltexsubimage1d-function"></a><span data-ttu-id="12733-105">glTexSubImage1D fonction)</span><span class="sxs-lookup"><span data-stu-id="12733-105">glTexSubImage1D function</span></span>

<span data-ttu-id="12733-106">La fonction **glTexSubImage1D** spécifie une partie d’une image de texture unidimensionnelle existante.</span><span class="sxs-lookup"><span data-stu-id="12733-106">The **glTexSubImage1D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="12733-107">Vous ne pouvez pas définir une nouvelle texture avec **glTexSubImage1D**.</span><span class="sxs-lookup"><span data-stu-id="12733-107">You cannot define a new texture with **glTexSubImage1D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="12733-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12733-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="12733-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12733-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12733-110">*cible*</span><span class="sxs-lookup"><span data-stu-id="12733-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-111">Texture cible.</span><span class="sxs-lookup"><span data-stu-id="12733-111">The target texture.</span></span> <span data-ttu-id="12733-112">Doit être une \_ texture GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="12733-112">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="12733-113">*level*</span><span class="sxs-lookup"><span data-stu-id="12733-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-114">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="12733-114">The level-of-detail number.</span></span> <span data-ttu-id="12733-115">Le niveau 0 est l’image de base.</span><span class="sxs-lookup"><span data-stu-id="12733-115">Level 0 is the base image.</span></span> <span data-ttu-id="12733-116">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="12733-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="12733-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="12733-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-118">Décalage de Texel dans la direction *x* dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="12733-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="12733-119">*width*</span><span class="sxs-lookup"><span data-stu-id="12733-119">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-120">Largeur de la sous-image de texture.</span><span class="sxs-lookup"><span data-stu-id="12733-120">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="12733-121">*format*</span><span class="sxs-lookup"><span data-stu-id="12733-121">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-122">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="12733-122">The format of the pixel data.</span></span> <span data-ttu-id="12733-123">Ce paramètre peut prendre l’une des valeurs symboliques suivantes.</span><span class="sxs-lookup"><span data-stu-id="12733-123">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="12733-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="12733-124">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="12733-125">Signification</span><span class="sxs-lookup"><span data-stu-id="12733-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="12733-126"><dt>**\_index de couleur GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-126"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="12733-127">Chaque élément est une valeur unique, un index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="12733-127">Each element is a single value, a color index.</span></span> <span data-ttu-id="12733-128">Elle est convertie au format à virgule fixe (avec un nombre non spécifié de 0 bits à droite du point binaire), décalée vers la gauche ou vers la droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajoutée au décalage de l' \_ index GL \_ (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="12733-128">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="12733-129">L’index résultant est converti en un ensemble de composants de couleur à l’aide de la \_ carte de pixels GL \_ \_ i \_ à \_ R, de \_ \_ cartes de pixels GL \_ i \_ à \_ G, de mappage de \_ Pixel GL \_ \_ i \_ à \_ B et de carte de \_ pixels GL \_ \_ i \_ en \_ tables, et fixé à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="12733-129">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="12733-130"><dt>**GL \_ rouge**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-130"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="12733-131">Chaque élément est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="12733-131">Each element is a single red component.</span></span> <span data-ttu-id="12733-132">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le vert et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="12733-132">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="12733-133">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="12733-133">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="12733-134"><dt>**\_vert GL**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-134"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="12733-135">Chaque élément est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="12733-135">Each element is a single green component.</span></span> <span data-ttu-id="12733-136">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="12733-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="12733-137">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="12733-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="12733-138"><dt>**\_bleu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-138"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="12733-139">Chaque élément est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="12733-139">Each element is a single blue component.</span></span> <span data-ttu-id="12733-140">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge et le vert, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="12733-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="12733-141">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="12733-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="12733-142"><dt>**GL \_ alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-142"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="12733-143">Chaque élément est un composant alpha unique.</span><span class="sxs-lookup"><span data-stu-id="12733-143">Each element is a single alpha component.</span></span> <span data-ttu-id="12733-144">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="12733-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="12733-145">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="12733-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="12733-146"><dt>**\_RGB GL**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-146"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="12733-147">Chaque élément est un triple RVB.</span><span class="sxs-lookup"><span data-stu-id="12733-147">Each element is an RGB triple.</span></span> <span data-ttu-id="12733-148">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="12733-148">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="12733-149">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="12733-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="12733-150"><dt>**GL \_ RVBA**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-150"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="12733-151">Chaque élément est un élément RVBA complet.</span><span class="sxs-lookup"><span data-stu-id="12733-151">Each element is a complete RGBA element.</span></span> <span data-ttu-id="12733-152">Elle est convertie au format à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="12733-152">It is converted to floating point format.</span></span> <span data-ttu-id="12733-153">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="12733-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="12733-154"><dt>**LUMINANCE du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-154"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="12733-155">Chaque élément est une valeur de luminance unique.</span><span class="sxs-lookup"><span data-stu-id="12733-155">Each element is a single luminance value.</span></span> <span data-ttu-id="12733-156">Elle est convertie au format à virgule flottante, puis Assemblée dans un élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu, et en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="12733-156">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="12733-157">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="12733-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="12733-158"><dt>**\_luminance \_ alpha du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-158"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="12733-159">Chaque élément est une paire luminance/alpha.</span><span class="sxs-lookup"><span data-stu-id="12733-159">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="12733-160">Il est converti au format à virgule flottante, puis assemblé en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="12733-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="12733-161">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="12733-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="12733-162">*type*</span><span class="sxs-lookup"><span data-stu-id="12733-162">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-163">Type de données des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="12733-163">The data type of the pixel data.</span></span> <span data-ttu-id="12733-164">Les valeurs symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="12733-164">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="12733-165">*pixels*</span><span class="sxs-lookup"><span data-stu-id="12733-165">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="12733-166">Pointeur vers les données de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="12733-166">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12733-167">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12733-167">Return value</span></span>

<span data-ttu-id="12733-168">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="12733-168">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="12733-169">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="12733-169">Error codes</span></span>

<span data-ttu-id="12733-170">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="12733-170">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="12733-171">Nom</span><span class="sxs-lookup"><span data-stu-id="12733-171">Name</span></span>                                                                                                  | <span data-ttu-id="12733-172">Signification</span><span class="sxs-lookup"><span data-stu-id="12733-172">Meaning</span></span>                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12733-173"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-173"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="12733-174">la *cible* n’était pas la texture de la comptabilité \_ \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="12733-174">*target* was not GL\_TEXTURE\_1D.</span></span><br/>                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="12733-175"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-175"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="12733-176">le *format* n’est pas une constante acceptée.</span><span class="sxs-lookup"><span data-stu-id="12733-176">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="12733-177"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="12733-178">le *type* n’est pas une constante acceptée.</span><span class="sxs-lookup"><span data-stu-id="12733-178">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="12733-179"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="12733-180">le *type* était \_ bitmap GL et le *format* n’était pas l’index de \_ couleur GL \_ .</span><span class="sxs-lookup"><span data-stu-id="12733-180">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="12733-181"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-181"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="12733-182">le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* était la valeur retournée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="12733-182">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="12733-183"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-183"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="12733-184">*xoffset* était inférieur à *b*, ou   +  la *largeur* de décalage était supérieure à *WB*, où *w* correspond à la \_ largeur de la texture GL \_ , et *b* à la largeur de la bordure de la \_ texture GL \_ de l’image de texture en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="12733-184">*xoffset* was less than *b*, or *offset* + *width* was greater than *wb*, where *w* is the GL\_TEXTURE\_WIDTH, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span><br/> <span data-ttu-id="12733-185">Notez que *w* comprend deux fois la largeur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="12733-185">Note that *w* includes twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="12733-186"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-186"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="12733-187">la *largeur* était inférieure à *b*, où *b* est la largeur de bordure du tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="12733-187">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="12733-188"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-188"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="12733-189">la *bordure* n’était pas égale à zéro ou 1.</span><span class="sxs-lookup"><span data-stu-id="12733-189">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="12733-190"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-190"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="12733-191">Le tableau texure n’a pas été défini par une opération **glTexImage1D** précédente.</span><span class="sxs-lookup"><span data-stu-id="12733-191">The texure array was not defined by a previous **glTexImage1D** operation.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="12733-192"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12733-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="12733-193">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="12733-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="12733-194">Notes</span><span class="sxs-lookup"><span data-stu-id="12733-194">Remarks</span></span>

<span data-ttu-id="12733-195">Une texture unidimensionnelle pour une primitive est activée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="12733-195">One-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_1D.</span></span> <span data-ttu-id="12733-196">Pendant la texturation, une partie d’une image de texture spécifiée est mappée à chaque primitive activée.</span><span class="sxs-lookup"><span data-stu-id="12733-196">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="12733-197">Vous utilisez la fonction **glTexSubImage1D** pour spécifier une sous-image contiguë d’une image de texture unidimensionnelle existante pour la texturation.</span><span class="sxs-lookup"><span data-stu-id="12733-197">You use the **glTexSubImage1D** function to specify a contiguous sub-image of an existing one-dimensional texture image for texturing.</span></span>

<span data-ttu-id="12733-198">Les texels référencés par les *pixels* remplacent une région du tableau de texture existant par des index *x* de *xoffset* et *xoffset* + (*largeur* 1) inclus.</span><span class="sxs-lookup"><span data-stu-id="12733-198">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive.</span></span> <span data-ttu-id="12733-199">Cette région ne peut pas inclure de texels en dehors de la plage du tableau de texture spécifié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="12733-199">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="12733-200">La spécification d’une sous-image avec une *largeur* de zéro n’a aucun effet et ne génère pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="12733-200">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="12733-201">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="12733-201">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="12733-202">En général, les images de texture peuvent être représentées par les mêmes formats de données que les pixels d’une commande [**glDrawPixels**](gldrawpixels.md) , à ceci près que le \_ \_ composant index de stencils GL et \_ profondeur GL \_ ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="12733-202">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="12733-203">Les modes [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="12733-203">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="12733-204">Les fonctions suivantes récupèrent les informations relatives à **glTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="12733-204">The following functions retrieve information related to **glTexSubImage1D**:</span></span>

[<span data-ttu-id="12733-205">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="12733-205">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="12733-206">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="12733-206">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="12733-207">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12733-207">Requirements</span></span>



| <span data-ttu-id="12733-208">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12733-208">Requirement</span></span> | <span data-ttu-id="12733-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="12733-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12733-210">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12733-210">Minimum supported client</span></span><br/> | <span data-ttu-id="12733-211">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12733-211">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="12733-212">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12733-212">Minimum supported server</span></span><br/> | <span data-ttu-id="12733-213">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12733-213">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12733-214">En-tête</span><span class="sxs-lookup"><span data-stu-id="12733-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="12733-215"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="12733-215"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="12733-216">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12733-216">Library</span></span><br/>                  | <dl> <span data-ttu-id="12733-217"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12733-217"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="12733-218">DLL</span><span class="sxs-lookup"><span data-stu-id="12733-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12733-219"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12733-219"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12733-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12733-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12733-221">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="12733-221">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="12733-222">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="12733-222">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="12733-223">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="12733-223">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="12733-224">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="12733-224">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="12733-225">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="12733-225">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="12733-226">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="12733-226">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="12733-227">**glFog**</span><span class="sxs-lookup"><span data-stu-id="12733-227">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="12733-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="12733-228">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="12733-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12733-229">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="12733-230">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="12733-230">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="12733-231">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="12733-231">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="12733-232">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="12733-232">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="12733-233">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="12733-233">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="12733-234">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="12733-234">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="12733-235">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="12733-235">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="12733-236">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="12733-236">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="12733-237">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="12733-237">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





