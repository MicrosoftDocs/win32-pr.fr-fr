---
title: Portage du code de fusion
description: Dans IRIS GL, quand vous dessinez sur des mémoires tampons d’arrière-plan et d’arrière-plan, la fusion est effectuée en lisant l’une des mémoires tampons, en fusionnant avec cette couleur, puis en écrivant le résultat dans les deux mémoires tampons. Dans OpenGL, toutefois, chaque tampon est lu successivement, fusionné, puis écrit.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Portage de l’IRIS dans le GL, fusion
- Portage à partir de IRIS GL, fusion
- portage vers OpenGL à partir de IRIS GL, fusion
- Portage OpenGL depuis IRIS GL, fusion
- mélanger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511035"
---
# <a name="porting-blending-code"></a><span data-ttu-id="a0e67-109">Portage du code de fusion</span><span class="sxs-lookup"><span data-stu-id="a0e67-109">Porting Blending Code</span></span>

<span data-ttu-id="a0e67-110">Dans IRIS GL, quand vous dessinez sur des mémoires tampons d’arrière-plan et d’arrière-plan, la fusion est effectuée en lisant l’une des mémoires tampons, en fusionnant avec cette couleur, puis en écrivant le résultat dans les deux mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="a0e67-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="a0e67-111">Dans OpenGL, toutefois, chaque tampon est lu successivement, fusionné, puis écrit.</span><span class="sxs-lookup"><span data-stu-id="a0e67-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="a0e67-112">Le tableau suivant répertorie les fonctions de fusion de l’IRIS dans le GL et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="a0e67-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a0e67-113">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="a0e67-113">IRIS GL function</span></span>  | <span data-ttu-id="a0e67-114">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="a0e67-114">OpenGL function</span></span>                            | <span data-ttu-id="a0e67-115">Signification</span><span class="sxs-lookup"><span data-stu-id="a0e67-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="a0e67-116">[**glEnable**](glenable.md) ( \_ mélange GL)</span><span class="sxs-lookup"><span data-stu-id="a0e67-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="a0e67-117">Active la fusion.</span><span class="sxs-lookup"><span data-stu-id="a0e67-117">Turns on blending.</span></span>          |
| <span data-ttu-id="a0e67-118">**blendfunction**</span><span class="sxs-lookup"><span data-stu-id="a0e67-118">**blendfunction**</span></span> | [<span data-ttu-id="a0e67-119">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="a0e67-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="a0e67-120">Spécifie une fonction de fusion.</span><span class="sxs-lookup"><span data-stu-id="a0e67-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="a0e67-121">La fonction OpenGL **glBlendFunc** et la fonction Iris GL **BLENDFUNCTION** sont presque identiques.</span><span class="sxs-lookup"><span data-stu-id="a0e67-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="a0e67-122">Le tableau suivant répertorie les facteurs de mélange IRIS GL et leurs équivalents OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a0e67-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="a0e67-123">IRIS GL</span><span class="sxs-lookup"><span data-stu-id="a0e67-123">IRIS GL</span></span>          | <span data-ttu-id="a0e67-124">Technologie</span><span class="sxs-lookup"><span data-stu-id="a0e67-124">OpenGL</span></span>                     | <span data-ttu-id="a0e67-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a0e67-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="a0e67-126">BF \_ zéro</span><span class="sxs-lookup"><span data-stu-id="a0e67-126">BF\_ZERO</span></span>         | <span data-ttu-id="a0e67-127">\_zéro GL</span><span class="sxs-lookup"><span data-stu-id="a0e67-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="a0e67-128">BF \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0e67-128">BF\_ONE</span></span>          | <span data-ttu-id="a0e67-129">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0e67-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="a0e67-130">\_As BF</span><span class="sxs-lookup"><span data-stu-id="a0e67-130">BF\_SA</span></span>           | <span data-ttu-id="a0e67-131">source de la \_ source GL \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="a0e67-132">BF \_ MSA</span><span class="sxs-lookup"><span data-stu-id="a0e67-132">BF\_MSA</span></span>          | <span data-ttu-id="a0e67-133">GL \_ un \_ moins de \_ src \_ alpha</span><span class="sxs-lookup"><span data-stu-id="a0e67-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="a0e67-134">BF \_ da</span><span class="sxs-lookup"><span data-stu-id="a0e67-134">BF\_DA</span></span>           | <span data-ttu-id="a0e67-135">de l' \_ heure d’été alpha du GL \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="a0e67-136">\_Assistant débogage MANAGÉ BF</span><span class="sxs-lookup"><span data-stu-id="a0e67-136">BF\_MDA</span></span>          | <span data-ttu-id="a0e67-137">GL \_ 1 \_ moins \_ heure d’été \_ alpha</span><span class="sxs-lookup"><span data-stu-id="a0e67-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="a0e67-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="a0e67-138">BF\_SC</span></span>           | <span data-ttu-id="a0e67-139">couleur de la source du GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="a0e67-140">BF \_ msc</span><span class="sxs-lookup"><span data-stu-id="a0e67-140">BF\_MSC</span></span>          | <span data-ttu-id="a0e67-141">GL \_ un \_ moins \_ \_ couleur SRC</span><span class="sxs-lookup"><span data-stu-id="a0e67-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="a0e67-142">Destination uniquement.</span><span class="sxs-lookup"><span data-stu-id="a0e67-142">Destination only.</span></span> |
| <span data-ttu-id="a0e67-143">\_DC BF</span><span class="sxs-lookup"><span data-stu-id="a0e67-143">BF\_DC</span></span>           | <span data-ttu-id="a0e67-144">couleur de l' \_ heure d’été GL \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="a0e67-145">Source uniquement.</span><span class="sxs-lookup"><span data-stu-id="a0e67-145">Source only.</span></span>      |
| <span data-ttu-id="a0e67-146">Carte \_ fille BF</span><span class="sxs-lookup"><span data-stu-id="a0e67-146">BF\_MDC</span></span>          | <span data-ttu-id="a0e67-147">\_couleur GL 1 \_ moins \_ DST \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="a0e67-148">Source uniquement.</span><span class="sxs-lookup"><span data-stu-id="a0e67-148">Source only.</span></span>      |
| <span data-ttu-id="a0e67-149">\_mini-MDA mn min \_ sa \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="a0e67-150">\_ \_ saturation alpha de la source GL \_</span><span class="sxs-lookup"><span data-stu-id="a0e67-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="a0e67-151">??</span><span class="sxs-lookup"><span data-stu-id="a0e67-151">??</span></span>

 

 




