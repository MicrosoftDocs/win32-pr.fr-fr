---
title: Registre de coordonnées de texture (référence HLSL VS)
description: Ce registre de sortie du nuanceur de vertex contient des coordonnées de texture par vertex.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102245"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="2c099-103">Registre de coordonnées de texture (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="2c099-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="2c099-104">Ce registre de sortie du nuanceur de vertex contient des coordonnées de texture par vertex.</span><span class="sxs-lookup"><span data-stu-id="2c099-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="2c099-105">Un registre se compose de propriétés qui déterminent le comportement de chaque registre.</span><span class="sxs-lookup"><span data-stu-id="2c099-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="2c099-106">Propriété</span><span class="sxs-lookup"><span data-stu-id="2c099-106">Property</span></span>        | <span data-ttu-id="2c099-107">Description</span><span class="sxs-lookup"><span data-stu-id="2c099-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="2c099-108">Nom</span><span class="sxs-lookup"><span data-stu-id="2c099-108">Name</span></span>            | <span data-ttu-id="2c099-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="2c099-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="2c099-110">Count</span><span class="sxs-lookup"><span data-stu-id="2c099-110">Count</span></span>           | <span data-ttu-id="2c099-111">Huit vecteurs</span><span class="sxs-lookup"><span data-stu-id="2c099-111">Eight vectors</span></span> |
| <span data-ttu-id="2c099-112">Autorisations d’e/s</span><span class="sxs-lookup"><span data-stu-id="2c099-112">I/O permissions</span></span> | <span data-ttu-id="2c099-113">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="2c099-113">Write-only</span></span>    |



 

<span data-ttu-id="2c099-114">Les registres de coordonnées de texture de sortie sont un tableau de registres de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="2c099-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="2c099-115">Les données de Registre sont itérées et utilisées comme coordonnées de texture par les étapes d’échantillonnage de texture pour fournir des données au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2c099-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="2c099-116">Lors de l’écriture dans un registre de coordonnées de texture, il est recommandé de passer uniquement autant de valeurs à virgule flottante que la dimension de la carte de texture correspondante.</span><span class="sxs-lookup"><span data-stu-id="2c099-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="2c099-117">Contrôler les valeurs passées avec un modificateur.</span><span class="sxs-lookup"><span data-stu-id="2c099-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="2c099-118">Par exemple, utilisez. XY pour une carte de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="2c099-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="2c099-119">Les indicateurs de pipeline de fonction fixe, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), doivent être définis sur zéro si vous utilisez un nuanceur de sommet programmable.</span><span class="sxs-lookup"><span data-stu-id="2c099-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="2c099-120">Les données de vertex d’objet fournissent des coordonnées de texture d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2c099-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="2c099-121">Les objets qui n’utilisent pas les textures en mosaïque ont généralement des coordonnées de texture dans la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="2c099-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="2c099-122">Les objets qui utilisent des textures en mosaïque, telles que le terrain, ont généralement des coordonnées de texture comprises entre \[ -n, + n, \] où n peut être n’importe quel nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="2c099-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="2c099-123">L’interpolation de coordonnée de texture est effectuée sur les données de vertex pour la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="2c099-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="2c099-124">Pendant la pixellisation, les coordonnées de texture sont interpolées entre les vertex d’objet, modifiées par habillage de texture et mises à l’échelle par la taille de la texture (en prenant également en compte les modes d’adressage de texture) pour produire un index d’entiers.</span><span class="sxs-lookup"><span data-stu-id="2c099-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="2c099-125">L’index est ensuite utilisé pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="2c099-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="2c099-126">Utilisez la valeur MaxTextureRepeat dans [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) pour déterminer combien de fois une texture peut être affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="2c099-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="2c099-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c099-127">Example</span></span>

<span data-ttu-id="2c099-128">Déclarez le registre de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="2c099-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="2c099-129">Copiez les coordonnées de texture par vertex dans le registre de sortie.</span><span class="sxs-lookup"><span data-stu-id="2c099-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="2c099-130">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="2c099-130">Vertex shader versions</span></span>      | <span data-ttu-id="2c099-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="2c099-131">1\_1</span></span> | <span data-ttu-id="2c099-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c099-132">2\_0</span></span> | <span data-ttu-id="2c099-133">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2c099-133">2\_sw</span></span> | <span data-ttu-id="2c099-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2c099-134">2\_x</span></span> | <span data-ttu-id="2c099-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c099-135">3\_0</span></span> | <span data-ttu-id="2c099-136">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2c099-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="2c099-137">Registre de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="2c099-137">Texture Coordinate Register</span></span> | <span data-ttu-id="2c099-138">x</span><span class="sxs-lookup"><span data-stu-id="2c099-138">x</span></span>    | <span data-ttu-id="2c099-139">x</span><span class="sxs-lookup"><span data-stu-id="2c099-139">x</span></span>    | <span data-ttu-id="2c099-140">x</span><span class="sxs-lookup"><span data-stu-id="2c099-140">x</span></span>     | <span data-ttu-id="2c099-141">x</span><span class="sxs-lookup"><span data-stu-id="2c099-141">x</span></span>    | <span data-ttu-id="2c099-142">x</span><span class="sxs-lookup"><span data-stu-id="2c099-142">x</span></span>    | <span data-ttu-id="2c099-143">x</span><span class="sxs-lookup"><span data-stu-id="2c099-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="2c099-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c099-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c099-145">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="2c099-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 