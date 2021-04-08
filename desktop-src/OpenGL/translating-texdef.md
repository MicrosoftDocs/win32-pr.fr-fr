---
title: Traduction de texdef
description: L’exemple de code suivant est une définition de texture de la comptabilité IRIS
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
- Portage du grand livre de l’IRIS, texdef
- Portage à partir de IRIS GL, texdef
- portage vers OpenGL à partir de IRIS GL, texdef
- Portage OpenGL à partir de IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840694"
---
# <a name="translating-texdef"></a><span data-ttu-id="27f39-113">Traduction de texdef</span><span class="sxs-lookup"><span data-stu-id="27f39-113">Translating texdef</span></span>

<span data-ttu-id="27f39-114">L’exemple de code suivant est une définition de texture de la comptabilité IRIS :</span><span class="sxs-lookup"><span data-stu-id="27f39-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="27f39-115">Dans l’exemple précédent, **texdef** spécifie le \_ filtre de point de transmission en tant que Zoom et le filtre de minimisation, et TX \_ REPEAT comme mécanisme d’habillage.</span><span class="sxs-lookup"><span data-stu-id="27f39-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="27f39-116">Il spécifie également l’image de texture : **\_ texture granit**.</span><span class="sxs-lookup"><span data-stu-id="27f39-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="27f39-117">Dans OpenGL, [**glTexImage**](glteximage1d.md) spécifie l’image et [glTexParameter](gltexparameter-functions.md) définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="27f39-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="27f39-118">Pour traduire les définitions de texture d’IRIS GL, remplacez la fonction **textdef** par **glTexImage** et un ou plusieurs appels à **glTexParameter**.</span><span class="sxs-lookup"><span data-stu-id="27f39-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="27f39-119">Le code de la comptabilité IRIS précédent ressemble à celui-ci lorsqu’il est traduit en OpenGL :</span><span class="sxs-lookup"><span data-stu-id="27f39-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="27f39-120">Le tableau suivant répertorie les paramètres d’IRIS GL texture et leurs paramètres OpenGL équivalents.</span><span class="sxs-lookup"><span data-stu-id="27f39-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="27f39-121">Paramètre de texture IRIS GL</span><span class="sxs-lookup"><span data-stu-id="27f39-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="27f39-122">Paramètre de texture OpenGL</span><span class="sxs-lookup"><span data-stu-id="27f39-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="27f39-123">TX \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="27f39-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="27f39-124">filtre de la \_ texture GL \_ min. \_</span><span class="sxs-lookup"><span data-stu-id="27f39-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="27f39-125">TX \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="27f39-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="27f39-126">filtre de la \_ texture GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="27f39-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="27f39-127">TX \_ Wrap, TX \_ Wrap \_ S</span><span class="sxs-lookup"><span data-stu-id="27f39-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="27f39-128">\_ \_ encapsuler la texture GL \_ S</span><span class="sxs-lookup"><span data-stu-id="27f39-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="27f39-129">TX \_ Wrap, TX \_ Wrap \_ T</span><span class="sxs-lookup"><span data-stu-id="27f39-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="27f39-130">\_couleur de \_ bordure de la \_ texture TGL de la \_ \_ texture \_ GL</span><span class="sxs-lookup"><span data-stu-id="27f39-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="27f39-131">Le tableau suivant répertorie les valeurs possibles des paramètres de texture IRIS GL et leurs paramètres OpenGL équivalents.</span><span class="sxs-lookup"><span data-stu-id="27f39-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="27f39-132">Paramètre de texture IRIS GL</span><span class="sxs-lookup"><span data-stu-id="27f39-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="27f39-133">Paramètre de texture OpenGL</span><span class="sxs-lookup"><span data-stu-id="27f39-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="27f39-134">POINT de transmission \_</span><span class="sxs-lookup"><span data-stu-id="27f39-134">TX\_POINT</span></span>                 | <span data-ttu-id="27f39-135">GL \_ le plus proche</span><span class="sxs-lookup"><span data-stu-id="27f39-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="27f39-136">unilinéaire TX \_</span><span class="sxs-lookup"><span data-stu-id="27f39-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="27f39-137">linéaire du GL \_</span><span class="sxs-lookup"><span data-stu-id="27f39-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="27f39-138">\_point MIPMAP \_ TX</span><span class="sxs-lookup"><span data-stu-id="27f39-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="27f39-139">MIPMAP du GL le plus proche \_ \_ \_ le plus proche</span><span class="sxs-lookup"><span data-stu-id="27f39-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="27f39-140">\_MIPMAP en \_ BIlinéaire TX</span><span class="sxs-lookup"><span data-stu-id="27f39-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="27f39-141">\_MIPMAP linéaire \_ GL \_ le plus proche</span><span class="sxs-lookup"><span data-stu-id="27f39-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="27f39-142">\_MIPMAP TX \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="27f39-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="27f39-143">MIPMAP linéaire de la comptabilité la \_ plus proche \_ \_</span><span class="sxs-lookup"><span data-stu-id="27f39-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="27f39-144">TX \_ TRIlinéaire</span><span class="sxs-lookup"><span data-stu-id="27f39-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="27f39-145">MIPMAP linéaire du GL du GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="27f39-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 





