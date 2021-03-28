---
title: ps
description: Cette instruction spécifie le numéro de version du nuanceur et fonctionne sur toutes les versions de nuanceur.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990820"
---
# <a name="ps"></a><span data-ttu-id="e9247-103">ps</span><span class="sxs-lookup"><span data-stu-id="e9247-103">ps</span></span>

<span data-ttu-id="e9247-104">Cette instruction spécifie le numéro de version du nuanceur et fonctionne sur toutes les versions de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e9247-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9247-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9247-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="e9247-106">Arguments d’entrée</span><span class="sxs-lookup"><span data-stu-id="e9247-106">Input Arguments</span></span>

<span data-ttu-id="e9247-107">Les arguments d’entrée contiennent un seul numéro de version principale avec un numéro de sous-version unique.</span><span class="sxs-lookup"><span data-stu-id="e9247-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="e9247-108">Les combinaisons autorisées sont répertoriées dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e9247-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="e9247-109">Versions principales</span><span class="sxs-lookup"><span data-stu-id="e9247-109">Main versions</span></span> | <span data-ttu-id="e9247-110">Sous-versions</span><span class="sxs-lookup"><span data-stu-id="e9247-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="e9247-111">1</span><span class="sxs-lookup"><span data-stu-id="e9247-111">1</span></span>             | <span data-ttu-id="e9247-112">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="e9247-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="e9247-113">2</span><span class="sxs-lookup"><span data-stu-id="e9247-113">2</span></span>             | <span data-ttu-id="e9247-114">0, x (étendu), SW (logiciel)</span><span class="sxs-lookup"><span data-stu-id="e9247-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="e9247-115">3</span><span class="sxs-lookup"><span data-stu-id="e9247-115">3</span></span>             | <span data-ttu-id="e9247-116">0, SW (logiciel)</span><span class="sxs-lookup"><span data-stu-id="e9247-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="e9247-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e9247-117">Remarks</span></span>



| <span data-ttu-id="e9247-118">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e9247-118">Pixel shader versions</span></span> | <span data-ttu-id="e9247-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="e9247-119">1\_1</span></span> | <span data-ttu-id="e9247-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="e9247-120">1\_2</span></span> | <span data-ttu-id="e9247-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e9247-121">1\_3</span></span> | <span data-ttu-id="e9247-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="e9247-122">1\_4</span></span> | <span data-ttu-id="e9247-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e9247-123">2\_0</span></span> | <span data-ttu-id="e9247-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e9247-124">2\_x</span></span> | <span data-ttu-id="e9247-125">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e9247-125">2\_sw</span></span> | <span data-ttu-id="e9247-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e9247-126">3\_0</span></span> | <span data-ttu-id="e9247-127">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e9247-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e9247-128">ps</span><span class="sxs-lookup"><span data-stu-id="e9247-128">ps</span></span>                    | <span data-ttu-id="e9247-129">x</span><span class="sxs-lookup"><span data-stu-id="e9247-129">x</span></span>    | <span data-ttu-id="e9247-130">x</span><span class="sxs-lookup"><span data-stu-id="e9247-130">x</span></span>    | <span data-ttu-id="e9247-131">x</span><span class="sxs-lookup"><span data-stu-id="e9247-131">x</span></span>    | <span data-ttu-id="e9247-132">x</span><span class="sxs-lookup"><span data-stu-id="e9247-132">x</span></span>    | <span data-ttu-id="e9247-133">x</span><span class="sxs-lookup"><span data-stu-id="e9247-133">x</span></span>    | <span data-ttu-id="e9247-134">x</span><span class="sxs-lookup"><span data-stu-id="e9247-134">x</span></span>    | <span data-ttu-id="e9247-135">x</span><span class="sxs-lookup"><span data-stu-id="e9247-135">x</span></span>     | <span data-ttu-id="e9247-136">x</span><span class="sxs-lookup"><span data-stu-id="e9247-136">x</span></span>    | <span data-ttu-id="e9247-137">x</span><span class="sxs-lookup"><span data-stu-id="e9247-137">x</span></span>     |



 

<span data-ttu-id="e9247-138">Cette instruction doit être la première instruction sans commentaire dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e9247-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="e9247-139">Les versions à accélération matérielle du logiciel (versions sans \_ logiciel dans le numéro de version) peuvent traiter les vertex avec le matériel accelearation ou utiliser le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="e9247-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="e9247-140">Les versions de logiciels (versions avec \_ SW dans le numéro de version) traitent les vertex uniquement avec le logiciel.</span><span class="sxs-lookup"><span data-stu-id="e9247-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="e9247-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="e9247-141">Examples</span></span>

<span data-ttu-id="e9247-142">Cet exemple partiel déclare un nuanceur de pixels de la version 1 \_ .</span><span class="sxs-lookup"><span data-stu-id="e9247-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="e9247-143">Cet exemple partiel déclare un nuanceur de pixels de la version 1 \_ .</span><span class="sxs-lookup"><span data-stu-id="e9247-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="e9247-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9247-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9247-145">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e9247-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




