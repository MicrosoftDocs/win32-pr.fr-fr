---
description: Le mappage d’environnement est une technique qui simule des surfaces fortement réfléchissantes sans utiliser le traçage de rayon.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mappage d’environnement (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745949"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="b8f1d-103">Mappage d’environnement (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b8f1d-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="b8f1d-104">Le mappage d’environnement est une technique qui simule des surfaces fortement réfléchissantes sans utiliser le traçage de rayon.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="b8f1d-105">Dans la pratique, le mappage d’environnement applique une carte de texture spéciale qui contient une image de la scène entourant un objet à l’objet lui-même.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="b8f1d-106">Le résultat est proche de l’apparence d’une surface réfléchissante, presque suffisamment pour tromper l’oeil, sans impliquer les calculs complexes impliqués dans le traçage de rayon.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="b8f1d-107">L’illustration suivante montre un type de mappage d’environnement appelé « mappage d’environnement sphérique ».</span><span class="sxs-lookup"><span data-stu-id="b8f1d-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="b8f1d-108">Pour plus d’informations, consultez [mappage d’environnement sphérique](spherical-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="b8f1d-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![illustration d’un théière avec une texture appliquée qui reflète l’environnement](images/spheremapped-teapot.png)

<span data-ttu-id="b8f1d-110">Le théière de cette image semble refléter son environnement ; Il s’agit en fait d’une texture appliquée à l’objet.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="b8f1d-111">Étant donné que le mappage d’environnement utilise une texture combinée à des coordonnées de texture calculées, il peut être exécuté en temps réel.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="b8f1d-112">Cette section fournit des informations sur l’exécution de deux types courants de mappage d’environnement avec Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="b8f1d-113">De nombreux types de mappage d’environnement sont utilisés dans l’ensemble de l’industrie graphique, mais les rubriques suivantes ciblent les deux formes les plus courantes : le mappage d’environnement cubique et le mappage d’environnement sphérique.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="b8f1d-114">Mappage d’environnement cubique</span><span class="sxs-lookup"><span data-stu-id="b8f1d-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="b8f1d-115">Mappage d’environnement sphérique</span><span class="sxs-lookup"><span data-stu-id="b8f1d-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="b8f1d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8f1d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8f1d-117">Pipeline de pixels</span><span class="sxs-lookup"><span data-stu-id="b8f1d-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



