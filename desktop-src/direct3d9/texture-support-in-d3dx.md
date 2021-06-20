---
description: En savoir plus sur la prise en charge de la texture dans D3DX. D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Prise en charge de la texture dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404602"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="1aaae-105">Prise en charge de la texture dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aaae-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="1aaae-106">D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance.</span><span class="sxs-lookup"><span data-stu-id="1aaae-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="1aaae-107">Il s’agit d’une couche au-dessus du composant Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1aaae-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="1aaae-108">Textures</span><span class="sxs-lookup"><span data-stu-id="1aaae-108">Textures</span></span>

<span data-ttu-id="1aaae-109">De nombreuses textures différentes sont prises en charge dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="1aaae-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="1aaae-110">Prise en charge standard de la texture mipmapped.</span><span class="sxs-lookup"><span data-stu-id="1aaae-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="1aaae-111">Voir [génération automatique de des mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="1aaae-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="1aaae-112">Prise en charge du mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="1aaae-112">Cube map support.</span></span> <span data-ttu-id="1aaae-113">Consultez [mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="1aaae-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="1aaae-114">Prise en charge de la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="1aaae-114">Volume texture support.</span></span> <span data-ttu-id="1aaae-115">Consultez [ressources de texture de volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="1aaae-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="1aaae-116">Prise en charge du mappage d’environnement.</span><span class="sxs-lookup"><span data-stu-id="1aaae-116">Environment mapping support.</span></span> <span data-ttu-id="1aaae-117">Voir [mappage d’environnement (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="1aaae-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="1aaae-118">Prise en charge du mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="1aaae-118">Bump mapping support.</span></span> <span data-ttu-id="1aaae-119">Voir placage [de relief (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="1aaae-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="1aaae-120">Conversion de couleur de texture</span><span class="sxs-lookup"><span data-stu-id="1aaae-120">Texture Color Conversion</span></span>

<span data-ttu-id="1aaae-121">Lorsque vous utilisez l’une des fonctions D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, la conversion des couleurs devra peut-être être effectuée.</span><span class="sxs-lookup"><span data-stu-id="1aaae-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="1aaae-122">Par exemple, une surface peut être de type RVBA et l’autre peut être UVWQ.</span><span class="sxs-lookup"><span data-stu-id="1aaae-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="1aaae-123">Pour les cas de formats différents, la séquence de conversion est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1aaae-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="1aaae-124">Mappage de RVBA à UVWQ</span><span class="sxs-lookup"><span data-stu-id="1aaae-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="1aaae-125">R <-> U, le canal R est mappé au canal U, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="1aaae-126">G <-> V, le canal G est mappé au canal V, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="1aaae-127">B <-> W, le canal B est mappé au canal W, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="1aaae-128">Une < > Q/L, un canal est mappé au canal Q ou L (en fonction de celui qui est disponible dans le format de destination), ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="1aaae-129">Mappage de l’UV au RVBA</span><span class="sxs-lookup"><span data-stu-id="1aaae-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="1aaae-130">U <-> R, le canal U est mappé au canal R, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="1aaae-131">V <-> G, le canal V est mappé au canal G, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="1aaae-132">1 <-> B, 1 est mappé au canal B, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="1aaae-133">1 <-> A, 1 est mappé au canal A, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1aaae-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="1aaae-134">Si un canal n’existe pas dans la source, il est supposé être 1 (à l’exception de A8, où R, G, B sont supposés être 0).</span><span class="sxs-lookup"><span data-stu-id="1aaae-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="1aaae-135">Exemple :</span><span class="sxs-lookup"><span data-stu-id="1aaae-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="1aaae-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1aaae-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aaae-137">D3DX</span><span class="sxs-lookup"><span data-stu-id="1aaae-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



