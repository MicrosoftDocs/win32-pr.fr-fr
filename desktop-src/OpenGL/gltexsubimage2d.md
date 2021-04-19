---
title: fonction glTexSubImage2D (GL. h)
description: La fonction glTexSubImage2D spécifie une partie d’une image de texture unidimensionnelle existante. Vous ne pouvez pas définir une nouvelle texture avec glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- glTexSubImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510727"
---
# <a name="gltexsubimage2d-function"></a><span data-ttu-id="5f811-105">glTexSubImage2D fonction)</span><span class="sxs-lookup"><span data-stu-id="5f811-105">glTexSubImage2D function</span></span>

<span data-ttu-id="5f811-106">La fonction **glTexSubImage2D** spécifie une partie d’une image de texture unidimensionnelle existante.</span><span class="sxs-lookup"><span data-stu-id="5f811-106">The **glTexSubImage2D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="5f811-107">Vous ne pouvez pas définir une nouvelle texture avec **glTexSubImage2D**.</span><span class="sxs-lookup"><span data-stu-id="5f811-107">You cannot define a new texture with **glTexSubImage2D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f811-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f811-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="5f811-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f811-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f811-110">*cible*</span><span class="sxs-lookup"><span data-stu-id="5f811-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-111">Texture cible.</span><span class="sxs-lookup"><span data-stu-id="5f811-111">The target texture.</span></span> <span data-ttu-id="5f811-112">Doit être une \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5f811-112">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-113">*level*</span><span class="sxs-lookup"><span data-stu-id="5f811-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-114">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="5f811-114">The level-of-detail number.</span></span> <span data-ttu-id="5f811-115">Le niveau 0 est l’image de base.</span><span class="sxs-lookup"><span data-stu-id="5f811-115">Level 0 is the base image.</span></span> <span data-ttu-id="5f811-116">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="5f811-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="5f811-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-118">Décalage de Texel dans la direction *x* dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="5f811-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-119">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="5f811-119">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-120">Décalage de Texel dans l’axe *y* dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="5f811-120">A texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-121">*width*</span><span class="sxs-lookup"><span data-stu-id="5f811-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-122">Largeur de la sous-image de texture.</span><span class="sxs-lookup"><span data-stu-id="5f811-122">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-123">*height*</span><span class="sxs-lookup"><span data-stu-id="5f811-123">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-124">Hauteur de la sous-image de texture.</span><span class="sxs-lookup"><span data-stu-id="5f811-124">The height of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-125">*format*</span><span class="sxs-lookup"><span data-stu-id="5f811-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-126">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="5f811-126">The format of the pixel data.</span></span> <span data-ttu-id="5f811-127">Elle peut prendre l’une des valeurs symboliques suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f811-127">It can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="5f811-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f811-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="5f811-129">Signification</span><span class="sxs-lookup"><span data-stu-id="5f811-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="5f811-130"><dt>**\_index de couleur GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="5f811-131">Chaque élément est une valeur unique, un index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="5f811-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="5f811-132">Elle est convertie au format à virgule fixe (avec un nombre non spécifié de 0 bits à droite du point binaire), décalée vers la gauche ou vers la droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajoutée au décalage de l' \_ index GL \_ (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="5f811-132">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="5f811-133">L’index résultant est converti en un ensemble de composants de couleur à l’aide de la \_ carte de pixels GL \_ \_ i \_ à \_ R, de \_ \_ cartes de pixels GL \_ i \_ à \_ G, de mappage de \_ Pixel GL \_ \_ i \_ à \_ B et de carte de \_ pixels GL \_ \_ i \_ en \_ tables, et fixé à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5f811-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="5f811-134"><dt>**GL \_ rouge**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="5f811-135">Chaque élément est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="5f811-135">Each element is a single red component.</span></span> <span data-ttu-id="5f811-136">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le vert et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="5f811-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="5f811-137">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="5f811-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="5f811-138"><dt>**\_vert GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="5f811-139">Chaque élément est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="5f811-139">Each element is a single green component.</span></span> <span data-ttu-id="5f811-140">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="5f811-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="5f811-141">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="5f811-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="5f811-142"><dt>**\_bleu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="5f811-143">Chaque élément est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="5f811-143">Each element is a single blue component.</span></span> <span data-ttu-id="5f811-144">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge et le vert, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="5f811-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="5f811-145">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="5f811-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="5f811-146"><dt>**GL \_ alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="5f811-147">Chaque élément est un composant alpha unique.</span><span class="sxs-lookup"><span data-stu-id="5f811-147">Each element is a single alpha component.</span></span> <span data-ttu-id="5f811-148">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="5f811-148">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="5f811-149">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="5f811-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="5f811-150"><dt>**\_RGB GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="5f811-151">Chaque élément est un triple RVB.</span><span class="sxs-lookup"><span data-stu-id="5f811-151">Each element is an RGB triple.</span></span> <span data-ttu-id="5f811-152">Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="5f811-152">It is converted to floating point format and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="5f811-153">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="5f811-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="5f811-154"><dt>**GL \_ RVBA**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="5f811-155">Chaque élément est un élément RVBA complet.</span><span class="sxs-lookup"><span data-stu-id="5f811-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="5f811-156">Elle est convertie en virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f811-156">It is converted to floating point.</span></span> <span data-ttu-id="5f811-157">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="5f811-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="5f811-158"><dt>**LUMINANCE du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-158"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="5f811-159">Chaque élément est une valeur de luminance unique.</span><span class="sxs-lookup"><span data-stu-id="5f811-159">Each element is a single luminance value.</span></span> <span data-ttu-id="5f811-160">Elle est convertie au format à virgule flottante, puis Assemblée dans un élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu, et en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="5f811-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="5f811-161">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="5f811-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="5f811-162"><dt>**\_luminance \_ alpha du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-162"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="5f811-163">Chaque élément est une paire luminance/alpha.</span><span class="sxs-lookup"><span data-stu-id="5f811-163">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="5f811-164">Il est converti au format à virgule flottante, puis assemblé en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="5f811-164">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="5f811-165">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="5f811-165">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="5f811-166">*type*</span><span class="sxs-lookup"><span data-stu-id="5f811-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-167">Type de données des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="5f811-167">The data type of the pixel data.</span></span> <span data-ttu-id="5f811-168">Les valeurs symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="5f811-168">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="5f811-169">*pixels*</span><span class="sxs-lookup"><span data-stu-id="5f811-169">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="5f811-170">Pointeur vers les données de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="5f811-170">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f811-171">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5f811-171">Return value</span></span>

<span data-ttu-id="5f811-172">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5f811-172">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f811-173">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5f811-173">Error codes</span></span>

<span data-ttu-id="5f811-174">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5f811-174">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5f811-175">Nom</span><span class="sxs-lookup"><span data-stu-id="5f811-175">Name</span></span>                                                                                                  | <span data-ttu-id="5f811-176">Signification</span><span class="sxs-lookup"><span data-stu-id="5f811-176">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f811-177"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5f811-178">la *cible* n’était pas la \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5f811-178">*target* was not GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5f811-179"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5f811-180">le *format* n’est pas une constante acceptée.</span><span class="sxs-lookup"><span data-stu-id="5f811-180">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="5f811-181"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-181"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5f811-182">le *type* n’est pas une constante acceptée.</span><span class="sxs-lookup"><span data-stu-id="5f811-182">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="5f811-183"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-183"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5f811-184">le *type* était \_ bitmap GL et le *format* n’était pas l’index de \_ couleur GL \_ .</span><span class="sxs-lookup"><span data-stu-id="5f811-184">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="5f811-185"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-185"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5f811-186">le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* était la valeur retournée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5f811-186">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="5f811-187"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-187"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5f811-188">*xoffset* était inférieur à-*b*; ou la largeur de *xoffset*  +   était supérieure à *w*  -  *b*; ou *YOFFSET* était inférieur à-*b*; ou *YOFFSET*  +  *hauteur* était supérieure à *h*  -  *b*, où *w* est la largeur de la \_ texture GL \_ , *h* est la \_ hauteur de la texture GL \_ et *b* est la largeur de la bordure de \_ texture GL \_ de l’image de texture en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="5f811-188">*xoffset* was less than -*b*; or *xoffset* + *width* was greater than *w* - *b*; or *yoffset* was less than -*b*; or *yoffset* + *height* was greater than *h* - *b*, where *w* is the GL\_TEXTURE\_WIDTH, *h* is the GL\_TEXTURE\_HEIGHT, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span> <br/> <span data-ttu-id="5f811-189">Notez que *w* et *h* incluent deux fois la largeur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="5f811-189">Note that *w* and *h* include twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="5f811-190"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5f811-191">la *largeur* était inférieure à *b*, où *b* est la largeur de bordure du tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="5f811-191">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="5f811-192"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-192"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5f811-193">la *bordure* n’était pas égale à zéro ou 1.</span><span class="sxs-lookup"><span data-stu-id="5f811-193">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5f811-194"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5f811-195">Le tableau de texture n’a pas été défini par une opération **glTexImage2D** précédente.</span><span class="sxs-lookup"><span data-stu-id="5f811-195">The texture array was not defined by a previous **glTexImage2D** operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5f811-196"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5f811-197">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5f811-197">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="5f811-198">Notes</span><span class="sxs-lookup"><span data-stu-id="5f811-198">Remarks</span></span>

<span data-ttu-id="5f811-199">La texturation à deux dimensions pour une primitive est activée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5f811-199">Two-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_2D.</span></span> <span data-ttu-id="5f811-200">Pendant la texturation, une partie d’une image de texture spécifiée est mappée à chaque primitive activée.</span><span class="sxs-lookup"><span data-stu-id="5f811-200">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="5f811-201">Vous utilisez la fonction **glTexSubImage2D** pour spécifier une sous-image contiguë d’une image de texture à deux dimensions existante pour la texturation.</span><span class="sxs-lookup"><span data-stu-id="5f811-201">You use the **glTexSubImage2D** function to specify a contiguous sub-image of an existing two-dimensional texture image for texturing.</span></span>

<span data-ttu-id="5f811-202">Les texels référencés par les *pixels* remplacent une région du tableau de texture existant par des index *x* de *xoffset* et *xoffset* + (*Width* 1) inclusifs et des index *y* de *YOFFSET* et *YOFFSET* + (*hauteur* 1).</span><span class="sxs-lookup"><span data-stu-id="5f811-202">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive and *y* indexes of *yoffset* and *yoffset* + (*height* 1) inclusive.</span></span> <span data-ttu-id="5f811-203">Cette région ne peut pas inclure de texels en dehors de la plage du tableau de texture spécifié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="5f811-203">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="5f811-204">La spécification d’une sous-image avec une *largeur* de zéro n’a aucun effet et ne génère pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5f811-204">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="5f811-205">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="5f811-205">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="5f811-206">En général, les images de texture peuvent être représentées par les mêmes formats de données que les pixels d’une commande [**glDrawPixels**](gldrawpixels.md) , à ceci près que le \_ \_ composant index de stencils GL et \_ profondeur GL \_ ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5f811-206">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="5f811-207">Les modes [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="5f811-207">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="5f811-208">Les fonctions suivantes récupèrent les informations relatives à **glTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="5f811-208">The following functions retrieve information related to **glTexSubImage2D**:</span></span>

[<span data-ttu-id="5f811-209">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="5f811-209">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="5f811-210">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="5f811-210">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="5f811-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f811-211">Requirements</span></span>



| <span data-ttu-id="5f811-212">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f811-212">Requirement</span></span> | <span data-ttu-id="5f811-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f811-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f811-214">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f811-214">Minimum supported client</span></span><br/> | <span data-ttu-id="5f811-215">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f811-215">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f811-216">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f811-216">Minimum supported server</span></span><br/> | <span data-ttu-id="5f811-217">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f811-217">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f811-218">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f811-218">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f811-219"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-219"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5f811-220">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f811-220">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f811-221"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-221"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f811-222">DLL</span><span class="sxs-lookup"><span data-stu-id="5f811-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f811-223"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f811-223"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f811-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f811-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f811-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="5f811-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="5f811-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="5f811-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="5f811-227">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="5f811-227">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="5f811-228">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="5f811-228">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="5f811-229">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="5f811-229">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="5f811-230">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="5f811-230">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="5f811-231">**glFog**</span><span class="sxs-lookup"><span data-stu-id="5f811-231">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="5f811-232">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="5f811-232">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="5f811-233">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5f811-233">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="5f811-234">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="5f811-234">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="5f811-235">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="5f811-235">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="5f811-236">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="5f811-236">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="5f811-237">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="5f811-237">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="5f811-238">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="5f811-238">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="5f811-239">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="5f811-239">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="5f811-240">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="5f811-240">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="5f811-241">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="5f811-241">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="5f811-242">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="5f811-242">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





