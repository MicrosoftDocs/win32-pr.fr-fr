---
title: Exemples de signatures racines
description: La section suivante montre les signatures racines qui diffèrent en matière de complexité par rapport à la totalité de l’espace vide.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104379"
---
# <a name="example-root-signatures"></a><span data-ttu-id="5d76f-103">Exemples de signatures racines</span><span class="sxs-lookup"><span data-stu-id="5d76f-103">Example Root Signatures</span></span>

<span data-ttu-id="5d76f-104">La section suivante montre les signatures racines qui diffèrent en matière de complexité par rapport à la totalité de l’espace vide.</span><span class="sxs-lookup"><span data-stu-id="5d76f-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="5d76f-105">Signature racine vide</span><span class="sxs-lookup"><span data-stu-id="5d76f-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="5d76f-106">Une constante</span><span class="sxs-lookup"><span data-stu-id="5d76f-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="5d76f-107">Ajout d’une vue de mémoire tampon constante racine</span><span class="sxs-lookup"><span data-stu-id="5d76f-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="5d76f-108">Tables de descripteurs de liaison</span><span class="sxs-lookup"><span data-stu-id="5d76f-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="5d76f-109">Signature racine plus complexe</span><span class="sxs-lookup"><span data-stu-id="5d76f-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="5d76f-110">Affichages de ressources de nuanceur de streaming</span><span class="sxs-lookup"><span data-stu-id="5d76f-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="5d76f-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5d76f-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="5d76f-112">Signature racine vide</span><span class="sxs-lookup"><span data-stu-id="5d76f-112">An empty root signature</span></span>

![une signature racine vide n’a pas de liaisons](images/root-tables-0.png)

<span data-ttu-id="5d76f-114">Une signature racine vide est peu susceptible d’être utile, mais elle peut être utilisée dans une passe de rendu trivial avec l’utilisation de seul l’assembleur d’entrée, ainsi que des nuanceurs de vertex et de pixels minimaux qui n’accèdent à aucun descripteur.</span><span class="sxs-lookup"><span data-stu-id="5d76f-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="5d76f-115">En outre, l’étape de fusion, la cible de rendu et les étapes du stencil de profondeur sont disponibles, même avec une signature racine vide.</span><span class="sxs-lookup"><span data-stu-id="5d76f-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="5d76f-116">Une constante</span><span class="sxs-lookup"><span data-stu-id="5d76f-116">One constant</span></span>

![une seule constante racine](images/root-tables-constant.png)

<span data-ttu-id="5d76f-118">L’emplacement de liaison d’API est l’emplacement où l’argument racine de ce paramètre sera lié au moment de l’enregistrement de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="5d76f-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="5d76f-119">Le nombre d’emplacements de liaison d’API est implicite, en fonction de l’ordre des paramètres dans la signature racine (le premier est toujours zéro).</span><span class="sxs-lookup"><span data-stu-id="5d76f-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="5d76f-120">L’emplacement de liaison HLSL est l’endroit où le nuanceur verra le paramètre racine apparaître.</span><span class="sxs-lookup"><span data-stu-id="5d76f-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="5d76f-121">Le type (« uint » dans l’exemple ci-dessus) n’est pas connu du matériel, mais il s’agit simplement d’un commentaire dans l’image, le matériel verra simplement la valeur DWORD unique comme contenu.</span><span class="sxs-lookup"><span data-stu-id="5d76f-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="5d76f-122">Pour lier une constante au moment de l’enregistrement de la liste de commandes, vous devez utiliser une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="5d76f-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="5d76f-123">Ajout d’une vue de mémoire tampon constante racine</span><span class="sxs-lookup"><span data-stu-id="5d76f-123">Adding a root Constant Buffer View</span></span>

![Ajoute une vue de mémoire tampon constante à la signature racine](images/root-tables-cbv.png)

<span data-ttu-id="5d76f-125">Cet exemple montre deux constantes racine et une vue de mémoire tampon constante racine (CBV) qui coûte deux emplacements DWORD.</span><span class="sxs-lookup"><span data-stu-id="5d76f-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="5d76f-126">Pour lier une vue de mémoire tampon constante, utilisez une commande telle que la suivante.</span><span class="sxs-lookup"><span data-stu-id="5d76f-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="5d76f-127">Notez que le premier paramètre (2) est l’emplacement indiqué dans l’image.</span><span class="sxs-lookup"><span data-stu-id="5d76f-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="5d76f-128">En général, un tableau de constantes sera configuré et mis à la disposition des nuanceurs à B0 en tant que CBV.</span><span class="sxs-lookup"><span data-stu-id="5d76f-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="5d76f-129">Tables de descripteurs de liaison</span><span class="sxs-lookup"><span data-stu-id="5d76f-129">Binding descriptor tables</span></span>

![Ajoute des tables de descripteurs à la signature racine](images/root-tables-2.png)

<span data-ttu-id="5d76f-131">Cet exemple illustre l’utilisation de deux tables de descripteurs : l’un déclarant une table de cinq descripteurs qui seront disponibles au moment de l’exécution dans un \_ \_ tas de descripteur UAV SRV CBV, et un autre déclarant une table de deux descripteurs qui s’affichera au moment de l’exécution dans un tas de descripteur d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="5d76f-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="5d76f-132">Pour lier des tables de descripteurs lors de l’enregistrement d’une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="5d76f-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="5d76f-133">Une autre fonctionnalité de la signature racine est la constante racine float4 dont la taille est de quatre DWORDs.</span><span class="sxs-lookup"><span data-stu-id="5d76f-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="5d76f-134">La commande suivante lie uniquement les deux DWORDs du milieu des quatre.</span><span class="sxs-lookup"><span data-stu-id="5d76f-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="5d76f-135">Signature racine plus complexe</span><span class="sxs-lookup"><span data-stu-id="5d76f-135">A more complex root signature</span></span>

![signature racine complexe avec de nombreux éléments](images/root-tables-3.png)

<span data-ttu-id="5d76f-137">Cet exemple montre une signature racine dense avec la plupart des types d’entrées.</span><span class="sxs-lookup"><span data-stu-id="5d76f-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="5d76f-138">Deux des tables de descripteurs (aux emplacements 3 et 6) incluent des tableaux de taille illimitée.</span><span class="sxs-lookup"><span data-stu-id="5d76f-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="5d76f-139">La charge ici est que l’application ne touche que des descripteurs valides dans un segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="5d76f-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="5d76f-140">Les tableaux non limités ou très grands nécessitent un niveau matériel 2 + de la prise en charge de la liaison de ressources.</span><span class="sxs-lookup"><span data-stu-id="5d76f-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="5d76f-141">Il existe deux échantillonneurs statiques (liés sans nécessiter d’emplacements de signature racine).</span><span class="sxs-lookup"><span data-stu-id="5d76f-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="5d76f-142">À l’emplacement 9, UAV U4 et UAV U5 sont déclarés au même décalage de table de descripteur.</span><span class="sxs-lookup"><span data-stu-id="5d76f-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="5d76f-143">Ceci est l’utilisation d’un descripteur avec alias, un descripteur en mémoire s’affiche à la fois comme U4 et U5 dans les nuanceurs HLSL.</span><span class="sxs-lookup"><span data-stu-id="5d76f-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="5d76f-144">Dans ce cas, le nuanceur doit être compilé avec l' \_ option les ressources du nuanceur D3D10 peut être un \_ \_ \_ alias ou l' `/res_may_alias` option ou dans fxc.</span><span class="sxs-lookup"><span data-stu-id="5d76f-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="5d76f-145">Les descripteurs avec alias permettent à un descripteur d’être lié à plusieurs points de liaison, sans avoir à apporter de modifications aux nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="5d76f-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="5d76f-146">Affichages de ressources de nuanceur de streaming</span><span class="sxs-lookup"><span data-stu-id="5d76f-146">Streaming Shader Resource Views</span></span>

![diffusion en continu des vues de ressources de nuanceur dans cette signature racine](images/root-tables-4.png)

<span data-ttu-id="5d76f-148">Cette signature racine illustre un scénario dans lequel tous les SRVs sont diffusés dans et en dehors d’un grand tableau.</span><span class="sxs-lookup"><span data-stu-id="5d76f-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="5d76f-149">Au moment de l’exécution, une table de descripteurs peut être définie une fois lorsque la signature racine est définie.</span><span class="sxs-lookup"><span data-stu-id="5d76f-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="5d76f-150">Ensuite, toutes les lectures de texture sont effectuées en indexant dans le tableau via des constantes alimentées via les premiers arguments racine.</span><span class="sxs-lookup"><span data-stu-id="5d76f-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="5d76f-151">Un seul tas de descripteurs est nécessaire et n’est mis à jour que lorsque les textures sont diffusées en continu ou en dehors des emplacements de descripteurs libres.</span><span class="sxs-lookup"><span data-stu-id="5d76f-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="5d76f-152">Les décalages de descripteur dans le tas de grande taille sont identifiés par des nuanceurs utilisant les constantes dans les vues de mémoire tampon constantes.</span><span class="sxs-lookup"><span data-stu-id="5d76f-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="5d76f-153">Par exemple, si un nuanceur reçoit un ID de matériau, il peut indexer dans un grand tableau à l’aide de la constante pour accéder au descripteur requis (qui fait référence à la texture requise).</span><span class="sxs-lookup"><span data-stu-id="5d76f-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="5d76f-154">Ce scénario nécessite un matériel avec la liaison de ressource niveau2 +.</span><span class="sxs-lookup"><span data-stu-id="5d76f-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d76f-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5d76f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d76f-156">Couches matérielles de liaison de ressources</span><span class="sxs-lookup"><span data-stu-id="5d76f-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="5d76f-157">Liaison de ressources en HLSL</span><span class="sxs-lookup"><span data-stu-id="5d76f-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="5d76f-158">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="5d76f-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




