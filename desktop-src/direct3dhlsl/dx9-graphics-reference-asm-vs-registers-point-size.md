---
title: Registre de la taille du point
description: Ce registre de sortie du nuanceur de vertex contient des données de taille de point par vertex.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379852"
---
# <a name="point-size-register"></a><span data-ttu-id="591c2-103">Registre de la taille du point</span><span class="sxs-lookup"><span data-stu-id="591c2-103">Point Size Register</span></span>

<span data-ttu-id="591c2-104">Ce registre de sortie du nuanceur de vertex contient des données de taille de point par vertex.</span><span class="sxs-lookup"><span data-stu-id="591c2-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="591c2-105">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="591c2-105">Vertex shader versions</span></span> | <span data-ttu-id="591c2-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="591c2-106">1\_1</span></span> | <span data-ttu-id="591c2-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="591c2-107">2\_0</span></span> | <span data-ttu-id="591c2-108">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="591c2-108">2\_sw</span></span> | <span data-ttu-id="591c2-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="591c2-109">2\_x</span></span> | <span data-ttu-id="591c2-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="591c2-110">3\_0</span></span> | <span data-ttu-id="591c2-111">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="591c2-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="591c2-112">Registre de la taille du point</span><span class="sxs-lookup"><span data-stu-id="591c2-112">Point Size Register</span></span>    | <span data-ttu-id="591c2-113">x</span><span class="sxs-lookup"><span data-stu-id="591c2-113">x</span></span>    | <span data-ttu-id="591c2-114">x</span><span class="sxs-lookup"><span data-stu-id="591c2-114">x</span></span>    | <span data-ttu-id="591c2-115">x</span><span class="sxs-lookup"><span data-stu-id="591c2-115">x</span></span>     | <span data-ttu-id="591c2-116">x</span><span class="sxs-lookup"><span data-stu-id="591c2-116">x</span></span>    | <span data-ttu-id="591c2-117">x</span><span class="sxs-lookup"><span data-stu-id="591c2-117">x</span></span>    | <span data-ttu-id="591c2-118">x</span><span class="sxs-lookup"><span data-stu-id="591c2-118">x</span></span>     |



 

<span data-ttu-id="591c2-119">Un registre se compose de propriétés qui déterminent le comportement de chaque registre.</span><span class="sxs-lookup"><span data-stu-id="591c2-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="591c2-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="591c2-120">Property</span></span>        | <span data-ttu-id="591c2-121">Description</span><span class="sxs-lookup"><span data-stu-id="591c2-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="591c2-122">Nom</span><span class="sxs-lookup"><span data-stu-id="591c2-122">Name</span></span>            | <span data-ttu-id="591c2-123">Décide</span><span class="sxs-lookup"><span data-stu-id="591c2-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="591c2-124">Count</span><span class="sxs-lookup"><span data-stu-id="591c2-124">Count</span></span>           | <span data-ttu-id="591c2-125">1 vecteur, dont 1 seul composant peut être utilisé et doit être spécifié par le masque de composant.</span><span class="sxs-lookup"><span data-stu-id="591c2-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="591c2-126">Autorisations d’e/s</span><span class="sxs-lookup"><span data-stu-id="591c2-126">I/O permissions</span></span> | <span data-ttu-id="591c2-127">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="591c2-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="591c2-128">Seul le composant x scalaire de la taille en points est utilisé.</span><span class="sxs-lookup"><span data-stu-id="591c2-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="591c2-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="591c2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="591c2-130">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="591c2-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




