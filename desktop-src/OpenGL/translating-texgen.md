---
title: Traduction de texgen
description: La fonction IRIS GL texgen est traduite en glTexGen pour OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
- Portage du grand livre de l’IRIS, texgen
- Portage à partir de IRIS GL, texgen
- portage vers OpenGL à partir de IRIS GL, texgen
- Portage OpenGL à partir de IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510844"
---
# <a name="translating-texgen"></a><span data-ttu-id="920a5-113">Traduction de texgen</span><span class="sxs-lookup"><span data-stu-id="920a5-113">Translating texgen</span></span>

<span data-ttu-id="920a5-114">La fonction IRIS GL **texgen** est traduite en [glTexGen](gltexgen-functions.md) pour OpenGL.</span><span class="sxs-lookup"><span data-stu-id="920a5-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="920a5-115">Avec IRIS GL, vous appelez **texgen** deux fois : une fois pour définir simultanément le mode et l’équation plan, et une fois pour activer la génération des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="920a5-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="920a5-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="920a5-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="920a5-117">Avec OpenGL, vous effectuez trois appels : deux à **glTexGen** (une fois pour définir le mode et une fois pour définir l’équation du plan) et un à [**glEnable**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="920a5-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="920a5-118">Par exemple, le code OpenGL équivalent au code de la comptabilité IRIS ci-dessus est le suivant :</span><span class="sxs-lookup"><span data-stu-id="920a5-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="920a5-119">Le tableau suivant répertorie les noms des coordonnées de texture et leurs équivalents OpenGL.</span><span class="sxs-lookup"><span data-stu-id="920a5-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="920a5-120">Coordonnée de texture du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="920a5-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="920a5-121">Coordonnée de texture OpenGL</span><span class="sxs-lookup"><span data-stu-id="920a5-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="920a5-122">argument glEnable</span><span class="sxs-lookup"><span data-stu-id="920a5-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="920a5-123">TX \_ S</span><span class="sxs-lookup"><span data-stu-id="920a5-123">TX\_S</span></span>                      | <span data-ttu-id="920a5-124">GL \_ S</span><span class="sxs-lookup"><span data-stu-id="920a5-124">GL\_S</span></span>                     | <span data-ttu-id="920a5-125">GL \_ texture \_ GEN \_ S</span><span class="sxs-lookup"><span data-stu-id="920a5-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="920a5-126">TX \_ T</span><span class="sxs-lookup"><span data-stu-id="920a5-126">TX\_T</span></span>                      | <span data-ttu-id="920a5-127">GL \_ T</span><span class="sxs-lookup"><span data-stu-id="920a5-127">GL\_T</span></span>                     | <span data-ttu-id="920a5-128">GL \_ texture \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="920a5-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="920a5-129">TX \_ R</span><span class="sxs-lookup"><span data-stu-id="920a5-129">TX\_R</span></span>                      | <span data-ttu-id="920a5-130">GL \_ R</span><span class="sxs-lookup"><span data-stu-id="920a5-130">GL\_R</span></span>                     | <span data-ttu-id="920a5-131">GL \_ texture \_ GEN \_ R</span><span class="sxs-lookup"><span data-stu-id="920a5-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="920a5-132">TX \_ Q</span><span class="sxs-lookup"><span data-stu-id="920a5-132">TX\_Q</span></span>                      | <span data-ttu-id="920a5-133">\_Q</span><span class="sxs-lookup"><span data-stu-id="920a5-133">GL\_Q</span></span>                     | <span data-ttu-id="920a5-134">GL \_ texture \_ GEN \_ Q</span><span class="sxs-lookup"><span data-stu-id="920a5-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="920a5-135">Le tableau suivant répertorie les modes de génération de texture de l’IRIS dans le GL ainsi que les modes de texture et les noms de plans OpenGL équivalents.</span><span class="sxs-lookup"><span data-stu-id="920a5-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="920a5-136">Mode de texture du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="920a5-136">IRIS GL texture mode</span></span> | <span data-ttu-id="920a5-137">Mode de texture OpenGL</span><span class="sxs-lookup"><span data-stu-id="920a5-137">OpenGL texture mode</span></span> | <span data-ttu-id="920a5-138">Nom du plan OpenGL</span><span class="sxs-lookup"><span data-stu-id="920a5-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="920a5-139">TG en \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="920a5-139">TG\_LINEAR</span></span>           | <span data-ttu-id="920a5-140">\_objet \_ linéaire de la comptabilité</span><span class="sxs-lookup"><span data-stu-id="920a5-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="920a5-141">\_plan d’objet GL \_</span><span class="sxs-lookup"><span data-stu-id="920a5-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="920a5-142">\_contour TG</span><span class="sxs-lookup"><span data-stu-id="920a5-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="920a5-143">linéaire de l' \_ oeil GL \_</span><span class="sxs-lookup"><span data-stu-id="920a5-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="920a5-144">\_plan oculaire \_ GL</span><span class="sxs-lookup"><span data-stu-id="920a5-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="920a5-145">TG \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="920a5-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="920a5-146">\_carte de sphère GL \_</span><span class="sxs-lookup"><span data-stu-id="920a5-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




