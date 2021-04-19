---
description: D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Prise en charge de la texture dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517144"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="7c94e-104">Prise en charge de la texture dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c94e-104">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="7c94e-105">D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance.</span><span class="sxs-lookup"><span data-stu-id="7c94e-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="7c94e-106">Il s’agit d’une couche au-dessus du composant Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7c94e-106">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="7c94e-107">Textures</span><span class="sxs-lookup"><span data-stu-id="7c94e-107">Textures</span></span>

<span data-ttu-id="7c94e-108">De nombreuses textures différentes sont prises en charge dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c94e-108">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="7c94e-109">Prise en charge standard de la texture mipmapped.</span><span class="sxs-lookup"><span data-stu-id="7c94e-109">Standard mipmapped texture support.</span></span> <span data-ttu-id="7c94e-110">Voir [génération automatique de des mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="7c94e-110">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="7c94e-111">Prise en charge du mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="7c94e-111">Cube map support.</span></span> <span data-ttu-id="7c94e-112">Consultez [mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="7c94e-112">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="7c94e-113">Prise en charge de la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="7c94e-113">Volume texture support.</span></span> <span data-ttu-id="7c94e-114">Consultez [ressources de texture de volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7c94e-114">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="7c94e-115">Prise en charge du mappage d’environnement.</span><span class="sxs-lookup"><span data-stu-id="7c94e-115">Environment mapping support.</span></span> <span data-ttu-id="7c94e-116">Voir [mappage d’environnement (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="7c94e-116">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="7c94e-117">Prise en charge du mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="7c94e-117">Bump mapping support.</span></span> <span data-ttu-id="7c94e-118">Voir placage [de relief (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="7c94e-118">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="7c94e-119">Conversion de couleur de texture</span><span class="sxs-lookup"><span data-stu-id="7c94e-119">Texture Color Conversion</span></span>

<span data-ttu-id="7c94e-120">Lorsque vous utilisez l’une des fonctions D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, la conversion des couleurs devra peut-être être effectuée.</span><span class="sxs-lookup"><span data-stu-id="7c94e-120">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="7c94e-121">Par exemple, une surface peut être de type RVBA et l’autre peut être UVWQ.</span><span class="sxs-lookup"><span data-stu-id="7c94e-121">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="7c94e-122">Pour les cas de formats différents, la séquence de conversion est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7c94e-122">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="7c94e-123">Mappage de RVBA à UVWQ</span><span class="sxs-lookup"><span data-stu-id="7c94e-123">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="7c94e-124">R <-> U, le canal R est mappé au canal U, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-124">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="7c94e-125">G <-> V, le canal G est mappé au canal V, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-125">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="7c94e-126">B <-> W, le canal B est mappé au canal W, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-126">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="7c94e-127">Une < > Q/L, un canal est mappé au canal Q ou L (en fonction de celui qui est disponible dans le format de destination), ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-127">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="7c94e-128">Mappage de l’UV au RVBA</span><span class="sxs-lookup"><span data-stu-id="7c94e-128">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="7c94e-129">U <-> R, le canal U est mappé au canal R, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-129">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="7c94e-130">V <-> G, le canal V est mappé au canal G, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-130">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="7c94e-131">1 <-> B, 1 est mappé au canal B, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-131">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="7c94e-132">1 <-> A, 1 est mappé au canal A, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="7c94e-132">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="7c94e-133">Si un canal n’existe pas dans la source, il est supposé être 1 (à l’exception de A8, où R, G, B sont supposés être 0).</span><span class="sxs-lookup"><span data-stu-id="7c94e-133">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="7c94e-134">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7c94e-134">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="7c94e-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c94e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c94e-136">D3DX</span><span class="sxs-lookup"><span data-stu-id="7c94e-136">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



