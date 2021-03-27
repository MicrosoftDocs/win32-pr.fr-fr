---
title: Registre de brouillard
description: Ce registre de sortie du nuanceur de sommets contient une couleur de brouillard par vertex.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971423"
---
# <a name="fog-register"></a><span data-ttu-id="50fae-103">Registre de brouillard</span><span class="sxs-lookup"><span data-stu-id="50fae-103">Fog Register</span></span>

<span data-ttu-id="50fae-104">Ce registre de sortie du nuanceur de sommets contient une couleur de brouillard par vertex.</span><span class="sxs-lookup"><span data-stu-id="50fae-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="50fae-105">Un registre se compose de propriétés qui déterminent le comportement de chaque registre.</span><span class="sxs-lookup"><span data-stu-id="50fae-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="50fae-106">Propriété</span><span class="sxs-lookup"><span data-stu-id="50fae-106">Property</span></span>        | <span data-ttu-id="50fae-107">Description</span><span class="sxs-lookup"><span data-stu-id="50fae-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50fae-108">Nom</span><span class="sxs-lookup"><span data-stu-id="50fae-108">Name</span></span>            | <span data-ttu-id="50fae-109">oFog</span><span class="sxs-lookup"><span data-stu-id="50fae-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="50fae-110">Count</span><span class="sxs-lookup"><span data-stu-id="50fae-110">Count</span></span>           | <span data-ttu-id="50fae-111">Un vecteur, dont un seul composant peut être utilisé et doit être spécifié par le masque de composant</span><span class="sxs-lookup"><span data-stu-id="50fae-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="50fae-112">Autorisations d’e/s</span><span class="sxs-lookup"><span data-stu-id="50fae-112">I/O permissions</span></span> | <span data-ttu-id="50fae-113">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="50fae-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="50fae-114">La valeur de brouillard de sortie est inscrite.</span><span class="sxs-lookup"><span data-stu-id="50fae-114">The output fog value registers.</span></span> <span data-ttu-id="50fae-115">La valeur est le facteur de brouillard à interpoler, puis est routé vers la table de brouillard.</span><span class="sxs-lookup"><span data-stu-id="50fae-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="50fae-116">Seul le composant x scalaire du brouillard est utilisé.</span><span class="sxs-lookup"><span data-stu-id="50fae-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50fae-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50fae-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50fae-118">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="50fae-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




