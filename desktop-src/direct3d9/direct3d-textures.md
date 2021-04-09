---
description: Les textures sont un puissant outil d’amélioration du réalisme des images 3D générées par ordinateur. Direct3D prend en charge un ensemble complet de fonctionnalités de texture, ce qui permet aux développeurs d’accéder facilement à des techniques avancées d’application de textures.
ms.assetid: 48dcbc86-631e-4bc7-b809-b0e4a0a9ae8e
title: Textures Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afebd7217b36ad5f740616e198963314a1d2aca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108467"
---
# <a name="direct3d-textures-direct3d-9"></a><span data-ttu-id="3489a-104">Textures Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-104">Direct3D Textures (Direct3D 9)</span></span>

<span data-ttu-id="3489a-105">Les textures sont un puissant outil d’amélioration du réalisme des images 3D générées par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3489a-105">Textures are a powerful tool in creating realism in computer-generated 3D images.</span></span> <span data-ttu-id="3489a-106">Direct3D prend en charge un ensemble complet de fonctionnalités de texture, ce qui permet aux développeurs d’accéder facilement à des techniques avancées d’application de textures.</span><span class="sxs-lookup"><span data-stu-id="3489a-106">Direct3D supports an extensive texturing feature set, providing developers with easy access to advanced texturing techniques.</span></span>

<span data-ttu-id="3489a-107">Cette section vous aidera à commencer à utiliser des textures.</span><span class="sxs-lookup"><span data-stu-id="3489a-107">This section will get you started using textures.</span></span>

-   [<span data-ttu-id="3489a-108">Concepts de base de la texturation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-108">Basic Texturing Concepts (Direct3D 9)</span></span>](basic-texturing-concepts.md)
-   [<span data-ttu-id="3489a-109">Coordonnées de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-109">Texture Coordinates (Direct3D 9)</span></span>](texture-coordinates.md)
-   [<span data-ttu-id="3489a-110">Filtrage de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-110">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
-   [<span data-ttu-id="3489a-111">Ressources de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-111">Texture Resources (Direct3D 9)</span></span>](texture-resources.md)
-   [<span data-ttu-id="3489a-112">Habillage de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-112">Texture Wrapping (Direct3D 9)</span></span>](texture-wrapping.md)
-   [<span data-ttu-id="3489a-113">Fusion de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-113">Texture Blending (Direct3D 9)</span></span>](texture-blending.md)

<span data-ttu-id="3489a-114">Ces rubriques vont plus en détail sur les fonctionnalités de texturation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3489a-114">These topics will go into more detail about additional texturing functionality.</span></span>

-   [<span data-ttu-id="3489a-115">Génération automatique de des mipmaps (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-115">Automatic Generation of Mipmaps (Direct3D 9)</span></span>](automatic-generation-of-mipmaps.md)
-   [<span data-ttu-id="3489a-116">Gestion automatique de la texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-116">Automatic Texture Management (Direct3D 9)</span></span>](automatic-texture-management.md)
-   [<span data-ttu-id="3489a-117">Ressources de texture compressées (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-117">Compressed Texture Resources (Direct3D 9)</span></span>](compressed-texture-resources.md)
-   [<span data-ttu-id="3489a-118">Considérations matérielles relatives à la texturation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-118">Hardware Considerations for Texturing (Direct3D 9)</span></span>](hardware-considerations-for-texturing.md)
-   [<span data-ttu-id="3489a-119">Ressources de texture de volume (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3489a-119">Volume Texture Resources (Direct3D 9)</span></span>](volume-texture-resources.md)

<span data-ttu-id="3489a-120">Pour améliorer les performances, envisagez d’utiliser des textures dynamiques.</span><span class="sxs-lookup"><span data-stu-id="3489a-120">For improved performance, consider using dynamic textures.</span></span> <span data-ttu-id="3489a-121">Une texture dynamique peut être verrouillée, écrite et déverrouillée pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="3489a-121">A dynamic texture can be locked, written to, and unlocked each frame.</span></span> <span data-ttu-id="3489a-122">Consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="3489a-122">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3489a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3489a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3489a-124">Prise en main</span><span class="sxs-lookup"><span data-stu-id="3489a-124">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



