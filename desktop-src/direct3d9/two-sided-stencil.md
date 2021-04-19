---
description: Les volumes de clichés instantanés permettent de dessiner des ombres avec la mémoire tampon de stencil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided gabarit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514101"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="6ab35-103">Two-Sided gabarit (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6ab35-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="6ab35-104">Les volumes de clichés instantanés permettent de dessiner des ombres avec la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="6ab35-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="6ab35-105">L’application calcule les volumes de clichés instantanés convertis par la géométrie de la Boucher, en calculant les bords silhouettes et en les séparant de la lumière dans un ensemble de volumes 3D.</span><span class="sxs-lookup"><span data-stu-id="6ab35-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="6ab35-106">Ces volumes sont ensuite restitués deux fois dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="6ab35-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="6ab35-107">Le premier rendu dessine des polygones vers l’avant et incrémente les valeurs de mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="6ab35-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="6ab35-108">Le deuxième rendu dessine les polygones de l’arrière-plan du volume de cliché instantané et décrémente les valeurs de la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="6ab35-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="6ab35-109">Normalement, toutes les valeurs incrémentées et décrémentées s’annulent les unes des autres. Toutefois, la scène était déjà rendue avec une géométrie normale provoquant l’échec du test de la mémoire tampon z pour certains pixels, car le volume de cliché instantané est rendu.</span><span class="sxs-lookup"><span data-stu-id="6ab35-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="6ab35-110">Les valeurs laissées dans la mémoire tampon du stencil correspondent aux pixels qui se trouvent dans l’ombre.</span><span class="sxs-lookup"><span data-stu-id="6ab35-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="6ab35-111">Ces contenus de tampons de stencil restants sont utilisés comme masque, afin de mélanger en 3D un grand nombre de cœurs noirs englobant tous dans la scène.</span><span class="sxs-lookup"><span data-stu-id="6ab35-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="6ab35-112">Avec la mémoire tampon de stencil jouant le rôle de masque, le résultat est d’assombrir les pixels qui se trouvent dans les ombres.</span><span class="sxs-lookup"><span data-stu-id="6ab35-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="6ab35-113">Cela signifie que la géométrie de l’ombre est dessinée deux fois par source de lumière, ce qui entraîne une pression sur le débit du vertex du GPU.</span><span class="sxs-lookup"><span data-stu-id="6ab35-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="6ab35-114">La fonctionnalité de stencil à deux côtés a été conçue pour atténuer cette situation.</span><span class="sxs-lookup"><span data-stu-id="6ab35-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="6ab35-115">Dans cette approche, il existe deux ensembles de l’état du gabarit (nommés ci-dessous), un jeu pour les triangles frontaux et l’autre pour les triangles de face arrière.</span><span class="sxs-lookup"><span data-stu-id="6ab35-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="6ab35-116">De cette façon, une seule passe est dessinée par volume de cliché instantané, par lumière.</span><span class="sxs-lookup"><span data-stu-id="6ab35-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="6ab35-117">Les modifications de l’API sont limitées à un nouvel ensemble d’États de rendu.</span><span class="sxs-lookup"><span data-stu-id="6ab35-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="6ab35-118">Le nouvel état de rendu D3DRS \_ deux \_ côtés \_ StencilMODE peut avoir la valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="6ab35-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="6ab35-119">Il a la **valeur false** par défaut, ce qui correspond au comportement actuel (DirectX 8).</span><span class="sxs-lookup"><span data-stu-id="6ab35-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="6ab35-120">Lorsque cette propriété a la valeur **true** (elle ne fonctionne que si D3DSTENCILCAPS \_ TWOSIDED est défini), les États de rendu suivants s’appliquent uniquement aux triangles avant (sens horaire).</span><span class="sxs-lookup"><span data-stu-id="6ab35-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="6ab35-121">État du rendu</span><span class="sxs-lookup"><span data-stu-id="6ab35-121">Render state</span></span>        | <span data-ttu-id="6ab35-122">Description</span><span class="sxs-lookup"><span data-stu-id="6ab35-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab35-123">D3DRS \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="6ab35-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="6ab35-124">D3DSTENCILOP à effectuer si le test du stencil échoue.</span><span class="sxs-lookup"><span data-stu-id="6ab35-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="6ab35-125">D3DRS \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="6ab35-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="6ab35-126">D3DSTENCILOP à effectuer si le test stencil réussit et que le test z échoue.</span><span class="sxs-lookup"><span data-stu-id="6ab35-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="6ab35-127">D3DRS \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="6ab35-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="6ab35-128">D3DSTENCILOP à effectuer si les deux stencils et z-tests réussissent.</span><span class="sxs-lookup"><span data-stu-id="6ab35-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="6ab35-129">D3DRS \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="6ab35-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="6ab35-130">D3DCMPFUNC FN.</span><span class="sxs-lookup"><span data-stu-id="6ab35-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="6ab35-131">Le test stencil réussit si ((Ref & Mask) stencilfn (gabarit & Mask)) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="6ab35-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="6ab35-132">Un nouvel ensemble d’États de rendu s’applique aux triangles de face arrière (à gauche).</span><span class="sxs-lookup"><span data-stu-id="6ab35-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="6ab35-133">État du rendu</span><span class="sxs-lookup"><span data-stu-id="6ab35-133">Render state</span></span>             | <span data-ttu-id="6ab35-134">Description</span><span class="sxs-lookup"><span data-stu-id="6ab35-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab35-135">D3DRS \_ CCW \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="6ab35-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="6ab35-136">D3DSTENCILOP à effectuer si le test du stencil échoue.</span><span class="sxs-lookup"><span data-stu-id="6ab35-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="6ab35-137">D3DRS \_ CCW \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="6ab35-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="6ab35-138">D3DSTENCILOP à effectuer si le test stencil réussit et que le test z échoue.</span><span class="sxs-lookup"><span data-stu-id="6ab35-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="6ab35-139">D3DRS \_ CCW \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="6ab35-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="6ab35-140">D3DSTENCILOP à effectuer si les deux stencils et z-tests réussissent.</span><span class="sxs-lookup"><span data-stu-id="6ab35-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="6ab35-141">D3DRS \_ CCW \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="6ab35-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="6ab35-142">Fonction D3DCMPFUNC.</span><span class="sxs-lookup"><span data-stu-id="6ab35-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="6ab35-143">Le test stencil réussit si ((Ref & Mask) stencilfn (gabarit & Mask)) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="6ab35-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="6ab35-144">Les États de rendu des stencils restants s’appliquent toujours à la fois à l’angle et dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="6ab35-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="6ab35-145">D3DRS \_ deux \_ côtés \_ StencilMODE est ignoré pour les lignes et les sprites point, ce qui signifie que le comportement est identique à celui de DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="6ab35-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="6ab35-146">Les \_ États de rendu du stencil D3DRS CCW \_ \* sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6ab35-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="6ab35-147">Un nouveau bit d’extrémité indique si l’appareil prend en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6ab35-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="6ab35-148">Les pilotes qui ne prennent pas en charge cette fonctionnalité sont censés ignorer ces nouveaux États de rendu.</span><span class="sxs-lookup"><span data-stu-id="6ab35-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="6ab35-149">Tous les autres bits d’extrémité du stencil s’appliquent aux deux modes de mise en mémoire tampon des stencils.</span><span class="sxs-lookup"><span data-stu-id="6ab35-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="6ab35-150">Étant donné que \_ \_ le stencil à deux côtés implique la possibilité de dessiner avec D3DCULLMODE \_ None Set, le Cap correspondant doit être défini par le pilote s’il prend en charge ce nouveau mode de stencil.</span><span class="sxs-lookup"><span data-stu-id="6ab35-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="6ab35-151">Les laboratoires WHQL (Microsoft Windows Hardware Quality Labs) doivent respecter ce point.</span><span class="sxs-lookup"><span data-stu-id="6ab35-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="6ab35-152">Nouveaux États de rendu :</span><span class="sxs-lookup"><span data-stu-id="6ab35-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="6ab35-153">Nouvelle limite :</span><span class="sxs-lookup"><span data-stu-id="6ab35-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="6ab35-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ab35-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab35-155">Techniques de tampon de stencil</span><span class="sxs-lookup"><span data-stu-id="6ab35-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="6ab35-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="6ab35-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
