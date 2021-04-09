---
title: fonction glTexImage1D (GL. h)
description: La fonction glTexImage1D spécifie une image de texture unidimensionnelle.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- glTexImage1D fonction OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032729"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="35633-104">glTexImage1D fonction)</span><span class="sxs-lookup"><span data-stu-id="35633-104">glTexImage1D function</span></span>

<span data-ttu-id="35633-105">La fonction **glTexImage1D** spécifie une image de texture unidimensionnelle.</span><span class="sxs-lookup"><span data-stu-id="35633-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="35633-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35633-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="35633-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35633-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35633-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="35633-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-109">Texture cible.</span><span class="sxs-lookup"><span data-stu-id="35633-109">The target texture.</span></span> <span data-ttu-id="35633-110">Doit être une \_ texture GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="35633-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="35633-111">*level*</span><span class="sxs-lookup"><span data-stu-id="35633-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-112">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="35633-112">The level-of-detail number.</span></span> <span data-ttu-id="35633-113">Le niveau 0 est le niveau d’image de base.</span><span class="sxs-lookup"><span data-stu-id="35633-113">Level 0 is the base image level.</span></span> <span data-ttu-id="35633-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="35633-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="35633-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="35633-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-116">Spécifie le nombre de composants de couleur dans la texture.</span><span class="sxs-lookup"><span data-stu-id="35633-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="35633-117">Doit être 1, 2, 3 ou 4, ou l’une des constantes symboliques suivantes : GL \_ alpha, GL \_ alpha4, GL \_ ALPHA8, GL \_ ALPHA12, GL ALPHA16, luminance GL, GL LUMINANCE4, GL LUMINANCE8, GL LUMINANCE12, GL LUMINANCE16, GL luminance alpha, GL LUMINANCE4 alpha4, GL LUMINANCE6 alpha2 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ alpha4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ Intensity, GL \_ INTENSITY4, GL INTENSITY8, \_ GL INTENSITY12 \_ , GL \_ INTENSITY16, GL \_ RGB, GL R3 G3 a2, GL RGB4, GL RGB5, GL RGB8, GL RGB10, GL RGB12, GL RGB16, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ RVBA, GL \_ RGBA2, GL RGBA4 \_ , GL \_ RGB5 \_ a1, GL \_ RGBA8, GL \_ RGB10 \_ a2, GL \_ RGBA12 ou GL \_ RGBA16.</span><span class="sxs-lookup"><span data-stu-id="35633-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="35633-118">*width*</span><span class="sxs-lookup"><span data-stu-id="35633-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-119">Largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="35633-119">The width of the texture image.</span></span> <span data-ttu-id="35633-120">Doit être 2 *n* + 2 ( *Border* ) pour un entier *n*.</span><span class="sxs-lookup"><span data-stu-id="35633-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="35633-121">La hauteur de l’image de texture est 1.</span><span class="sxs-lookup"><span data-stu-id="35633-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="35633-122">*2S*</span><span class="sxs-lookup"><span data-stu-id="35633-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-123">Largeur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="35633-123">The width of the border.</span></span> <span data-ttu-id="35633-124">Doit être 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="35633-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="35633-125">*format*</span><span class="sxs-lookup"><span data-stu-id="35633-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-126">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="35633-126">The format of the pixel data.</span></span> <span data-ttu-id="35633-127">Elle peut prendre l’une des neuf valeurs symboliques.</span><span class="sxs-lookup"><span data-stu-id="35633-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="35633-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="35633-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="35633-129">Signification</span><span class="sxs-lookup"><span data-stu-id="35633-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="35633-130"><dt>**\_index de couleur GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="35633-131">Chaque élément est une valeur unique, un index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="35633-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="35633-132">Elle est convertie en virgule fixe (avec un nombre non spécifié de 0 bits à droite du point binaire), décalée vers la gauche ou vers la droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajoutée au décalage de l' \_ index GL \_ (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="35633-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="35633-133">L’index résultant est converti en un ensemble de composants de couleur à l’aide de la \_ carte de pixels GL \_ \_ i \_ à \_ R, de \_ \_ cartes de pixels GL \_ i \_ à \_ G, de mappage de \_ Pixel GL \_ \_ i \_ à \_ B et de carte de \_ pixels GL \_ \_ i \_ en \_ tables, et fixé à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="35633-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="35633-134"><dt>**GL \_ rouge**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="35633-135">Chaque élément est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="35633-135">Each element is a single red component.</span></span> <span data-ttu-id="35633-136">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le vert et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="35633-137">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="35633-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="35633-138"><dt>**\_vert GL**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="35633-139">Chaque élément est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="35633-139">Each element is a single green component.</span></span> <span data-ttu-id="35633-140">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="35633-141">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="35633-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="35633-142"><dt>**\_bleu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="35633-143">Chaque élément est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="35633-143">Each element is a single blue component.</span></span> <span data-ttu-id="35633-144">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge et le vert, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="35633-145">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="35633-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="35633-146"><dt>**GL \_ alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="35633-147">Chaque élément est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="35633-147">Each element is a single red component.</span></span> <span data-ttu-id="35633-148">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="35633-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="35633-149">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="35633-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="35633-150"><dt>**\_RGB GL**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="35633-151">Chaque élément est un triple RVB.</span><span class="sxs-lookup"><span data-stu-id="35633-151">Each element is an RGB triple.</span></span> <span data-ttu-id="35633-152">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="35633-153">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="35633-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="35633-154"><dt>**GL \_ RVBA**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="35633-155">Chaque élément est un élément RVBA complet.</span><span class="sxs-lookup"><span data-stu-id="35633-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="35633-156">Elle est convertie en virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="35633-156">It is converted to floating point.</span></span> <span data-ttu-id="35633-157">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="35633-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="35633-158"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="35633-159">Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.</span><span class="sxs-lookup"><span data-stu-id="35633-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="35633-160">GL \_ BGR \_ ext fournit un format qui correspond à la disposition de la mémoire des bitmaps indépendantes du périphérique (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="35633-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="35633-161">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="35633-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="35633-162"><dt>**GL \_ BGRA \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="35633-163">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="35633-164">GL \_ BGRA \_ ext fournit un format qui correspond à la disposition de la mémoire des bitmaps indépendantes du périphérique (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="35633-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="35633-165">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="35633-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="35633-166"><dt>**LUMINANCE du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="35633-167">Chaque élément est une valeur de luminance unique.</span><span class="sxs-lookup"><span data-stu-id="35633-167">Each element is a single luminance value.</span></span> <span data-ttu-id="35633-168">Elle est convertie en virgule flottante, puis Assemblée en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu, et en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="35633-169">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="35633-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="35633-170"><dt>**\_luminance \_ alpha du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="35633-171">Chaque élément est une paire luminance/alpha.</span><span class="sxs-lookup"><span data-stu-id="35633-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="35633-172">Elle est convertie en virgule flottante, puis Assemblée en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="35633-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="35633-173">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="35633-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="35633-174">*type*</span><span class="sxs-lookup"><span data-stu-id="35633-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-175">Type de données des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="35633-175">The data type of the pixel data.</span></span> <span data-ttu-id="35633-176">Les valeurs symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="35633-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="35633-177">*pixels*</span><span class="sxs-lookup"><span data-stu-id="35633-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="35633-178">Pointeur vers les données de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="35633-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35633-179">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35633-179">Return value</span></span>

<span data-ttu-id="35633-180">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35633-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35633-181">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="35633-181">Error codes</span></span>

<span data-ttu-id="35633-182">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="35633-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="35633-183">Nom</span><span class="sxs-lookup"><span data-stu-id="35633-183">Name</span></span>                                                                                                  | <span data-ttu-id="35633-184">Signification</span><span class="sxs-lookup"><span data-stu-id="35633-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35633-185"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="35633-186">la *cible* n’était pas une \_ texture GL.</span><span class="sxs-lookup"><span data-stu-id="35633-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="35633-187"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="35633-188">le *format* n’était pas une constante de *format* acceptée.</span><span class="sxs-lookup"><span data-stu-id="35633-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="35633-189">Seules les constantes de format autres que l' \_ index du stencil GL et le composant de \_ \_ profondeur GL \_ sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="35633-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="35633-190">Pour obtenir la liste des valeurs possibles, consultez la description du paramètre *format* .</span><span class="sxs-lookup"><span data-stu-id="35633-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="35633-191"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="35633-192">le *type* n’est pas une constante de *type* .</span><span class="sxs-lookup"><span data-stu-id="35633-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="35633-193"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="35633-194">le *type* était \_ bitmap GL et le *format* n’était pas l’index de \_ couleur GL \_ .</span><span class="sxs-lookup"><span data-stu-id="35633-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="35633-195"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="35633-196">le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* était la valeur retournée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35633-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="35633-197"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="35633-198">*internalformat* n’était pas 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="35633-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="35633-199"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="35633-200">la *largeur* était inférieure à zéro ou supérieure à 2 + \_ la \_ taille de texture GL maximum \_ , ou elle ne peut pas être représentée sous la forme 2 *n* + 2 (bordure) pour une valeur entière de *n*.</span><span class="sxs-lookup"><span data-stu-id="35633-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="35633-201"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="35633-202">la *bordure* n’est pas 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="35633-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="35633-203"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35633-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="35633-204">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="35633-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="35633-205">Notes</span><span class="sxs-lookup"><span data-stu-id="35633-205">Remarks</span></span>

<span data-ttu-id="35633-206">La fonction **glTexImage1D** spécifie une image de texture unidimensionnelle.</span><span class="sxs-lookup"><span data-stu-id="35633-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="35633-207">La texturation mappe une partie d’une *image de texture* spécifiée sur chaque primitive graphique pour laquelle la texturation est activée.</span><span class="sxs-lookup"><span data-stu-id="35633-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="35633-208">La texturation unidimensionnelle est activée et désactivée à l’aide de [**glEnable**](glenable.md) et **GLDISABLE** avec argument GL \_ texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="35633-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="35633-209">Les images de texture sont définies avec **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="35633-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="35633-210">Les arguments décrivent les paramètres de l’image de texture, tels que la largeur, la largeur de la bordure, le nombre de niveaux de détail (voir [**glTexParameter**](gltexparameter-functions.md)) et le nombre de composants de couleur fournis.</span><span class="sxs-lookup"><span data-stu-id="35633-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="35633-211">Les trois derniers arguments décrivent le mode de représentation de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="35633-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="35633-212">Ces arguments sont identiques aux formats de pixels utilisés pour [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="35633-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="35633-213">Les données sont lues à partir de *pixels* sous la forme d’une séquence d’octets signés ou non signés, de shorts ou de longs, ou de valeurs à virgule flottante simple précision, en fonction du *type*.</span><span class="sxs-lookup"><span data-stu-id="35633-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="35633-214">Ces valeurs sont regroupées en jeux d’une, deux, trois ou quatre valeurs, selon le *format*, pour former des éléments.</span><span class="sxs-lookup"><span data-stu-id="35633-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="35633-215">Si le *type* est \_ bitmap GL, les données sont considérées comme une chaîne d’octets non signés (et le *format* doit être un index de couleur GL \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="35633-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="35633-216">Chaque octet de données est traité comme des éléments 8 1 bits, l’ordonnancement des bits étant déterminé par le \_ décompression GL \_ LSB en \_ premier (voir [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="35633-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="35633-217">Une image de texture peut avoir jusqu’à quatre composants par élément de texture, en fonction des *composants*.</span><span class="sxs-lookup"><span data-stu-id="35633-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="35633-218">Une image de texture à un composant utilise uniquement le composant rouge de la couleur RVBA extraite des *pixels*.</span><span class="sxs-lookup"><span data-stu-id="35633-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="35633-219">Une image à deux composants utilise les valeurs R et A.</span><span class="sxs-lookup"><span data-stu-id="35633-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="35633-220">Une image à trois composants utilise les valeurs R, G et B.</span><span class="sxs-lookup"><span data-stu-id="35633-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="35633-221">Une image à quatre composants utilise tous les composants RVBA.</span><span class="sxs-lookup"><span data-stu-id="35633-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="35633-222">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="35633-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="35633-223">L’image de texture peut être représentée par les mêmes formats de données que les pixels d’une commande [**glDrawPixels**](gldrawpixels.md) , à ceci près que le \_ composant index du stencil GL \_ et profondeur du GL \_ \_ ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="35633-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="35633-224">Les modes [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="35633-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="35633-225">Une image de texture avec une largeur nulle indique la texture null.</span><span class="sxs-lookup"><span data-stu-id="35633-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="35633-226">Si la texture null est spécifiée pour le niveau de détail 0, c’est comme si la texturation était désactivée.</span><span class="sxs-lookup"><span data-stu-id="35633-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="35633-227">Les fonctions suivantes récupèrent les informations relatives à **glTexImageID**:</span><span class="sxs-lookup"><span data-stu-id="35633-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="35633-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="35633-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="35633-229">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="35633-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="35633-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35633-230">Requirements</span></span>



| <span data-ttu-id="35633-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35633-231">Requirement</span></span> | <span data-ttu-id="35633-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="35633-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35633-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35633-233">Minimum supported client</span></span><br/> | <span data-ttu-id="35633-234">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35633-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35633-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35633-235">Minimum supported server</span></span><br/> | <span data-ttu-id="35633-236">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35633-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35633-237">En-tête</span><span class="sxs-lookup"><span data-stu-id="35633-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="35633-238"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="35633-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="35633-239">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35633-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="35633-240"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35633-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35633-241">DLL</span><span class="sxs-lookup"><span data-stu-id="35633-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35633-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35633-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35633-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35633-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35633-244">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="35633-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="35633-245">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="35633-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="35633-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="35633-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="35633-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="35633-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="35633-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="35633-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="35633-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="35633-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="35633-250">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="35633-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="35633-251">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="35633-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="35633-252">**glFog**</span><span class="sxs-lookup"><span data-stu-id="35633-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="35633-253">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="35633-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="35633-254">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="35633-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="35633-255">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="35633-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="35633-256">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="35633-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="35633-257">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="35633-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="35633-258">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="35633-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="35633-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="35633-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="35633-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="35633-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="35633-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="35633-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="35633-262">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="35633-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





