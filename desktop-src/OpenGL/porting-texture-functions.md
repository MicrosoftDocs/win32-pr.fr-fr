---
title: Portage des fonctions de texture
description: Portage des fonctions de texture
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029436"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="b20d6-108">Portage des fonctions de texture</span><span class="sxs-lookup"><span data-stu-id="b20d6-108">Porting Texture Functions</span></span>

<span data-ttu-id="b20d6-109">Lors du Portage des fonctions de texture du GL IRIS vers OpenGL, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="b20d6-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="b20d6-110">OpenGL ne gère pas les tables de textures ; elle utilise une texture 1D et une texture 2D uniquement.</span><span class="sxs-lookup"><span data-stu-id="b20d6-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="b20d6-111">Pour réutiliser les textures de votre code IRIS GL, placez-les dans une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b20d6-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="b20d6-112">OpenGL ne génère pas automatiquement des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="b20d6-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="b20d6-113">Si vous utilisez des mipmaps, vous devez d’abord appeler la fonction [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .</span><span class="sxs-lookup"><span data-stu-id="b20d6-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="b20d6-114">Dans OpenGL, vous utilisez [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) pour activer et désactiver les fonctionnalités de texture.</span><span class="sxs-lookup"><span data-stu-id="b20d6-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="b20d6-115">Dans OpenGL, la taille de la texture est plus rigoureusement régulée que dans IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="b20d6-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="b20d6-116">La taille d’une texture OpenGL doit être :</span><span class="sxs-lookup"><span data-stu-id="b20d6-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="b20d6-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="b20d6-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="b20d6-118">où *n* est un entier et *b* est :</span><span class="sxs-lookup"><span data-stu-id="b20d6-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="b20d6-119">0, si la texture n’a pas de bordure</span><span class="sxs-lookup"><span data-stu-id="b20d6-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="b20d6-120">1, si la texture a un pixel de bordure (les textures OpenGL peuvent avoir des bordures de 1 pixel.)</span><span class="sxs-lookup"><span data-stu-id="b20d6-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="b20d6-121">Le tableau suivant répertorie les fonctions de texture de l’IRIS dans le GL et leurs équivalents OpenGL généraux.</span><span class="sxs-lookup"><span data-stu-id="b20d6-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="b20d6-122">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="b20d6-122">IRIS GL function</span></span> | <span data-ttu-id="b20d6-123">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="b20d6-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="b20d6-124">Signification</span><span class="sxs-lookup"><span data-stu-id="b20d6-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b20d6-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="b20d6-125">**textdef2d**</span></span>    | <span data-ttu-id="b20d6-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="b20d6-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="b20d6-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="b20d6-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="b20d6-128">Spécifie une image de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="b20d6-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="b20d6-129">**textbind**</span><span class="sxs-lookup"><span data-stu-id="b20d6-129">**textbind**</span></span>     | <span data-ttu-id="b20d6-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="b20d6-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="b20d6-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="b20d6-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="b20d6-132">Sélectionne une fonction de texture.</span><span class="sxs-lookup"><span data-stu-id="b20d6-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="b20d6-133">**tevdef**</span><span class="sxs-lookup"><span data-stu-id="b20d6-133">**tevdef**</span></span>       | [<span data-ttu-id="b20d6-134">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="b20d6-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="b20d6-135">Définit un environnement de mappage de texture.</span><span class="sxs-lookup"><span data-stu-id="b20d6-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="b20d6-136">**tevbind**</span><span class="sxs-lookup"><span data-stu-id="b20d6-136">**tevbind**</span></span>      | <span data-ttu-id="b20d6-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="b20d6-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="b20d6-138">Sélectionne un environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="b20d6-138">Selects a texture environment.</span></span>                                                              |
| <span data-ttu-id="b20d6-139">**H2**</span><span class="sxs-lookup"><span data-stu-id="b20d6-139">**t2**</span></span>           | [<span data-ttu-id="b20d6-140">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b20d6-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="b20d6-141">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="b20d6-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="b20d6-142">**texgen**</span><span class="sxs-lookup"><span data-stu-id="b20d6-142">**texgen**</span></span>       | <span data-ttu-id="b20d6-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="b20d6-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="b20d6-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="b20d6-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="b20d6-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="b20d6-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="b20d6-146">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="b20d6-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="b20d6-147">Contrôle la génération des coordonnées de texture. Met à l’échelle une image à une taille arbitraire.</span><span class="sxs-lookup"><span data-stu-id="b20d6-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="b20d6-148">Pour plus d’informations sur la texturation, consultez le *Guide de programmation OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="b20d6-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="b20d6-149">Cette rubrique contient des informations sur les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="b20d6-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="b20d6-150">Traduction de tevdef</span><span class="sxs-lookup"><span data-stu-id="b20d6-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="b20d6-151">Traduction de texdef</span><span class="sxs-lookup"><span data-stu-id="b20d6-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="b20d6-152">Traduction de texgen</span><span class="sxs-lookup"><span data-stu-id="b20d6-152">Translating texgen</span></span>](translating-texgen.md)

 

 





