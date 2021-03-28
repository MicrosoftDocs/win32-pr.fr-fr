---
title: Textures
description: Cette section décrit les textures utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197090"
---
# <a name="textures"></a><span data-ttu-id="59cd5-103">Textures</span><span class="sxs-lookup"><span data-stu-id="59cd5-103">Textures</span></span>

<span data-ttu-id="59cd5-104">Une texture stocke les informations de Texel.</span><span class="sxs-lookup"><span data-stu-id="59cd5-104">A texture stores texel information.</span></span> <span data-ttu-id="59cd5-105">Cette section décrit les textures utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.</span><span class="sxs-lookup"><span data-stu-id="59cd5-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="59cd5-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="59cd5-106">In this section</span></span>



| <span data-ttu-id="59cd5-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="59cd5-107">Topic</span></span>                                                                                                    | <span data-ttu-id="59cd5-108">Description</span><span class="sxs-lookup"><span data-stu-id="59cd5-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59cd5-109">Présentation des textures dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="59cd5-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="59cd5-110">Une ressource de texture est une collection structurée de données conçue pour stocker des texels.</span><span class="sxs-lookup"><span data-stu-id="59cd5-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="59cd5-111">Un Texel représente la plus petite unité d’une texture qui peut être lue ou écrite par le pipeline.</span><span class="sxs-lookup"><span data-stu-id="59cd5-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="59cd5-112">Contrairement aux mémoires tampons, les textures peuvent être filtrées par des échantillonneurs de texture, car elles sont lues par des unités de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="59cd5-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="59cd5-113">Le type de texture affecte la manière dont la texture est filtrée.</span><span class="sxs-lookup"><span data-stu-id="59cd5-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="59cd5-114">Chaque Texel contient des composants de 1 à 4, organisés dans l’un des formats DXGI définis par l' \_ énumération de format DXGI.</span><span class="sxs-lookup"><span data-stu-id="59cd5-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="59cd5-115">Compression de bloc de texture dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="59cd5-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="59cd5-116">La prise en charge de la compression par bloc (BC) des textures a été étendue dans Direct3D 11 pour inclure les algorithmes BC6H et BC7.</span><span class="sxs-lookup"><span data-stu-id="59cd5-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="59cd5-117">BC6H prend en charge les données sources de plage haute dynamique, et BC7 fournit une compression de qualité supérieure à la moyenne avec moins d’artefacts pour les données sources RGB standard.</span><span class="sxs-lookup"><span data-stu-id="59cd5-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="59cd5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59cd5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59cd5-119">Comment : créer une texture</span><span class="sxs-lookup"><span data-stu-id="59cd5-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="59cd5-120">Comment : initialiser une texture par programmation</span><span class="sxs-lookup"><span data-stu-id="59cd5-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="59cd5-121">Comment : initialiser une texture à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="59cd5-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="59cd5-122">Ressources</span><span class="sxs-lookup"><span data-stu-id="59cd5-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





