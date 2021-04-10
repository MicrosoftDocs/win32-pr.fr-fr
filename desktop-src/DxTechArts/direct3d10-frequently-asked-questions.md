---
title: 'Direct3D 10 : Forum Aux Questions'
description: Cet article contient certaines des questions fréquemment posées concernant Direct3D 10, du point de vue d’un développeur qui Portage une application existante de Direct3D 9 (D3D9) vers Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101897"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="a41fc-103">Direct3D 10 : Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="a41fc-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="a41fc-104">Cet article contient certaines des questions fréquemment posées concernant Direct3D 10, du point de vue d’un développeur qui Portage une application existante de Direct3D 9 (D3D9) vers Direct3D 10 (D3D10).</span><span class="sxs-lookup"><span data-stu-id="a41fc-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="a41fc-105">Mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="a41fc-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="a41fc-106">State</span><span class="sxs-lookup"><span data-stu-id="a41fc-106">State</span></span>](#state)
-   [<span data-ttu-id="a41fc-107">Formats</span><span class="sxs-lookup"><span data-stu-id="a41fc-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="a41fc-108">Liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a41fc-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="a41fc-109">Appels de dessin</span><span class="sxs-lookup"><span data-stu-id="a41fc-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="a41fc-110">Ressources</span><span class="sxs-lookup"><span data-stu-id="a41fc-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="a41fc-111">Profondeur comme texture</span><span class="sxs-lookup"><span data-stu-id="a41fc-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="a41fc-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="a41fc-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="a41fc-113">Crashes</span><span class="sxs-lookup"><span data-stu-id="a41fc-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="a41fc-114">Rendu prédicat</span><span class="sxs-lookup"><span data-stu-id="a41fc-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="a41fc-115">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="a41fc-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="a41fc-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="a41fc-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="a41fc-117">Mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="a41fc-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Quelle est la meilleure façon de mettre à jour les mémoires tampons constantes ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="a41fc-119">UpdateSubresource et Map with Discard doivent être à la même vitesse.</span><span class="sxs-lookup"><span data-stu-id="a41fc-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="a41fc-120">Choisissez entre elles en fonction de laquelle une copie la plus petite quantité de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a41fc-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="a41fc-121">Si vos données sont déjà stockées en mémoire dans un bloc contigu, utilisez UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="a41fc-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="a41fc-122">Si vous devez accumuler des données à partir d’autres emplacements, utilisez la fonction Map with Discard.</span><span class="sxs-lookup"><span data-stu-id="a41fc-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Quelle est la pire façon d’organiser les mémoires tampons constantes ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="a41fc-124">Les pires performances sont obtenues en plaçant toutes les constantes d’un nuanceur particulier dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="a41fc-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="a41fc-125">Bien qu’il s’agisse souvent du moyen le plus simple de portage de D3D9 vers D3D10, cela peut paralyser les performances.</span><span class="sxs-lookup"><span data-stu-id="a41fc-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="a41fc-126">Par exemple, imaginez un scénario qui utilise la mémoire tampon constante suivante :</span><span class="sxs-lookup"><span data-stu-id="a41fc-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="a41fc-127">La mémoire tampon est de 6560 octets.</span><span class="sxs-lookup"><span data-stu-id="a41fc-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="a41fc-128">Supposons qu’il existe une application avec 1000 objets à restituer, 100 qui sont des maillages dépouillés et 900 de maillages statiques.</span><span class="sxs-lookup"><span data-stu-id="a41fc-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="a41fc-129">Par ailleurs, supposons que cette application utilise le mappage Shadow avec une source de lumière.</span><span class="sxs-lookup"><span data-stu-id="a41fc-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="a41fc-130">Cela signifie qu’il y a deux passes, une pour la carte de profondeur rendue à partir de la lumière et une pour la passe de rendu avant.</span><span class="sxs-lookup"><span data-stu-id="a41fc-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="a41fc-131">Cela provoque des appels 2000 Draw.</span><span class="sxs-lookup"><span data-stu-id="a41fc-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="a41fc-132">Bien que chaque appel de dessin n’ait pas besoin de mettre à jour toutes les parties de la mémoire tampon constante, la totalité de la mémoire tampon constante est toujours mise à jour et envoyée à la carte.</span><span class="sxs-lookup"><span data-stu-id="a41fc-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="a41fc-133">Cela entraîne la mise à jour de 13 Mo de données toutes les trames (2000 de dessin appelle l’heure 6560 Ko).</span><span class="sxs-lookup"><span data-stu-id="a41fc-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Quelle est la meilleure façon d’organiser mes mémoires tampons constantes ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="a41fc-135">Le meilleur moyen consiste à organiser des mémoires tampons constantes par fréquence de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a41fc-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="a41fc-136">Les constantes mises à jour à des fréquences similaires doivent se trouver dans la même mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a41fc-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="a41fc-137">Par exemple, considérez le scénario présenté sous, « quel est le pire moyen d’organiser les mémoires tampons constantes ? », mais avec une meilleure disposition constante :</span><span class="sxs-lookup"><span data-stu-id="a41fc-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="a41fc-138">Les mémoires tampons constantes sont divisées en fonction de leur fréquence de mise à jour, mais ce n’est que la moitié de la solution.</span><span class="sxs-lookup"><span data-stu-id="a41fc-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="a41fc-139">L’application doit mettre à jour les mémoires tampons constantes correctement afin de tirer pleinement parti du fractionnement.</span><span class="sxs-lookup"><span data-stu-id="a41fc-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="a41fc-140">Nous allons supposer la même scène que ci-dessus : 900 maillages statiques, 100 maillages dépouillés, un passe de lumière et une passe directe.</span><span class="sxs-lookup"><span data-stu-id="a41fc-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="a41fc-141">Nous supposons également que certaines mémoires tampons constantes par objet seront stockées.</span><span class="sxs-lookup"><span data-stu-id="a41fc-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="a41fc-142">Cela signifie que chaque objet contiendra soit un VSPerSkinnedCB, soit un VSPerStaticCB, selon qu’il est dépouillé ou statique.</span><span class="sxs-lookup"><span data-stu-id="a41fc-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="a41fc-143">Nous faisons cela pour éviter le double de la quantité de matrices envoyées via le pipeline.</span><span class="sxs-lookup"><span data-stu-id="a41fc-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="a41fc-144">Nous séparons le cadre en trois phases.</span><span class="sxs-lookup"><span data-stu-id="a41fc-144">We split the frame into three phases.</span></span> <span data-ttu-id="a41fc-145">La première phase est le début du frame et ne nécessite pas de rendu, juste des mises à jour constantes.</span><span class="sxs-lookup"><span data-stu-id="a41fc-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Frame de début**</span><span class="sxs-lookup"><span data-stu-id="a41fc-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="a41fc-147">Mettre à jour VSGlobalPerFrameCB pour l’heure de l’application (4 octets)</span><span class="sxs-lookup"><span data-stu-id="a41fc-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="a41fc-148">Mise à jour 100 VSPerSkinnedCB pour les objets dépouillés 100 (640000 octets)</span><span class="sxs-lookup"><span data-stu-id="a41fc-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="a41fc-149">Mettre à jour VSPerStaticCB pour 900 objets statiques (57600 octets)</span><span class="sxs-lookup"><span data-stu-id="a41fc-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="a41fc-150">L’étape suivante est le passage de la table fictive.</span><span class="sxs-lookup"><span data-stu-id="a41fc-150">Next is the shadow map pass.</span></span> <span data-ttu-id="a41fc-151">Notez que la seule mémoire tampon constante qui est réellement mise à jour est VSPerPassCB.</span><span class="sxs-lookup"><span data-stu-id="a41fc-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="a41fc-152">Toutes les autres mémoires tampons constantes ont été mises à jour pendant le passage de frame de début.</span><span class="sxs-lookup"><span data-stu-id="a41fc-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="a41fc-153">Bien que nous ayons toujours besoin de lier ces mémoires tampons constantes, la quantité d’informations transmises à la carte vidéo est minime, car les tampons ont déjà été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a41fc-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Passe-miroir**</span><span class="sxs-lookup"><span data-stu-id="a41fc-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="a41fc-155">Mettre à jour VSPerPassCB (72 octets)</span><span class="sxs-lookup"><span data-stu-id="a41fc-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="a41fc-156">Dessiner 100 maillages dépouillés (100 liaisons, aucune mise à jour)</span><span class="sxs-lookup"><span data-stu-id="a41fc-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="a41fc-157">Dessiner 900 mailles statiques (100 liaisons, aucune mise à jour)</span><span class="sxs-lookup"><span data-stu-id="a41fc-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="a41fc-158">De même, le test de rendu de transfert doit uniquement mettre à jour les données par matériau, car il n’a pas été stocké par maillage.</span><span class="sxs-lookup"><span data-stu-id="a41fc-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="a41fc-159">Si nous partons du principe qu’il existe 500 matériaux en cours d’utilisation dans la scène :</span><span class="sxs-lookup"><span data-stu-id="a41fc-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Transfert direct**</span><span class="sxs-lookup"><span data-stu-id="a41fc-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="a41fc-161">Mettre à jour VSPerPassCB (72 octets)</span><span class="sxs-lookup"><span data-stu-id="a41fc-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="a41fc-162">Mise à jour 500 VSPerMaterialCBs (10000 octets)</span><span class="sxs-lookup"><span data-stu-id="a41fc-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="a41fc-163">Il en résulte un total de 707 Ko seulement.</span><span class="sxs-lookup"><span data-stu-id="a41fc-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="a41fc-164">Bien qu’il s’agisse d’un scénario très fictif, il illustre simplement la quantité de surcharge de mise à jour constante pouvant être réduite en triant les constantes par fréquence de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a41fc-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a41fc-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Que se passe-t-il si je n’ai pas suffisamment d’espace pour stocker des mémoires tampons constantes pour mes maillages, notre matériel, etc. ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-166">Vous pouvez toujours utiliser un système à plusieurs niveaux de mémoires tampons constantes.</span><span class="sxs-lookup"><span data-stu-id="a41fc-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="a41fc-167">Créez des mémoires tampons constantes de taille variable (16 octets, 32 octets, 64 octets, etc.) jusqu’à la plus grande taille de mémoire tampon constante nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a41fc-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="a41fc-168">Lorsqu’il est temps de lier une mémoire tampon constante à un nuanceur, sélectionnez la plus petite mémoire tampon constante qui peut contenir les données requises par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="a41fc-169">Bien que cette approche soit légèrement moins efficace, il s’agit d’une bonne étape intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="a41fc-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Je partage des mémoires tampons constantes entre différents nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="a41fc-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="a41fc-171">Un nuanceur peut utiliser toutes les constantes, mais un autre peut utiliser certaines des constantes.</span><span class="sxs-lookup"><span data-stu-id="a41fc-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="a41fc-172">Quelle est la meilleure façon de les mettre à jour ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-173">Une approche consiste à fractionner le tampon constant encore plus loin.</span><span class="sxs-lookup"><span data-stu-id="a41fc-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="a41fc-174">Toutefois, il y a un point où trop de mémoires tampons constantes sont liées.</span><span class="sxs-lookup"><span data-stu-id="a41fc-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="a41fc-175">Dans ce cas, déplacez les constantes qui sont susceptibles d’être inutilisées par plusieurs nuanceurs jusqu’à la fin de la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="a41fc-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="a41fc-176">Lors de l’obtention des données de la variable à partir du nuanceur, utilisez l' \_ indicateur D3D10 SVF \_ used de la \_ variable de nuanceur D3D10 \_ \_ desc pour déterminer si la variable est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a41fc-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="a41fc-177">En plaçant les variables inutilisées à la fin de la mémoire tampon constante, vous pouvez lier une mémoire tampon plus petite au nuanceur qui n’utilise pas ces variables, ce qui permet d’économiser les coûts de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a41fc-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Combien puis-je améliorer la fréquence d’images si je charge uniquement les segments de mon caractère une fois par image au lieu d’une fois par passe/dessin ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-179">Vous pouvez améliorer la fréquence d’images comprise entre 8% et 50% en fonction de la quantité de données redondantes.</span><span class="sxs-lookup"><span data-stu-id="a41fc-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="a41fc-180">Dans le pire des cas, les performances ne seront pas réduites.</span><span class="sxs-lookup"><span data-stu-id="a41fc-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Combien de mémoires tampons constantes dois-je lier en même temps ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-182">Liez le nombre minimal de mémoires tampons constantes nécessaires à l’extraction de toutes vos données dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="a41fc-183">Dans un scénario réaliste, cinq est le nombre recommandé de mémoires tampons constantes à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a41fc-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="a41fc-184">Le partage de mémoires tampons constantes entre les nuanceurs (en liant le même CB aux VS et PS) peut également améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="a41fc-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Y a-t-il un coût pour la liaison de mémoires tampons constantes sans les utiliser ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-186">Oui, si vous ne prévoyez pas d’utiliser la mémoire tampon, n’appelez pas VSSetConsantBuffer ou PSSetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="a41fc-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="a41fc-187">Cette surcharge d’API supplémentaire peut être ajoutée au cours de plusieurs appels de dessin.</span><span class="sxs-lookup"><span data-stu-id="a41fc-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="a41fc-188">State</span><span class="sxs-lookup"><span data-stu-id="a41fc-188">State</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Quelle est la meilleure façon de gérer l’État dans D3D10 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-190">La meilleure solution consiste à connaître l’ensemble de votre état en amont et à créer les objets d’État en amont.</span><span class="sxs-lookup"><span data-stu-id="a41fc-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="a41fc-191">Cela signifie qu’au moment du rendu, la liaison d’État est la seule opération qui doit se produire.</span><span class="sxs-lookup"><span data-stu-id="a41fc-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="a41fc-192">D3D10 filtre également les doublons.</span><span class="sxs-lookup"><span data-stu-id="a41fc-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Mon jeu a été chargé dynamiquement ou possède du contenu généré par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="a41fc-194">Je ne peux pas charger tous mes objets d’État en amont.</span><span class="sxs-lookup"><span data-stu-id="a41fc-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="a41fc-195">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-196">Il existe deux solutions ici.</span><span class="sxs-lookup"><span data-stu-id="a41fc-196">There are two solutions here.</span></span> <span data-ttu-id="a41fc-197">La première consiste à créer des objets d’État à la volée et à laisser D3D10 filtrer les doublons.</span><span class="sxs-lookup"><span data-stu-id="a41fc-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="a41fc-198">Toutefois, cela n’est pas recommandé pour les scénarios avec de nombreuses modifications d’objets d’État par frame.</span><span class="sxs-lookup"><span data-stu-id="a41fc-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="a41fc-199">Une meilleure solution consiste à hacher les objets d’État vous-même et à créer un objet d’état uniquement s’il est introuvable dans la table de hachage.</span><span class="sxs-lookup"><span data-stu-id="a41fc-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="a41fc-200">Le raisonnement derrière l’utilisation d’une table de hachage personnalisée est qu’une application peut sélectionner un hachage rapide basé sur le scénario d’utilisation spécifique à cette application.</span><span class="sxs-lookup"><span data-stu-id="a41fc-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="a41fc-201">Par exemple, si une application modifie uniquement le rendertargetwritemask dans le BlendState et conserve toutes les autres valeurs de la même façon, l’application peut générer un hachage à partir du rendertargetwritemask au lieu de la structure entière.</span><span class="sxs-lookup"><span data-stu-id="a41fc-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>L’état de AlphaTest a disparu.</span><span class="sxs-lookup"><span data-stu-id="a41fc-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="a41fc-203">Où se trouve-t-il ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-204">AlphaTest doit maintenant avoir des performances dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="a41fc-205">Consultez l’exemple FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="a41fc-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Qu’est-il arrivé aux plans de clip utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-207">Les plans de clip utilisateur ont été déplacés dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="a41fc-208">Il existe deux façons de gérer cela.</span><span class="sxs-lookup"><span data-stu-id="a41fc-208">There are two ways to handle this.</span></span> <span data-ttu-id="a41fc-209">La première consiste à générer une sortie \_ de SV ClipDistance à partir du nuanceur de sommets ou du nuanceur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="a41fc-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="a41fc-210">L’autre option consiste à utiliser ignorer dans le nuanceur de pixels en fonction d’une valeur passée par le nuanceur de sommets ou le nuanceur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="a41fc-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="a41fc-211">Expérimentez les deux pour voir qui est plus rapide pour votre scénario particulier.</span><span class="sxs-lookup"><span data-stu-id="a41fc-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="a41fc-212">L’utilisation de SV \_ ClipDistance peut entraîner l’utilisation par le matériel d’une routine de découpage basée sur la géométrie qui peut entraîner des appels de dessin liés à la géométrie pour s’exécuter plus lentement.</span><span class="sxs-lookup"><span data-stu-id="a41fc-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="a41fc-213">De même, l’utilisation de l’opération ignorer déplace le travail vers le nuanceur de pixels, ce qui peut ralentir l’exécution des appels de dessin liés aux pixels.</span><span class="sxs-lookup"><span data-stu-id="a41fc-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Efface ne respecte pas les paramètres d’État, tels que les paramètres des rectangles ciseaux dans mon état de rastériseur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-215">Les effacs ont été séparés de l’état du pipeline.</span><span class="sxs-lookup"><span data-stu-id="a41fc-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="a41fc-216">Pour obtenir un comportement de style D3D9, émule les effaces en dessinant un quadruple écran plein écran.</span><span class="sxs-lookup"><span data-stu-id="a41fc-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Je définis mes États sur par défaut pour essayer et diagnostiquer une erreur de rendu.</span><span class="sxs-lookup"><span data-stu-id="a41fc-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="a41fc-218">À présent, mon écran affiche le noir, bien que je sache que je dessine des objets sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="a41fc-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-219">Lors de la définition de l’État sur les valeurs par défaut (NULL), assurez-vous que le SampleMask dans l’appel à OMSetBlendState n’est jamais égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a41fc-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="a41fc-220">Si SampleMask a la valeur zéro, tous les échantillons sont logiquement et avec zéro.</span><span class="sxs-lookup"><span data-stu-id="a41fc-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="a41fc-221">Dans ce scénario, aucun échantillon ne passera le test Blend.</span><span class="sxs-lookup"><span data-stu-id="a41fc-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Où l’état de D3DSAMP SRGBTEXTURE est- \_ il atteint ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-223">SRVB a été supprimé dans le cadre de l’état de l’échantillonneur et est maintenant lié au format de texture.</span><span class="sxs-lookup"><span data-stu-id="a41fc-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="a41fc-224">La liaison d’une texture sRVB aura pour résultat le même échantillonnage que celui obtenu si vous avez spécifié D3DSAMP \_ SRGBTEXTURE dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a41fc-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="a41fc-225">Formats</span><span class="sxs-lookup"><span data-stu-id="a41fc-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Quel format D3D9 correspond au format D3D10 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-227">Pour plus d’informations, consultez [considérations relatives à Direct3D 9 vers Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span><span class="sxs-lookup"><span data-stu-id="a41fc-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Qu’est-il arrivé aux formats de texture A8R8G8B8 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-229">Ils ont été dépréciés dans D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="a41fc-230">Vous pouvez resourcer vos Textures en tant que R8G8B8A8, ou vous pouvez Swizzle au chargement, ou vous pouvez Swizzle dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Comment faire utiliser des textures en palette ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-232">Placez votre palette de couleurs dans une texture ou dans une mémoire tampon constante et liez-la au pipeline.</span><span class="sxs-lookup"><span data-stu-id="a41fc-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="a41fc-233">Dans le nuanceur de pixels, effectuez une recherche indirecte à l’aide de l’index dans votre texture en palette.</span><span class="sxs-lookup"><span data-stu-id="a41fc-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Quels sont ces nouveaux formats sRVB ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-235">SRVB a été supprimé dans le cadre de l’état de l’échantillonneur et est maintenant lié au format de texture.</span><span class="sxs-lookup"><span data-stu-id="a41fc-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="a41fc-236">La liaison d’une texture sRVB aura pour résultat le même échantillonnage que celui obtenu si vous avez spécifié D3DSAMP \_ SRGBTEXTURE dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a41fc-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Où les fans de triangle ont-ils atteint ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-238">Les ventilateurs triangulaires ont été dépréciés dans D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="a41fc-239">Les ventilateurs à triangle doivent être convertis dans le pipeline de contenu ou lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="a41fc-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="a41fc-240">Liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a41fc-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Mes nuanceurs Direct3D 9 se compilent correctement avec le modèle de nuanceur 4,0, mais lorsque je les lie au pipeline, j’obtiens des erreurs de liaison qui s’affichent dans la sortie de débogage avec le runtime de débogage.</span><span class="sxs-lookup"><span data-stu-id="a41fc-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-242">La liaison de nuanceur est plus stricte dans D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="a41fc-243">Les éléments d’une étape suivante doivent être lus dans l’ordre dans lequel ils sont générés à partir de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="a41fc-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="a41fc-244">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a41fc-244">For example:</span></span>

<span data-ttu-id="a41fc-245">Un nuanceur de sommets génère :</span><span class="sxs-lookup"><span data-stu-id="a41fc-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="a41fc-246">Un nuanceur de pixels lit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a41fc-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="a41fc-247">Même si la position n’est pas nécessaire dans le nuanceur de pixels, cela provoque une erreur de liaison, car la position est la sortie du nuanceur de sommets, mais elle n’est pas lue par le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a41fc-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="a41fc-248">La version la plus correcte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="a41fc-248">The more correct version would look like this:</span></span>

<span data-ttu-id="a41fc-249">Un nuanceur de sommets génère :</span><span class="sxs-lookup"><span data-stu-id="a41fc-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="a41fc-250">Un nuanceur de pixels lit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a41fc-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="a41fc-251">Dans ce cas, le nuanceur de sommets génère les mêmes informations, mais maintenant le nuanceur de pixels lit les éléments dans la sortie de commande.</span><span class="sxs-lookup"><span data-stu-id="a41fc-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="a41fc-252">Étant donné que le nuanceur de pixels ne lit rien après Tex, nous n’avons pas à vous soucier de la génération d’informations supplémentaires par rapport à la lecture de PS.</span><span class="sxs-lookup"><span data-stu-id="a41fc-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>J’ai besoin d’une signature de nuanceur pour créer une disposition d’entrée, mais je charge mes maillages et je crée des dispositions avant de créer des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="a41fc-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="a41fc-254">Que faire ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-255">Une solution consiste à changer l’ordre et à charger les nuanceurs avant de charger les maillages.</span><span class="sxs-lookup"><span data-stu-id="a41fc-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="a41fc-256">Toutefois, c’est beaucoup plus facile à dire qu’à faire.</span><span class="sxs-lookup"><span data-stu-id="a41fc-256">However, this is much easier said than done.</span></span> <span data-ttu-id="a41fc-257">Vous pouvez toujours créer les dispositions d’entrée à la demande lorsque l’application l’exige.</span><span class="sxs-lookup"><span data-stu-id="a41fc-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="a41fc-258">Vous devez conserver une version de la signature du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="a41fc-259">Vous devez créer un hachage basé sur la disposition du nuanceur et de la mémoire tampon, et créer uniquement la disposition d’entrée si celle qui correspond n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="a41fc-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="a41fc-260">Appels de dessin</span><span class="sxs-lookup"><span data-stu-id="a41fc-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Quelle est la limite des appels de dessin pour D3D10 pour atteindre 60 Hz ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="a41fc-262">30 Hz ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-263">Direct3D 9 avait une limitation du nombre d’appels de dessin en raison du coût de l’UC par appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="a41fc-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="a41fc-264">Sur Direct3D 10, le coût de chaque appel de dessin a été réduit.</span><span class="sxs-lookup"><span data-stu-id="a41fc-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="a41fc-265">Toutefois, il n’existe plus de corrélation définie entre les appels de dessin et les fréquences d’images.</span><span class="sxs-lookup"><span data-stu-id="a41fc-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="a41fc-266">Étant donné que les appels de dessin requièrent souvent de nombreux appels de support (mises à jour de tampon constantes, liaisons de texture, paramètres d’État, etc.), l’impact sur la fréquence de trame de l’API est désormais plus dépendant de l’utilisation globale de l’API, contrairement au simple dessin des nombres d’appels.</span><span class="sxs-lookup"><span data-stu-id="a41fc-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="a41fc-267">Ressources</span><span class="sxs-lookup"><span data-stu-id="a41fc-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Quel type d’utilisation de ressource dois-je utiliser pour quelles opérations ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-269">Utilisez la feuille de triche suivante :</span><span class="sxs-lookup"><span data-stu-id="a41fc-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="a41fc-270">L’UC met à jour la ressource plusieurs fois par image : D3D10 \_ utilisation \_ dynamique</span><span class="sxs-lookup"><span data-stu-id="a41fc-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="a41fc-271">L’UC met à jour la ressource moins d’une fois par Frame : D3D10 \_ usage \_ default</span><span class="sxs-lookup"><span data-stu-id="a41fc-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="a41fc-272">L’UC ne met pas à jour la ressource : utilisation de D3D10 \_ \_ immuable</span><span class="sxs-lookup"><span data-stu-id="a41fc-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="a41fc-273">L’UC doit lire la ressource : D3D10 \_ usage \_ Staging</span><span class="sxs-lookup"><span data-stu-id="a41fc-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="a41fc-274">Étant donné que les mémoires tampons constantes sont toujours censées être mises à jour fréquemment, elles ne sont pas conformes à la « feuille de triche ».</span><span class="sxs-lookup"><span data-stu-id="a41fc-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="a41fc-275">Pour connaître les types de ressources à utiliser pour les mémoires tampons constantes, consultez la section [mémoires tampons constantes](#constant-buffers) .</span><span class="sxs-lookup"><span data-stu-id="a41fc-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Qu’est-il arrivé à DrawPrimitiveUP et DrawIndexedPrimitiveUP ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-277">Ils sont abD3D10s.</span><span class="sxs-lookup"><span data-stu-id="a41fc-277">They are gone in D3D10.</span></span> <span data-ttu-id="a41fc-278">Pour une géométrie dynamique, utilisez une \_ mémoire tampon dynamique de grande utilisation D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="a41fc-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="a41fc-279">Au début du frame, mappez-le avec D3D10 \_ carte d' \_ écriture \_ ignorée.</span><span class="sxs-lookup"><span data-stu-id="a41fc-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="a41fc-280">Pour chaque appel de dessin suivant avance le pointeur d’écriture au-delà de la position des vertex précédemment dessinés et mappez la mémoire tampon avec la carte de D3D10 \_ \_ \_ n’écrire aucun remplacement \_ .</span><span class="sxs-lookup"><span data-stu-id="a41fc-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="a41fc-281">Si vous approchez de la fin de la mémoire tampon avant la fin du frame, encapsulez le pointeur d’écriture au début et mappez avec D3D10 \_ carte d' \_ écriture \_ ignorée.</span><span class="sxs-lookup"><span data-stu-id="a41fc-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Puis-je écrire des index 16 bits et des index 32 bits dans la même mémoire tampon de géométrie dynamique ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-283">Oui, vous pouvez, mais cela peut entraîner une baisse des performances sur un certain matériel.</span><span class="sxs-lookup"><span data-stu-id="a41fc-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="a41fc-284">Il est plus sûr de créer des mémoires tampons distinctes pour les données d’index 16 bits dynamiques et les données d’index 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a41fc-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Comment faire lire les données du GPU vers le processeur ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-286">Vous devez utiliser une ressource intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="a41fc-286">You must use a staging resource.</span></span> <span data-ttu-id="a41fc-287">Copiez les données de la ressource GPU vers la ressource intermédiaire à l’aide de CopyResource.</span><span class="sxs-lookup"><span data-stu-id="a41fc-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="a41fc-288">Mappez la ressource intermédiaire pour lire les données.</span><span class="sxs-lookup"><span data-stu-id="a41fc-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Mon application dépend de la fonctionnalité StretchRect.</span><span class="sxs-lookup"><span data-stu-id="a41fc-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-290">Comme il s’agissait essentiellement d’un wrapper pour la fonctionnalité Direct3D de base, il a été supprimé de l’API.</span><span class="sxs-lookup"><span data-stu-id="a41fc-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="a41fc-291">Certaines fonctionnalités de StretchRect ont été déplacées dans D3DX10LoadTextureFromTexture.</span><span class="sxs-lookup"><span data-stu-id="a41fc-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="a41fc-292">Pour les conversions de format et la copie des textures, D3DX10LoadTextureFromTexture peut effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="a41fc-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="a41fc-293">Toutefois, les opérations telles que la conversion d’une taille à une autre peuvent nécessiter un rendu pour une opération de texture dans l’application.</span><span class="sxs-lookup"><span data-stu-id="a41fc-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Il n’existe aucun décalage ni aucune taille sur les appels de carte pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="a41fc-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="a41fc-295">Ils se trouvaient sur des appels de verrou sur Direct3D 9 ; Pourquoi a-t-il changé ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-296">Les décalages et les tailles sur les appels de verrou sur Direct3D 9 étaient l’encombrement de l’API et sont souvent ignorés par le pilote.</span><span class="sxs-lookup"><span data-stu-id="a41fc-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="a41fc-297">Les décalages doivent être calculés à la place de l’application à partir du pointeur retourné dans l’appel de carte.</span><span class="sxs-lookup"><span data-stu-id="a41fc-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="a41fc-298">Profondeur comme texture</span><span class="sxs-lookup"><span data-stu-id="a41fc-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Qui est plus rapide ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="a41fc-300">Vous utilisez la profondeur comme une texture ou une profondeur d’écriture dans alpha et que vous lisez ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-301">Il s’agit d’une application et d’un matériel spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a41fc-301">This is application and hardware specific.</span></span> <span data-ttu-id="a41fc-302">Utilisez celui qui économise le plus de bande passante.</span><span class="sxs-lookup"><span data-stu-id="a41fc-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="a41fc-303">Si vous utilisez déjà plusieurs cibles de rendu et que vous avez un canal supplémentaire, l’écriture de profondeur à partir du nuanceur peut être une meilleure solution.</span><span class="sxs-lookup"><span data-stu-id="a41fc-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="a41fc-304">En outre, l’écriture de profondeur dans alpha ou une autre cible de rendu vous permet d’écrire des valeurs de profondeur linéaire qui peuvent accélérer les calculs qui doivent accéder à la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>PUIS-je avoir une texture liée en tant qu’entrée et être liée comme une texture de stencil de profondeur tant que je désactive les écritures de profondeur ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-306">Pas dans D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="a41fc-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="a41fc-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Puis-je résoudre une texture de stencil de profondeur MSAA ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-309">Pas dans D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-309">Not in D3D10.</span></span> <span data-ttu-id="a41fc-310">Toutefois, vous pouvez échantillonner des échantillons individuels à partir de la texture MSAA.</span><span class="sxs-lookup"><span data-stu-id="a41fc-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="a41fc-311">Pour plus d’informations, consultez la section [HLSL](#hlsl) .</span><span class="sxs-lookup"><span data-stu-id="a41fc-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Pourquoi mon application se bloque-t-elle dès que j’active MSAA ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-313">Veillez à activer un nombre d’échantillons MSAA et un numéro de qualité qui sont réellement énumérés par le pilote.</span><span class="sxs-lookup"><span data-stu-id="a41fc-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="a41fc-314">Crashes</span><span class="sxs-lookup"><span data-stu-id="a41fc-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Mon application se bloque dans D3D10 ou dans le pilote et je ne sais pas pourquoi.</span><span class="sxs-lookup"><span data-stu-id="a41fc-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-316">La première étape consiste à activer le runtime de débogage (D3D10 créer l’indicateur de [**\_ \_ \_ débogage**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) de l’appareil passé dans [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="a41fc-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="a41fc-317">Cela exposera les erreurs les plus courantes comme sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="a41fc-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX se bloque lorsque j’essaie d’utiliser mon application avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="a41fc-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-319">La première étape consiste à activer le runtime de débogage (D3D10 créer l’indicateur de [**\_ \_ \_ débogage**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) de l’appareil passé dans [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="a41fc-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="a41fc-320">PIX a une probabilité plus élevée de blocage si la sortie de débogage n’est pas propre.</span><span class="sxs-lookup"><span data-stu-id="a41fc-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Mon jeu ne dispose plus de suffisamment d’espace d’adressage virtuel sur Vista 32 bits sous D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="a41fc-322">Il n’y a aucun problème sur D3D9.</span><span class="sxs-lookup"><span data-stu-id="a41fc-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-323">Certains problèmes se sont produits avec D3D10 et l’espace d’adressage virtuel.</span><span class="sxs-lookup"><span data-stu-id="a41fc-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="a41fc-324">Ce problème a été résolu dans [KB940105](https://support.microsoft.com/kb/940105).</span><span class="sxs-lookup"><span data-stu-id="a41fc-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="a41fc-325">Si cela ne résout pas votre problème, assurez-vous de ne pas créer plus de ressources qui peuvent être mappées (verrouillées) dans D3D10 que dans D3D9.</span><span class="sxs-lookup"><span data-stu-id="a41fc-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="a41fc-326">Pensez également au portage vers 64 bits, car cela deviendra plus répandu à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="a41fc-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="a41fc-327">Rendu prédicat</span><span class="sxs-lookup"><span data-stu-id="a41fc-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>J’ai utilisé le rendu prédicat (en fonction des résultats d’une requête d’occlusion).</span><span class="sxs-lookup"><span data-stu-id="a41fc-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="a41fc-329">Pourquoi mon application a-t-elle toujours la même vitesse ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-330">Tout d’abord, assurez-vous que le rendu que vous souhaitez ignorer est en fait le goulot d’étranglement de l’application.</span><span class="sxs-lookup"><span data-stu-id="a41fc-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="a41fc-331">S’il ne s’agit pas du goulot d’étranglement, le fait d’ignorer le rendu ne permet pas d’obtenir une fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="a41fc-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="a41fc-332">Ensuite, assurez-vous que suffisamment de temps s’est écoulé entre le problème de la requête et du rendu que vous souhaitez définir comme prédicat.</span><span class="sxs-lookup"><span data-stu-id="a41fc-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="a41fc-333">Si la requête n’est pas terminée au moment où l’appel de rendu atteint le GPU, le rendu se produit tout de même.</span><span class="sxs-lookup"><span data-stu-id="a41fc-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="a41fc-334">Troisièmement, le prédicat ignore uniquement certains appels.</span><span class="sxs-lookup"><span data-stu-id="a41fc-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="a41fc-335">Les appels ignorés sont dessiner, effacer, copier, mettre à jour, ResolveSubresource et GenerateMips.</span><span class="sxs-lookup"><span data-stu-id="a41fc-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="a41fc-336">Le paramètre d’État, le programme d’installation d’IA, le mappage et les appels de création ne respectent pas la prédicat.</span><span class="sxs-lookup"><span data-stu-id="a41fc-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="a41fc-337">Si un grand nombre d’appels de paramètres d’État autour de l’appel de dessin doivent être prédicats, ces États sont toujours définis.</span><span class="sxs-lookup"><span data-stu-id="a41fc-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="a41fc-338">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="a41fc-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Dois-je utiliser le nuanceur Geometry pour paver mon (insérer quoi que ce soit ici) ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-340">Non.</span><span class="sxs-lookup"><span data-stu-id="a41fc-340">No.</span></span> <span data-ttu-id="a41fc-341">Le nuanceur Geometry ne doit pas être utilisé pour le pavage.</span><span class="sxs-lookup"><span data-stu-id="a41fc-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Puis-je utiliser le nuanceur Geometry pour créer une géométrie ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-343">Oui, dans des scénarios très limités.</span><span class="sxs-lookup"><span data-stu-id="a41fc-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="a41fc-344">Le nuanceur Geometry des parties D3D10 actuelles (2008) n’est pas conçu pour gérer une grande expansion.</span><span class="sxs-lookup"><span data-stu-id="a41fc-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="a41fc-345">Cela peut changer à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="a41fc-345">This may change in the future.</span></span> <span data-ttu-id="a41fc-346">Les fournisseurs de cartes vidéo peuvent avoir un chemin d’accès spécial pour quatre expansions en raison d’un matériel de point-Sprite existant.</span><span class="sxs-lookup"><span data-stu-id="a41fc-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="a41fc-347">Toute autre expansion devrait être très limitée.</span><span class="sxs-lookup"><span data-stu-id="a41fc-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="a41fc-348">Les exemples ParticlesGS et PipesGS permettent d’obtenir des fréquences d’images élevées en n’ayant qu’une expansion limitée.</span><span class="sxs-lookup"><span data-stu-id="a41fc-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="a41fc-349">Seuls quelques points sont développés par frame.</span><span class="sxs-lookup"><span data-stu-id="a41fc-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>À quoi dois-je utiliser le nuanceur Geometry ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-351">Tout ce qui nécessite des opérations sur une primitive entière, comme la détection silhouette, les coordonnées Barycentric, etc.</span><span class="sxs-lookup"><span data-stu-id="a41fc-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="a41fc-352">Vous pouvez également l’utiliser pour sélectionner le secteur d’un tableau cible de rendu auquel envoyer les primitives.</span><span class="sxs-lookup"><span data-stu-id="a41fc-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Puis-je générer des quantités variables de géométrie à partir du nuanceur Geometry ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-354">Oui, mais cela peut entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="a41fc-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="a41fc-355">Prenons l’exemple de la génération d’un point 1 pour un appel et de 4 points pour un autre.</span><span class="sxs-lookup"><span data-stu-id="a41fc-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="a41fc-356">En cas de montage dans les règles de développement, cela peut entraîner l’exécution en série des threads du nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="a41fc-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Comment D3D10 sait-il comment générer des index d’adjacence pour ma maille ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="a41fc-358">Ou bien, pourquoi D3D10 ne s’affiche pas correctement lorsque je spécifie que le nuanceur Geometry a besoin d’informations d’adjacence.</span><span class="sxs-lookup"><span data-stu-id="a41fc-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-359">Les informations d’adjacence ne sont pas créées par D3D10, mais par l’application.</span><span class="sxs-lookup"><span data-stu-id="a41fc-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="a41fc-360">Les index d’adjacence sont générés par l’application et doivent contenir six index par primitive ; Parmi les six, les index impairs sont les vertex adjacents du bord.</span><span class="sxs-lookup"><span data-stu-id="a41fc-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="a41fc-361">ID3DX10Mesh :: GenerateAdjacencyAndPointsReps peut être utilisé pour générer ces données.</span><span class="sxs-lookup"><span data-stu-id="a41fc-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="a41fc-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="a41fc-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="a41fc-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Les instructions d’entiers et de bits sont-elles lentes ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-364">Ils peuvent être.</span><span class="sxs-lookup"><span data-stu-id="a41fc-364">They can be.</span></span> <span data-ttu-id="a41fc-365">Diverses cartes D3D10 peuvent uniquement être en mesure d’émettre des opérations d’entiers sur un sous-ensemble des unités ALU disponibles.</span><span class="sxs-lookup"><span data-stu-id="a41fc-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="a41fc-366">Cela dépend fortement du matériel.</span><span class="sxs-lookup"><span data-stu-id="a41fc-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="a41fc-367">Pour obtenir des recommandations sur la façon d’effectuer des opérations sur les entiers sur ce matériel particulier, consultez le fournisseur de votre matériel.</span><span class="sxs-lookup"><span data-stu-id="a41fc-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="a41fc-368">En outre, veillez à effectuer des casts entre les types.</span><span class="sxs-lookup"><span data-stu-id="a41fc-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Qu’est-il arrivé à VPOS ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-370">Si vous déclarez une entrée à votre nuanceur de pixels comme position de SV \_ , vous obtiendrez le même comportement que le déclarer comme VPOS.</span><span class="sxs-lookup"><span data-stu-id="a41fc-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Comment faire un exemple de texture MSAA ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-372">Dans votre nuanceur, déclarez votre texture comme Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="a41fc-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="a41fc-373">Vous pouvez ensuite extraire des exemples individuels à l’aide des exemples de méthodes de l’objet Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="a41fc-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Comment faire indiquer si une variable de nuanceur dans une mémoire tampon constante est réellement utilisée ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-375">Examinez le \_ \_ struct Description variable de nuanceur D3D10 réfléchi \_ pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="a41fc-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="a41fc-376">uFlags doit avoir l' \_ indicateur D3D10 SVF \_ utilisé défini.</span><span class="sxs-lookup"><span data-stu-id="a41fc-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Comment faire indiquer si une variable de nuanceur dans une mémoire tampon constante utilise réellement FX10 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-378">Cela n’est pas possible actuellement avec FX10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Je n’ai aucun contrôle sur les mémoires tampons constantes créées par FX10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="a41fc-380">Comment sont-ils créés et mis à jour ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-381">Toutes les mémoires tampons constantes gérées par FX10 sont créées en tant que \_ \_ ressources par défaut d’utilisation D3D10 et sont mises à jour à l’aide de UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="a41fc-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="a41fc-382">Étant donné que FX10 conserve un magasin de stockage de toutes les données constantes, UpdateSubresource est la meilleure approche pour les mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="a41fc-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Comment faire émuler le pipeline de fonction fixe à l’aide de nuanceurs ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-384">Consultez l’exemple FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="a41fc-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Dois-je utiliser les nouveaux \[ \] indicateurs de compilation, de boucle, de \[ \] \[ branche \] , etc. ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-386">En général, non.</span><span class="sxs-lookup"><span data-stu-id="a41fc-386">In general, no.</span></span> <span data-ttu-id="a41fc-387">Le compilateur essaiera souvent les deux façons et choisissez le plus rapide.</span><span class="sxs-lookup"><span data-stu-id="a41fc-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="a41fc-388">Dans certains cas, il peut être nécessaire d’utiliser la \[ désroll \] , par exemple, lorsqu’une extraction de texture à l’intérieur d’une boucle a besoin d’accéder à un dégradé.</span><span class="sxs-lookup"><span data-stu-id="a41fc-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>La précision partielle fait-elle une différence sur les D3D10 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="a41fc-390">Je peux spécifier une précision partielle dans mon D3D9 HLSL, mais pas dans mon D3D10 HLSL.</span><span class="sxs-lookup"><span data-stu-id="a41fc-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-391">Toutes les opérations D3D10 sont spécifiées pour s’exécuter à la précision à virgule flottante 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a41fc-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="a41fc-392">Par conséquent, la précision partielle ne doit pas faire de différence dans D3D10.</span><span class="sxs-lookup"><span data-stu-id="a41fc-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>Dans D3D9, il serait possible de procéder à un filtrage instantané PCF en liant une mémoire tampon de profondeur comme texture et en utilisant les instructions standard tex2d HLSL.</span><span class="sxs-lookup"><span data-stu-id="a41fc-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="a41fc-394">Comment faire le faire sur D3D10 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-395">Vous devez utiliser un état d’échantillonnage de comparaison et utiliser des instructions SampleCmp.</span><span class="sxs-lookup"><span data-stu-id="a41fc-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Comment ce mot clé Register fonctionne-t-il dans D3D10 ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-397">Le mot clé Register dans D3D10 s’applique désormais à l’emplacement auquel une ressource particulière est liée.</span><span class="sxs-lookup"><span data-stu-id="a41fc-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="a41fc-398">Dans ce cas, la ressource peut être une mémoire tampon (constante ou autre), une texture ou un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a41fc-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="a41fc-399">Pour les mémoires tampons constantes, utilisez la syntaxe suivante : Register (-), où N est l’emplacement d’entrée (0-15)</span><span class="sxs-lookup"><span data-stu-id="a41fc-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="a41fc-400">Pour les textures, utilisez la syntaxe : Register (tN), où N est l’emplacement d’entrée (0-127)</span><span class="sxs-lookup"><span data-stu-id="a41fc-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="a41fc-401">Pour les échantillonneurs, utilisez la syntaxe suivante : Register (sN), où N est l’emplacement d’entrée (0-127)</span><span class="sxs-lookup"><span data-stu-id="a41fc-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="a41fc-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Comment faire placer une variable à l’intérieur d’une mémoire tampon constante si le Registre est simplement utilisé pour spécifier l’emplacement de la liaison de la mémoire tampon entière ?</span><span class="sxs-lookup"><span data-stu-id="a41fc-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="a41fc-403">Utilisez le mot clé packoffset.</span><span class="sxs-lookup"><span data-stu-id="a41fc-403">Use the packoffset keyword.</span></span> <span data-ttu-id="a41fc-404">L’argument de packoffset se présente sous la forme c \[ 0-4095 \] . \[ x, y, z, w \] .</span><span class="sxs-lookup"><span data-stu-id="a41fc-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="a41fc-405">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a41fc-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="a41fc-406">Dans ce tampon de constante, IWaste2Floats est placé au troisième float (douzième octet) dans la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="a41fc-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="a41fc-407">IWasteMore est placé au 13e float4 ou 52nd float dans la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="a41fc-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 