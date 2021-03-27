---
title: Registre de position
description: Ce registre de sortie du nuanceur de vertex contient des données de position par vertex.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673590"
---
# <a name="position-register"></a><span data-ttu-id="ff760-103">Registre de position</span><span class="sxs-lookup"><span data-stu-id="ff760-103">Position Register</span></span>

<span data-ttu-id="ff760-104">Ce registre de sortie du nuanceur de vertex contient des données de position par vertex.</span><span class="sxs-lookup"><span data-stu-id="ff760-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="ff760-105">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="ff760-105">Vertex shader versions</span></span> | <span data-ttu-id="ff760-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="ff760-106">1\_1</span></span> | <span data-ttu-id="ff760-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff760-107">2\_0</span></span> | <span data-ttu-id="ff760-108">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ff760-108">2\_sw</span></span> | <span data-ttu-id="ff760-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ff760-109">2\_x</span></span> | <span data-ttu-id="ff760-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff760-110">3\_0</span></span> | <span data-ttu-id="ff760-111">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ff760-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="ff760-112">Registre de position</span><span class="sxs-lookup"><span data-stu-id="ff760-112">Position Register</span></span>      | <span data-ttu-id="ff760-113">x</span><span class="sxs-lookup"><span data-stu-id="ff760-113">x</span></span>    | <span data-ttu-id="ff760-114">x</span><span class="sxs-lookup"><span data-stu-id="ff760-114">x</span></span>    | <span data-ttu-id="ff760-115">x</span><span class="sxs-lookup"><span data-stu-id="ff760-115">x</span></span>     | <span data-ttu-id="ff760-116">x</span><span class="sxs-lookup"><span data-stu-id="ff760-116">x</span></span>    | <span data-ttu-id="ff760-117">x</span><span class="sxs-lookup"><span data-stu-id="ff760-117">x</span></span>    | <span data-ttu-id="ff760-118">x</span><span class="sxs-lookup"><span data-stu-id="ff760-118">x</span></span>     |



 

<span data-ttu-id="ff760-119">Un registre se compose de propriétés qui déterminent le comportement de chaque registre.</span><span class="sxs-lookup"><span data-stu-id="ff760-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="ff760-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="ff760-120">Property</span></span>        | <span data-ttu-id="ff760-121">Description</span><span class="sxs-lookup"><span data-stu-id="ff760-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="ff760-122">Nom</span><span class="sxs-lookup"><span data-stu-id="ff760-122">Name</span></span>            | <span data-ttu-id="ff760-123">oPos</span><span class="sxs-lookup"><span data-stu-id="ff760-123">oPos</span></span>        |
| <span data-ttu-id="ff760-124">Count</span><span class="sxs-lookup"><span data-stu-id="ff760-124">Count</span></span>           | <span data-ttu-id="ff760-125">1 vecteur</span><span class="sxs-lookup"><span data-stu-id="ff760-125">1 vector</span></span>    |
| <span data-ttu-id="ff760-126">Autorisations d’e/s</span><span class="sxs-lookup"><span data-stu-id="ff760-126">I/O permissions</span></span> | <span data-ttu-id="ff760-127">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ff760-127">Write-only.</span></span> |



 

<span data-ttu-id="ff760-128">La valeur correspond à la position dans l’espace de découpage homogène.</span><span class="sxs-lookup"><span data-stu-id="ff760-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="ff760-129">Cette valeur doit être écrite par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ff760-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="ff760-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff760-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="ff760-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff760-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff760-132">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="ff760-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




