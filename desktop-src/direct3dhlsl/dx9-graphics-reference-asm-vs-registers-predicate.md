---
title: Registre de prédicats (référence HLSL VS)
description: Ce registre de sortie du nuanceur de sommets contient une valeur booléenne par canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104030632"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="38b36-103">Registre de prédicats (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="38b36-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="38b36-104">Ce registre de sortie du nuanceur de sommets contient une valeur booléenne par canal.</span><span class="sxs-lookup"><span data-stu-id="38b36-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="38b36-105">Un registre de prédicat est pris en charge par les versions suivantes.</span><span class="sxs-lookup"><span data-stu-id="38b36-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="38b36-106">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="38b36-106">Vertex shader versions</span></span> | <span data-ttu-id="38b36-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="38b36-107">1\_1</span></span> | <span data-ttu-id="38b36-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="38b36-108">2\_0</span></span> | <span data-ttu-id="38b36-109">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="38b36-109">2\_sw</span></span> | <span data-ttu-id="38b36-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="38b36-110">2\_x</span></span> | <span data-ttu-id="38b36-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="38b36-111">3\_0</span></span> | <span data-ttu-id="38b36-112">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="38b36-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="38b36-113">Registre de prédicat</span><span class="sxs-lookup"><span data-stu-id="38b36-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="38b36-114">x</span><span class="sxs-lookup"><span data-stu-id="38b36-114">x</span></span>    | <span data-ttu-id="38b36-115">x</span><span class="sxs-lookup"><span data-stu-id="38b36-115">x</span></span>    | <span data-ttu-id="38b36-116">x</span><span class="sxs-lookup"><span data-stu-id="38b36-116">x</span></span>     |



 

<span data-ttu-id="38b36-117">Voici les propriétés du Registre.</span><span class="sxs-lookup"><span data-stu-id="38b36-117">Here are the register properties.</span></span>



| <span data-ttu-id="38b36-118">Type de Registre</span><span class="sxs-lookup"><span data-stu-id="38b36-118">Register type</span></span> | <span data-ttu-id="38b36-119">Count</span><span class="sxs-lookup"><span data-stu-id="38b36-119">Count</span></span> | <span data-ttu-id="38b36-120">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="38b36-120">R/W</span></span> | <span data-ttu-id="38b36-121">\# Ports de lecture</span><span class="sxs-lookup"><span data-stu-id="38b36-121">\# Read ports</span></span> | <span data-ttu-id="38b36-122">\# Lectures/inst</span><span class="sxs-lookup"><span data-stu-id="38b36-122">\# Reads/inst</span></span> | <span data-ttu-id="38b36-123">Dimension</span><span class="sxs-lookup"><span data-stu-id="38b36-123">Dimension</span></span> | <span data-ttu-id="38b36-124">RelAddr</span><span class="sxs-lookup"><span data-stu-id="38b36-124">RelAddr</span></span> | <span data-ttu-id="38b36-125">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="38b36-125">Defaults</span></span> | <span data-ttu-id="38b36-126">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="38b36-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="38b36-127">Prédicat (p)</span><span class="sxs-lookup"><span data-stu-id="38b36-127">Predicate(p)</span></span>  | <span data-ttu-id="38b36-128">1</span><span class="sxs-lookup"><span data-stu-id="38b36-128">1</span></span>     | <span data-ttu-id="38b36-129">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="38b36-129">R/W</span></span> | <span data-ttu-id="38b36-130">1</span><span class="sxs-lookup"><span data-stu-id="38b36-130">1</span></span>             | <span data-ttu-id="38b36-131">1</span><span class="sxs-lookup"><span data-stu-id="38b36-131">1</span></span>             | <span data-ttu-id="38b36-132">4</span><span class="sxs-lookup"><span data-stu-id="38b36-132">4</span></span>         | <span data-ttu-id="38b36-133">N/A</span><span class="sxs-lookup"><span data-stu-id="38b36-133">N/A</span></span>     | <span data-ttu-id="38b36-134">None</span><span class="sxs-lookup"><span data-stu-id="38b36-134">None</span></span>     | <span data-ttu-id="38b36-135">N</span><span class="sxs-lookup"><span data-stu-id="38b36-135">N</span></span>            |



 

<span data-ttu-id="38b36-136">Le registre de prédicat peut être modifié avec [setp \_ COMP-vs](setp-comp---vs.md). Il n’y a aucune valeur par défaut pour ce registre, une application doit définir le registre avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="38b36-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38b36-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38b36-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b36-138">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="38b36-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




