---
title: Mémoires tampons
description: Les mémoires tampons contiennent des données utilisées pour décrire la géométrie, les informations géométriques d’indexation et les constantes de nuanceur. Cette section décrit les mémoires tampons utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.
ms.assetid: 4ab4c9e5-9155-4bfd-b69b-40b3e8cdd4ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c544f00515f25c9c311f6c75fda109d3e88294b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310434"
---
# <a name="buffers"></a><span data-ttu-id="7345a-104">Mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="7345a-104">Buffers</span></span>

<span data-ttu-id="7345a-105">Les mémoires tampons contiennent des données utilisées pour décrire la géométrie, les informations géométriques d’indexation et les constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="7345a-105">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="7345a-106">Cette section décrit les mémoires tampons utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.</span><span class="sxs-lookup"><span data-stu-id="7345a-106">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7345a-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="7345a-107">In this section</span></span>



| <span data-ttu-id="7345a-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7345a-108">Topic</span></span>                                                                                                  | <span data-ttu-id="7345a-109">Description</span><span class="sxs-lookup"><span data-stu-id="7345a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7345a-110">Présentation des mémoires tampons dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7345a-110">Introduction to Buffers in Direct3D 11</span></span>](overviews-direct3d-11-resources-buffers-intro.md)<br/> | <span data-ttu-id="7345a-111">Une ressource de mémoire tampon est une collection de données entièrement typées regroupées en éléments.</span><span class="sxs-lookup"><span data-stu-id="7345a-111">A buffer resource is a collection of fully typed data grouped into elements.</span></span> <span data-ttu-id="7345a-112">Vous pouvez utiliser des mémoires tampons pour stocker un large éventail de données, notamment des vecteurs de position, des vecteurs normaux, des coordonnées de texture dans une mémoire tampon de vertex, des index dans une mémoire tampon d’index ou un état de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7345a-112">You can use buffers to store a wide variety of data, including position vectors, normal vectors, texture coordinates in a vertex buffer, indexes in an index buffer, or device state.</span></span> <span data-ttu-id="7345a-113">Un élément buffer est constitué de 1 à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="7345a-113">A buffer element is made up of 1 to 4 components.</span></span> <span data-ttu-id="7345a-114">Les éléments de mémoire tampon peuvent inclure des valeurs de données compressées (telles que des valeurs de surface R8G8B8A8), des entiers 8 bits uniques ou des valeurs à virgule flottante 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7345a-114">Buffer elements can include packed data values (like R8G8B8A8 surface values), single 8-bit integers, or four 32-bit floating point values.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7345a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7345a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7345a-116">Comment : créer une mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="7345a-116">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
</dt> <dt>

[<span data-ttu-id="7345a-117">Comment : créer un tampon d’index</span><span class="sxs-lookup"><span data-stu-id="7345a-117">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
</dt> <dt>

[<span data-ttu-id="7345a-118">Comment : créer une mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="7345a-118">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
</dt> <dt>

[<span data-ttu-id="7345a-119">Ressources</span><span class="sxs-lookup"><span data-stu-id="7345a-119">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





