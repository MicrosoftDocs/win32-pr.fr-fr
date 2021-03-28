---
title: Fonctionnalités Direct3D 11,3
description: Les sections suivantes décrivent la fonctionnalité qui a été ajoutée dans Direct3D 11,3. Ces fonctionnalités sont également disponibles dans Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383352"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="59d7a-104">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="59d7a-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="59d7a-105">Les sections suivantes décrivent la fonctionnalité qui a été ajoutée dans Direct3D 11,3.</span><span class="sxs-lookup"><span data-stu-id="59d7a-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="59d7a-106">Ces fonctionnalités sont également disponibles dans Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="59d7a-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="59d7a-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="59d7a-107">In this section</span></span>



| <span data-ttu-id="59d7a-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="59d7a-108">Topic</span></span>                                                                                               | <span data-ttu-id="59d7a-109">Description</span><span class="sxs-lookup"><span data-stu-id="59d7a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59d7a-110">Pixellisation conservatrice</span><span class="sxs-lookup"><span data-stu-id="59d7a-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="59d7a-111">La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.</span><span class="sxs-lookup"><span data-stu-id="59d7a-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="59d7a-112">Mappage de texture par défaut</span><span class="sxs-lookup"><span data-stu-id="59d7a-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="59d7a-113">L’utilisation du mappage de texture par défaut réduit la copie et l’utilisation de la mémoire tout en partageant des données d’image entre le GPU et le processeur.</span><span class="sxs-lookup"><span data-stu-id="59d7a-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="59d7a-114">Toutefois, il ne doit être utilisé que dans des situations spécifiques.</span><span class="sxs-lookup"><span data-stu-id="59d7a-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="59d7a-115">La disposition standard Swizzle évite la copie ou la swizzling des données dans plusieurs dispositions.</span><span class="sxs-lookup"><span data-stu-id="59d7a-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="59d7a-116">Vues de l’ordre du rastériseur</span><span class="sxs-lookup"><span data-stu-id="59d7a-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="59d7a-117">Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.</span><span class="sxs-lookup"><span data-stu-id="59d7a-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="59d7a-118">Cela permet l’utilisation d’algorithmes OIT (commande Independent transparent), ce qui donne de meilleurs résultats de rendu lorsque plusieurs objets transparents sont alignés les uns avec les autres dans une vue.</span><span class="sxs-lookup"><span data-stu-id="59d7a-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="59d7a-119">Valeur de référence du stencil spécifié par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="59d7a-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="59d7a-120">L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.</span><span class="sxs-lookup"><span data-stu-id="59d7a-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="59d7a-121">Chargements de vues d’accès non ordonnées typées</span><span class="sxs-lookup"><span data-stu-id="59d7a-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="59d7a-122">Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un format DXGI spécifique \_ .</span><span class="sxs-lookup"><span data-stu-id="59d7a-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="59d7a-123">Architecture de la mémoire unifiée</span><span class="sxs-lookup"><span data-stu-id="59d7a-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="59d7a-124">L’interrogation de la prise en charge de l’architecture mémoire unifiée (UMA) peut vous aider à déterminer comment gérer certaines ressources.</span><span class="sxs-lookup"><span data-stu-id="59d7a-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="59d7a-125">Ressources en mosaïque de volume</span><span class="sxs-lookup"><span data-stu-id="59d7a-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="59d7a-126">Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="59d7a-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="59d7a-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59d7a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59d7a-128">Nouveautés de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="59d7a-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





