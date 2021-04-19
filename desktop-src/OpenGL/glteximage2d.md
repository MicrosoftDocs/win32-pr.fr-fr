---
title: fonction glTexImage2D (GL. h)
description: La fonction glTexImage2D spécifie une image de texture à deux dimensions.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- glTexImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517335"
---
# <a name="glteximage2d-function"></a><span data-ttu-id="1c0a7-104">glTexImage2D fonction)</span><span class="sxs-lookup"><span data-stu-id="1c0a7-104">glTexImage2D function</span></span>

<span data-ttu-id="1c0a7-105">La fonction **glTexImage2D** spécifie une image de texture à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-105">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c0a7-106">Syntax</span></span>


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="1c0a7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c0a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c0a7-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-109">Texture cible.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-109">The target texture.</span></span> <span data-ttu-id="1c0a7-110">Doit être une \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-111">*level*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-112">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-112">The level-of-detail number.</span></span> <span data-ttu-id="1c0a7-113">Le niveau 0 est le niveau d’image de base.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-113">Level 0 is the base image level.</span></span> <span data-ttu-id="1c0a7-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-116">Nombre de composants de couleur dans la texture.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-116">The number of color components in the texture.</span></span> <span data-ttu-id="1c0a7-117">Doit être 1, 2, 3 ou 4, ou l’une des constantes symboliques suivantes : GL \_ alpha, GL \_ alpha4, GL \_ ALPHA8, GL \_ ALPHA12, GL ALPHA16, luminance GL, GL LUMINANCE4, GL LUMINANCE8, GL LUMINANCE12, GL LUMINANCE16, GL luminance alpha, GL LUMINANCE4 alpha4, GL LUMINANCE6 alpha2 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ alpha4, comptabilité GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL Intensity, GL INTENSITY4, GL INTENSITY8, GL INTENSITY12, GL INTENSITY16, GL R3 G3 B2, GL RGB, \_ GL RGB4 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , GL RGB5, GL RGB8, GL RGB10, GL RGB12, GL RGB16, grand livre, GL RGBA2, GL RGBA4, GL RGB5 a1, GL RGBA8, GL RGB10 a2, GL RGBA12 ou GL RGBA16.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_R3\_G3\_B2, GL\_RGB, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-118">*width*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-119">Largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-119">The width of the texture image.</span></span> <span data-ttu-id="1c0a7-120">Doit être 2 *n* + 2 (*Border*) pour un entier *n*.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-120">Must be 2 *n* + 2(*border*) for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-121">*height*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-121">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-122">Hauteur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-122">The height of the texture image.</span></span> <span data-ttu-id="1c0a7-123">Doit être 2 *<sup>m</sup>* + 2 (*bordure*) pour un entier *m*.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-123">Must be 2 *<sup>m</sup>* + 2(*border*) for some integer *m*.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-124">*2S*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-124">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-125">Largeur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-125">The width of the border.</span></span> <span data-ttu-id="1c0a7-126">Doit être 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-126">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-127">*format*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-127">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-128">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-128">The format of the pixel data.</span></span> <span data-ttu-id="1c0a7-129">Elle peut prendre l’une des neuf valeurs symboliques.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-129">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="1c0a7-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0a7-130">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="1c0a7-131">Signification</span><span class="sxs-lookup"><span data-stu-id="1c0a7-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="1c0a7-132"><dt>**\_index de couleur GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-132"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="1c0a7-133">Chaque élément est une valeur unique, un index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-133">Each element is a single value, a color index.</span></span> <span data-ttu-id="1c0a7-134">Elle est convertie en virgule fixe (avec un nombre non spécifié de 0 bits à droite du point binaire), décalée vers la gauche ou vers la droite selon la valeur et le signe du décalage de l' \_ index GL \_ , puis ajoutée au décalage de l' \_ index GL \_ (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-134">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="1c0a7-135">L’index résultant est converti en un ensemble de composants de couleur à l’aide de la \_ carte de pixels GL \_ \_ i \_ à \_ R, de \_ \_ cartes de pixels GL \_ i \_ à \_ G, de mappage de \_ Pixel GL \_ \_ i \_ à \_ B et de carte de \_ pixels GL \_ \_ i \_ en \_ tables, et fixé à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-135">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="1c0a7-136"><dt>**GL \_ rouge**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-136"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="1c0a7-137">Chaque élément est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-137">Each element is a single red component.</span></span> <span data-ttu-id="1c0a7-138">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le vert et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-138">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="1c0a7-139">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-139">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="1c0a7-140"><dt>**\_vert GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-140"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="1c0a7-141">Chaque élément est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-141">Each element is a single green component.</span></span> <span data-ttu-id="1c0a7-142">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge et le bleu, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-142">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="1c0a7-143">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-143">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="1c0a7-144"><dt>**\_bleu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-144"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="1c0a7-145">Chaque élément est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-145">Each element is a single blue component.</span></span> <span data-ttu-id="1c0a7-146">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge et le vert, et 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-146">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="1c0a7-147">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-147">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="1c0a7-148"><dt>**GL \_ alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-148"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="1c0a7-149">Chaque élément est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-149">Each element is a single red component.</span></span> <span data-ttu-id="1c0a7-150">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-150">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="1c0a7-151">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-151">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="1c0a7-152"><dt>**\_RGB GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-152"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="1c0a7-153">Chaque élément est un triple RVB.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-153">Each element is an RGB triple.</span></span> <span data-ttu-id="1c0a7-154">Il est converti en virgule flottante et assemblé en élément RVBA en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-154">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="1c0a7-155">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-155">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="1c0a7-156"><dt>**GL \_ RVBA**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-156"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="1c0a7-157">Chaque élément est un élément RVBA complet.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-157">Each element is a complete RGBA element.</span></span> <span data-ttu-id="1c0a7-158">Elle est convertie en virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-158">It is converted to floating point.</span></span> <span data-ttu-id="1c0a7-159">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-159">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="1c0a7-160"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-160"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="1c0a7-161">Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-161">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="1c0a7-162">GL \_ BGR \_ ext fournit un format qui correspond à la disposition de la mémoire des bitmaps indépendantes du périphérique (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-162">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="1c0a7-163">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-163">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="1c0a7-164"><dt>**GL \_ BGRA \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-164"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="1c0a7-165">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-165">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span> <span data-ttu-id="1c0a7-166">GL \_ BGRA \_ ext fournit un format qui correspond à la disposition de la mémoire des bitmaps indépendantes du périphérique (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-166">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="1c0a7-167">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-167">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="1c0a7-168"><dt>**LUMINANCE du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-168"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="1c0a7-169">Chaque élément est une valeur de luminance unique.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-169">Each element is a single luminance value.</span></span> <span data-ttu-id="1c0a7-170">Elle est convertie en virgule flottante, puis Assemblée en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu, et en joignant 1,0 pour alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-170">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="1c0a7-171">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-171">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="1c0a7-172"><dt>**\_luminance \_ alpha du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-172"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="1c0a7-173">Chaque élément est une paire luminance/alpha.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-173">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="1c0a7-174">Elle est convertie en virgule flottante, puis Assemblée en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-174">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="1c0a7-175">Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-175">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="1c0a7-176">*type*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-176">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-177">Type de données des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-177">The data type of the pixel data.</span></span> <span data-ttu-id="1c0a7-178">Les valeurs symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-178">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a7-179">*pixels*</span><span class="sxs-lookup"><span data-stu-id="1c0a7-179">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="1c0a7-180">Pointeur vers les données de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-180">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c0a7-181">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c0a7-181">Return value</span></span>

<span data-ttu-id="1c0a7-182">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-182">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1c0a7-183">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1c0a7-183">Error codes</span></span>

<span data-ttu-id="1c0a7-184">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-184">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1c0a7-185">Nom</span><span class="sxs-lookup"><span data-stu-id="1c0a7-185">Name</span></span>                                                                                                  | <span data-ttu-id="1c0a7-186">Signification</span><span class="sxs-lookup"><span data-stu-id="1c0a7-186">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c0a7-187"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1c0a7-188">la *cible* n’était pas une \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-188">*target* was not an GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="1c0a7-189"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-189"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1c0a7-190">le *format* n’était pas une constante de *format* acceptée.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-190">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="1c0a7-191">Seules les constantes de format autres que l' \_ index du stencil GL et le composant de \_ \_ profondeur GL \_ sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-191">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="1c0a7-192">Pour obtenir la liste des valeurs possibles, consultez la description du paramètre *format* .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-192">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="1c0a7-193"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1c0a7-194">le *type* n’est pas une constante de *type* .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-194">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1c0a7-195"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-195"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1c0a7-196">le *type* était \_ bitmap GL et le *format* n’était pas l’index de \_ couleur GL \_ .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-196">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="1c0a7-197"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1c0a7-198">le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* était la valeur retournée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-198">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="1c0a7-199"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1c0a7-200">*internalformat* n’était pas 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-200">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="1c0a7-201"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1c0a7-202">la *largeur* ou la hauteur est inférieure à zéro ou supérieure à 2 + la \_ taille de la texture GL maximum \_ \_ , ou elle ne peut pas être représentée sous la forme 2 *n* + 2 (bordure) pour une valeur entière de *n*.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-202">*width* or height was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="1c0a7-203"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-203"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1c0a7-204">la *bordure* n’est pas 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-204">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1c0a7-205"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-205"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1c0a7-206">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-206">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="1c0a7-207">Notes</span><span class="sxs-lookup"><span data-stu-id="1c0a7-207">Remarks</span></span>

<span data-ttu-id="1c0a7-208">La fonction **glTexImage2D** spécifie une image de texture à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-208">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span> <span data-ttu-id="1c0a7-209">La texturation mappe une partie d’une *image de texture* spécifiée sur chaque primitive graphique pour laquelle la texturation est activée.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-209">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="1c0a7-210">La texturation à deux dimensions est activée et désactivée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-210">Two-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="1c0a7-211">Les images de texture sont définies avec **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-211">Texture images are defined with **glTexImage2D**.</span></span> <span data-ttu-id="1c0a7-212">Les arguments décrivent les paramètres de l’image de texture, tels que la hauteur, la largeur, la largeur de la bordure, le nombre de niveaux de détail (voir [**glTexParameter**](gltexparameter-functions.md)) et le nombre de composants de couleur fournis.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-212">The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="1c0a7-213">Les trois derniers arguments décrivent le mode de représentation de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-213">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="1c0a7-214">Ces arguments sont identiques aux formats de pixels utilisés pour [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-214">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="1c0a7-215">Les données sont lues à partir de *pixels* sous la forme d’une séquence d’octets signés ou non signés, de shorts ou de longs, ou de valeurs à virgule flottante simple précision, en fonction du *type*.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-215">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="1c0a7-216">Ces valeurs sont regroupées en jeux d’une, deux, trois ou quatre valeurs, selon le *format*, pour former des éléments.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-216">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="1c0a7-217">Si le *type* est \_ bitmap GL, les données sont considérées comme une chaîne d’octets non signés (et le *format* doit être un index de couleur GL \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-217">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="1c0a7-218">Chaque octet de données est traité comme des éléments 8 1 bits, l’ordonnancement des bits étant déterminé par le \_ décompression GL \_ LSB en \_ premier (voir [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0a7-218">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span> <span data-ttu-id="1c0a7-219">Pour obtenir une description des valeurs acceptables pour le paramètre de *type* , consultez [**glDrawPixels**](gldrawpixels.md) .</span><span class="sxs-lookup"><span data-stu-id="1c0a7-219">Please see [**glDrawPixels**](gldrawpixels.md) for a description of the acceptable values for the *type* parameter.</span></span>

<span data-ttu-id="1c0a7-220">Une image de texture peut avoir jusqu’à quatre composants par élément de texture, en fonction des *composants*.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-220">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="1c0a7-221">Une image de texture à un composant utilise uniquement le composant rouge de la couleur RVBA extraite des *pixels*.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-221">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="1c0a7-222">Une image à deux composants utilise les valeurs R et A.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-222">A two-component image uses the R and A values.</span></span> <span data-ttu-id="1c0a7-223">Une image à trois composants utilise les valeurs R, G et B.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-223">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="1c0a7-224">Une image à quatre composants utilise tous les composants RVBA.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-224">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="1c0a7-225">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-225">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="1c0a7-226">L’image de texture peut être représentée par les mêmes formats de données que les pixels d’une commande **glDrawPixels** , à ceci près que le \_ composant index du stencil GL \_ et profondeur du GL \_ \_ ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-226">The texture image can be represented by the same data formats as the pixels in a **glDrawPixels** command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="1c0a7-227">Les modes [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-227">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="1c0a7-228">Une image de texture avec une hauteur ou une largeur nulle indique la texture null.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-228">A texture image with zero height or width indicates the null texture.</span></span> <span data-ttu-id="1c0a7-229">Si la texture null est spécifiée pour le niveau de détail 0, c’est comme si la texturation était désactivée.</span><span class="sxs-lookup"><span data-stu-id="1c0a7-229">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="1c0a7-230">Les fonctions suivantes récupèrent les informations relatives à **glTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="1c0a7-230">The following functions retrieve information related to **glTexImage2D**:</span></span>

[<span data-ttu-id="1c0a7-231">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-231">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="1c0a7-232">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="1c0a7-232">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="1c0a7-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c0a7-233">Requirements</span></span>



| <span data-ttu-id="1c0a7-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c0a7-234">Requirement</span></span> | <span data-ttu-id="1c0a7-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0a7-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0a7-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0a7-236">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0a7-237">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c0a7-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1c0a7-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0a7-238">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0a7-239">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c0a7-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c0a7-240">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c0a7-240">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c0a7-241"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-241"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1c0a7-242">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c0a7-242">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c0a7-243"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-243"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1c0a7-244">DLL</span><span class="sxs-lookup"><span data-stu-id="1c0a7-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c0a7-245"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a7-245"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0a7-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c0a7-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0a7-247">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-247">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-248">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-248">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-249">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-249">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-250">**glFog**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-250">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-251">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-251">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-252">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-252">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-253">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-253">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-254">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-254">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-255">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-255">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1c0a7-257">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1c0a7-257">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





