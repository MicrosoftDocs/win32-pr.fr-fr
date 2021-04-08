---
title: Portage des opérations de pixels
description: Portage des opérations de pixels
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Portage de l’IRIS dans le GL, pixels
- Portage à partir de IRIS GL, pixels
- portage vers OpenGL à partir de IRIS GL, pixels
- Portage OpenGL à partir de IRIS GL, pixels
- pixels, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674538"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="4073e-108">Portage des opérations de pixels</span><span class="sxs-lookup"><span data-stu-id="4073e-108">Porting Pixel Operations</span></span>

<span data-ttu-id="4073e-109">Lors du Portage de code impliquant des opérations de pixels, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="4073e-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="4073e-110">Les opérations de pixels logiques ne sont pas appliquées aux tampons de couleurs RVBA.</span><span class="sxs-lookup"><span data-stu-id="4073e-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="4073e-111">Pour plus d’informations, consultez [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="4073e-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="4073e-112">En général, IRIS GL utilise le format ABGR pour les pixels, tandis que OpenGL utilise RVBA.</span><span class="sxs-lookup"><span data-stu-id="4073e-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="4073e-113">Vous pouvez modifier le format avec [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4073e-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="4073e-114">Lors du Portage des fonctions **lrectwrite** , veillez à noter l’endroit où **lrectwrite** écrit (par exemple, il peut écrire dans le tampon de profondeur).</span><span class="sxs-lookup"><span data-stu-id="4073e-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="4073e-115">OpenGL offre une plus grande flexibilité en matière d’opérations de pixels.</span><span class="sxs-lookup"><span data-stu-id="4073e-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="4073e-116">Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour les opérations de pixels et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="4073e-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4073e-117">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="4073e-117">IRIS GL function</span></span>                                   | <span data-ttu-id="4073e-118">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="4073e-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="4073e-119">Signification</span><span class="sxs-lookup"><span data-stu-id="4073e-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4073e-120">**lrectread**, **rectread**,**readRGB**</span><span class="sxs-lookup"><span data-stu-id="4073e-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="4073e-121">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="4073e-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="4073e-122">Lit un bloc de pixels à partir du trame.</span><span class="sxs-lookup"><span data-stu-id="4073e-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="4073e-123">**lrectwrite**, **rectwrite**</span><span class="sxs-lookup"><span data-stu-id="4073e-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="4073e-124">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="4073e-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="4073e-125">Écrit un bloc de pixels dans le trame.</span><span class="sxs-lookup"><span data-stu-id="4073e-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="4073e-126">**rectcopy**</span><span class="sxs-lookup"><span data-stu-id="4073e-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="4073e-127">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="4073e-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="4073e-128">Copie les pixels dans le trame.</span><span class="sxs-lookup"><span data-stu-id="4073e-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="4073e-129">**rectzoom**</span><span class="sxs-lookup"><span data-stu-id="4073e-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="4073e-130">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="4073e-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="4073e-131">Spécifie les facteurs de zoom de pixel pour **glDrawPixels** et **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="4073e-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="4073e-132">**cmov**</span><span class="sxs-lookup"><span data-stu-id="4073e-132">**cmov**</span></span>                                           | [<span data-ttu-id="4073e-133">glRasterPos</span><span class="sxs-lookup"><span data-stu-id="4073e-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="4073e-134">Spécifie la position raster pour les opérations de pixel.</span><span class="sxs-lookup"><span data-stu-id="4073e-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="4073e-135">**readsource**</span><span class="sxs-lookup"><span data-stu-id="4073e-135">**readsource**</span></span>                                     | [<span data-ttu-id="4073e-136">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="4073e-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="4073e-137">Sélectionne une source de mémoire tampon de couleur pour les pixels.</span><span class="sxs-lookup"><span data-stu-id="4073e-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="4073e-138">**pixmode**</span><span class="sxs-lookup"><span data-stu-id="4073e-138">**pixmode**</span></span>                                        | <span data-ttu-id="4073e-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="4073e-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="4073e-140">Définit les modes de stockage en pixels. Définissez les modes de transfert de pixels.</span><span class="sxs-lookup"><span data-stu-id="4073e-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="4073e-141">**logicop**</span><span class="sxs-lookup"><span data-stu-id="4073e-141">**logicop**</span></span>                                        | [<span data-ttu-id="4073e-142">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="4073e-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="4073e-143">Spécifie une opération logique pour les écritures de pixels.</span><span class="sxs-lookup"><span data-stu-id="4073e-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="4073e-144">[**glEnable**](glenable.md) (GL \_ Logic \_ op)</span><span class="sxs-lookup"><span data-stu-id="4073e-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="4073e-145">Active les opérations de logiques de pixels.</span><span class="sxs-lookup"><span data-stu-id="4073e-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="4073e-146">Pour obtenir la liste complète des opérations logiques possibles, consultez [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="4073e-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="4073e-147">Cet exemple de code IRIS GL illustre une écriture de pixels classique :</span><span class="sxs-lookup"><span data-stu-id="4073e-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="4073e-148">Le code précédent ressemble à celui-ci lorsqu’il est traduit en OpenGL :</span><span class="sxs-lookup"><span data-stu-id="4073e-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





