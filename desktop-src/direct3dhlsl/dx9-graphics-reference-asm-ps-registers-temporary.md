---
title: Registre temporaire (référence du PS HLSL)
description: Les registres temporaires d’entrée de nuanceur de pixels sont utilisés pour conserver les résultats intermédiaires.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841717"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="c4bf8-103">Registre temporaire (référence du PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4bf8-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="c4bf8-104">Les registres temporaires d’entrée de nuanceur de pixels sont utilisés pour conserver les résultats intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="c4bf8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4bf8-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="c4bf8-106">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c4bf8-106">Pixel shader versions</span></span> | <span data-ttu-id="c4bf8-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="c4bf8-107">1\_1</span></span> | <span data-ttu-id="c4bf8-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="c4bf8-108">1\_2</span></span> | <span data-ttu-id="c4bf8-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c4bf8-109">1\_3</span></span> | <span data-ttu-id="c4bf8-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="c4bf8-110">1\_4</span></span> | <span data-ttu-id="c4bf8-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4bf8-111">2\_0</span></span> | <span data-ttu-id="c4bf8-112">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c4bf8-112">2\_sw</span></span> | <span data-ttu-id="c4bf8-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c4bf8-113">2\_x</span></span> | <span data-ttu-id="c4bf8-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4bf8-114">3\_0</span></span> | <span data-ttu-id="c4bf8-115">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c4bf8-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="c4bf8-116">Registre temporaire</span><span class="sxs-lookup"><span data-stu-id="c4bf8-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="c4bf8-117">x</span><span class="sxs-lookup"><span data-stu-id="c4bf8-117">x</span></span>    | <span data-ttu-id="c4bf8-118">x</span><span class="sxs-lookup"><span data-stu-id="c4bf8-118">x</span></span>     | <span data-ttu-id="c4bf8-119">x</span><span class="sxs-lookup"><span data-stu-id="c4bf8-119">x</span></span>    | <span data-ttu-id="c4bf8-120">x</span><span class="sxs-lookup"><span data-stu-id="c4bf8-120">x</span></span>    | <span data-ttu-id="c4bf8-121">x</span><span class="sxs-lookup"><span data-stu-id="c4bf8-121">x</span></span>     |



 

-   <span data-ttu-id="c4bf8-122">Il y a 12 registres temporaires de nuanceur de pixels : R0 à R11.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="c4bf8-123">Ces registres sont utilisés pour stocker les résultats intermédiaires lors des calculs.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="c4bf8-124">Si un registre temporaire utilise des composants qui ne sont pas définis dans le code précédent, la validation du nuanceur échoue.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="c4bf8-125">Il s’agit au moins d’une précision à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="c4bf8-126">Un maximum de trois peut être utilisé dans une instruction unique.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4bf8-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4bf8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4bf8-128">Inscrit</span><span class="sxs-lookup"><span data-stu-id="c4bf8-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




