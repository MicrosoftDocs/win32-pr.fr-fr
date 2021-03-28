---
title: vs
description: Cette instruction spécifie le numéro de version du nuanceur. Cette instruction fonctionne sur toutes les versions de nuanceur.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381223"
---
# <a name="vs"></a><span data-ttu-id="53f64-104">vs</span><span class="sxs-lookup"><span data-stu-id="53f64-104">vs</span></span>

<span data-ttu-id="53f64-105">Cette instruction spécifie le numéro de version du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53f64-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="53f64-106">Cette instruction fonctionne sur toutes les versions de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53f64-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f64-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53f64-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="53f64-108">Arguments d’entrée</span><span class="sxs-lookup"><span data-stu-id="53f64-108">Input Arguments</span></span>

<span data-ttu-id="53f64-109">Les arguments d’entrée contiennent un seul numéro de version principale avec un numéro de sous-version unique.</span><span class="sxs-lookup"><span data-stu-id="53f64-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="53f64-110">Les combinaisons autorisées sont répertoriées dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="53f64-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="53f64-111">Versions principales</span><span class="sxs-lookup"><span data-stu-id="53f64-111">Main versions</span></span> | <span data-ttu-id="53f64-112">Sous-versions</span><span class="sxs-lookup"><span data-stu-id="53f64-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="53f64-113">1</span><span class="sxs-lookup"><span data-stu-id="53f64-113">1</span></span>             | <span data-ttu-id="53f64-114">1</span><span class="sxs-lookup"><span data-stu-id="53f64-114">1</span></span>                              |
| <span data-ttu-id="53f64-115">2</span><span class="sxs-lookup"><span data-stu-id="53f64-115">2</span></span>             | <span data-ttu-id="53f64-116">0, SW (logiciel), x (étendu)</span><span class="sxs-lookup"><span data-stu-id="53f64-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="53f64-117">3</span><span class="sxs-lookup"><span data-stu-id="53f64-117">3</span></span>             | <span data-ttu-id="53f64-118">0, SW (logiciel)</span><span class="sxs-lookup"><span data-stu-id="53f64-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="53f64-119">Notes</span><span class="sxs-lookup"><span data-stu-id="53f64-119">Remarks</span></span>



| <span data-ttu-id="53f64-120">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="53f64-120">Vertex shader versions</span></span> | <span data-ttu-id="53f64-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="53f64-121">1\_1</span></span> | <span data-ttu-id="53f64-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53f64-122">2\_0</span></span> | <span data-ttu-id="53f64-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53f64-123">2\_x</span></span> | <span data-ttu-id="53f64-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="53f64-124">2\_sw</span></span> | <span data-ttu-id="53f64-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53f64-125">3\_0</span></span> | <span data-ttu-id="53f64-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="53f64-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="53f64-127">vs</span><span class="sxs-lookup"><span data-stu-id="53f64-127">vs</span></span>                     | <span data-ttu-id="53f64-128">x</span><span class="sxs-lookup"><span data-stu-id="53f64-128">x</span></span>    | <span data-ttu-id="53f64-129">x</span><span class="sxs-lookup"><span data-stu-id="53f64-129">x</span></span>    | <span data-ttu-id="53f64-130">x</span><span class="sxs-lookup"><span data-stu-id="53f64-130">x</span></span>    | <span data-ttu-id="53f64-131">x</span><span class="sxs-lookup"><span data-stu-id="53f64-131">x</span></span>     | <span data-ttu-id="53f64-132">x</span><span class="sxs-lookup"><span data-stu-id="53f64-132">x</span></span>    | <span data-ttu-id="53f64-133">x</span><span class="sxs-lookup"><span data-stu-id="53f64-133">x</span></span>     |



 

<span data-ttu-id="53f64-134">Cette instruction doit être la première instruction sans commentaire dans un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="53f64-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="53f64-135">Cette instruction est prise en charge dans toutes les versions de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="53f64-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="53f64-136">Les versions à accélération matérielle du logiciel (versions sans \_ logiciel dans le numéro de version) peuvent traiter les vertex avec le matériel accelearation ou utiliser le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="53f64-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="53f64-137">Les versions de logiciels (versions avec \_ SW dans le numéro de version) traitent les vertex uniquement avec le logiciel.</span><span class="sxs-lookup"><span data-stu-id="53f64-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="53f64-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="53f64-138">Examples</span></span>

<span data-ttu-id="53f64-139">Cet exemple partiel déclare un \_ nuanceur vertex version 1 1.</span><span class="sxs-lookup"><span data-stu-id="53f64-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="53f64-140">Cet exemple partiel déclare un nuanceur vertex de la version 2.</span><span class="sxs-lookup"><span data-stu-id="53f64-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="53f64-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53f64-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53f64-142">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="53f64-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




