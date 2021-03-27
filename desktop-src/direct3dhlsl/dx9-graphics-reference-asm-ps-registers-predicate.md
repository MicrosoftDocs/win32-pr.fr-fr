---
title: Registre de prédicats (référence PS HLSL)
description: Ce registre de sortie du nuanceur de pixels contient une valeur booléenne par canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679221"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="e8550-103">Registre de prédicats (référence PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8550-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="e8550-104">Ce registre de sortie du nuanceur de pixels contient une valeur booléenne par canal.</span><span class="sxs-lookup"><span data-stu-id="e8550-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="e8550-105">Un registre de prédicat est pris en charge par les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8550-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="e8550-106">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e8550-106">Pixel shader versions</span></span> | <span data-ttu-id="e8550-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="e8550-107">1\_1</span></span> | <span data-ttu-id="e8550-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="e8550-108">1\_2</span></span> | <span data-ttu-id="e8550-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e8550-109">1\_3</span></span> | <span data-ttu-id="e8550-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="e8550-110">1\_4</span></span> | <span data-ttu-id="e8550-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8550-111">2\_0</span></span> | <span data-ttu-id="e8550-112">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e8550-112">2\_sw</span></span> | <span data-ttu-id="e8550-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e8550-113">2\_x</span></span> | <span data-ttu-id="e8550-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8550-114">3\_0</span></span> | <span data-ttu-id="e8550-115">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e8550-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="e8550-116">Registre de prédicat</span><span class="sxs-lookup"><span data-stu-id="e8550-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="e8550-117">x</span><span class="sxs-lookup"><span data-stu-id="e8550-117">x</span></span>    | <span data-ttu-id="e8550-118">x</span><span class="sxs-lookup"><span data-stu-id="e8550-118">x</span></span>    | <span data-ttu-id="e8550-119">x</span><span class="sxs-lookup"><span data-stu-id="e8550-119">x</span></span>     |



 

<span data-ttu-id="e8550-120">Voici les propriétés du Registre.</span><span class="sxs-lookup"><span data-stu-id="e8550-120">Here are the register properties.</span></span>



| <span data-ttu-id="e8550-121">Type de Registre</span><span class="sxs-lookup"><span data-stu-id="e8550-121">Register type</span></span> | <span data-ttu-id="e8550-122">Count</span><span class="sxs-lookup"><span data-stu-id="e8550-122">Count</span></span> | <span data-ttu-id="e8550-123">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="e8550-123">R/W</span></span> | <span data-ttu-id="e8550-124">\# Ports de lecture</span><span class="sxs-lookup"><span data-stu-id="e8550-124">\# Read ports</span></span> | <span data-ttu-id="e8550-125">\# Lectures/inst</span><span class="sxs-lookup"><span data-stu-id="e8550-125">\# Reads/inst</span></span> | <span data-ttu-id="e8550-126">Dimension</span><span class="sxs-lookup"><span data-stu-id="e8550-126">Dimension</span></span> | <span data-ttu-id="e8550-127">RelAddr</span><span class="sxs-lookup"><span data-stu-id="e8550-127">RelAddr</span></span> | <span data-ttu-id="e8550-128">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="e8550-128">Defaults</span></span> | <span data-ttu-id="e8550-129">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8550-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="e8550-130">Prédicat (p)</span><span class="sxs-lookup"><span data-stu-id="e8550-130">Predicate(p)</span></span>  | <span data-ttu-id="e8550-131">1</span><span class="sxs-lookup"><span data-stu-id="e8550-131">1</span></span>     | <span data-ttu-id="e8550-132">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="e8550-132">R/W</span></span> | <span data-ttu-id="e8550-133">1</span><span class="sxs-lookup"><span data-stu-id="e8550-133">1</span></span>             | <span data-ttu-id="e8550-134">1</span><span class="sxs-lookup"><span data-stu-id="e8550-134">1</span></span>             | <span data-ttu-id="e8550-135">4</span><span class="sxs-lookup"><span data-stu-id="e8550-135">4</span></span>         | <span data-ttu-id="e8550-136">N/A</span><span class="sxs-lookup"><span data-stu-id="e8550-136">N/A</span></span>     | <span data-ttu-id="e8550-137">None</span><span class="sxs-lookup"><span data-stu-id="e8550-137">None</span></span>     | <span data-ttu-id="e8550-138">N</span><span class="sxs-lookup"><span data-stu-id="e8550-138">N</span></span>            |



 

<span data-ttu-id="e8550-139">Le registre de prédicat peut être modifié avec [setp \_ COMP-PS](setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="e8550-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="e8550-140">Il n’y a aucune valeur par défaut pour ce registre ; une application doit définir le registre avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="e8550-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8550-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8550-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8550-142">Inscrit</span><span class="sxs-lookup"><span data-stu-id="e8550-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




