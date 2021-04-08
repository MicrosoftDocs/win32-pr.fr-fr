---
title: Traduction de tevdef
description: L’exemple de code suivant est une définition d’environnement de texture de GL d’IRIS qui spécifie le \_ paramètre d’environnement de texture de DÉCALCOMANIE TV
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
- Portage du grand livre de l’IRIS, tevdef
- Portage à partir de IRIS GL, tevdef
- portage vers OpenGL à partir de IRIS GL, tevdef
- Portage OpenGL à partir de IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940280"
---
# <a name="translating-tevdef"></a><span data-ttu-id="c38ae-113">Traduction de tevdef</span><span class="sxs-lookup"><span data-stu-id="c38ae-113">Translating tevdef</span></span>

<span data-ttu-id="c38ae-114">L’exemple de code suivant est une définition d’environnement de texture de GL d’IRIS qui spécifie le \_ paramètre d’environnement de texture de DÉCALCOMANIE TV :</span><span class="sxs-lookup"><span data-stu-id="c38ae-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="c38ae-115">et le même code traduit en OpenGL :</span><span class="sxs-lookup"><span data-stu-id="c38ae-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="c38ae-116">Le tableau suivant répertorie les paramètres d’environnement de texture du GL d’IRIS et leurs paramètres OpenGL équivalents.</span><span class="sxs-lookup"><span data-stu-id="c38ae-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="c38ae-117">Paramètre IRIS GL</span><span class="sxs-lookup"><span data-stu-id="c38ae-117">IRIS GL parameter</span></span>     | <span data-ttu-id="c38ae-118">Paramètre OpenGL</span><span class="sxs-lookup"><span data-stu-id="c38ae-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="c38ae-119">\_modulation TV</span><span class="sxs-lookup"><span data-stu-id="c38ae-119">TV\_MODULATE</span></span>          | <span data-ttu-id="c38ae-120">module comptabilité GL \_</span><span class="sxs-lookup"><span data-stu-id="c38ae-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="c38ae-121">\_DÉCALCOMANIE TV</span><span class="sxs-lookup"><span data-stu-id="c38ae-121">TV\_DECAL</span></span>             | <span data-ttu-id="c38ae-122">décalque GL \_</span><span class="sxs-lookup"><span data-stu-id="c38ae-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="c38ae-123">\_fusion TV</span><span class="sxs-lookup"><span data-stu-id="c38ae-123">TV\_BLEND</span></span>             | <span data-ttu-id="c38ae-124">fusion du GL \_</span><span class="sxs-lookup"><span data-stu-id="c38ae-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="c38ae-125">\_couleur TV</span><span class="sxs-lookup"><span data-stu-id="c38ae-125">TV\_COLOR</span></span>             | <span data-ttu-id="c38ae-126">couleur de la texture du GL \_ \_ env \_</span><span class="sxs-lookup"><span data-stu-id="c38ae-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="c38ae-127">TV \_ alpha</span><span class="sxs-lookup"><span data-stu-id="c38ae-127">TV\_ALPHA</span></span>             | <span data-ttu-id="c38ae-128">Aucun équivalent OpenGL direct.</span><span class="sxs-lookup"><span data-stu-id="c38ae-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="c38ae-129">\_sélection du composant TV \_</span><span class="sxs-lookup"><span data-stu-id="c38ae-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="c38ae-130">Aucun équivalent OpenGL direct.</span><span class="sxs-lookup"><span data-stu-id="c38ae-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="c38ae-131">Pour plus d’informations sur les paramètres de l’environnement de texture, consultez [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c38ae-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 




