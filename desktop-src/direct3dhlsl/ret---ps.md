---
title: RET-PS
description: Prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution. Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971546"
---
# <a name="ret---ps"></a><span data-ttu-id="c8a40-104">RET-PS</span><span class="sxs-lookup"><span data-stu-id="c8a40-104">ret - ps</span></span>

<span data-ttu-id="c8a40-105">Prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution.</span><span class="sxs-lookup"><span data-stu-id="c8a40-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="c8a40-106">Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c8a40-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a40-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8a40-107">Syntax</span></span>



| <span data-ttu-id="c8a40-108">Av</span><span class="sxs-lookup"><span data-stu-id="c8a40-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="c8a40-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c8a40-109">Remarks</span></span>



| <span data-ttu-id="c8a40-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c8a40-110">Pixel shader versions</span></span> | <span data-ttu-id="c8a40-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="c8a40-111">1\_1</span></span> | <span data-ttu-id="c8a40-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="c8a40-112">1\_2</span></span> | <span data-ttu-id="c8a40-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c8a40-113">1\_3</span></span> | <span data-ttu-id="c8a40-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="c8a40-114">1\_4</span></span> | <span data-ttu-id="c8a40-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c8a40-115">2\_0</span></span> | <span data-ttu-id="c8a40-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c8a40-116">2\_x</span></span> | <span data-ttu-id="c8a40-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c8a40-117">2\_sw</span></span> | <span data-ttu-id="c8a40-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c8a40-118">3\_0</span></span> | <span data-ttu-id="c8a40-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c8a40-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c8a40-120">Av</span><span class="sxs-lookup"><span data-stu-id="c8a40-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="c8a40-121">x</span><span class="sxs-lookup"><span data-stu-id="c8a40-121">x</span></span>    | <span data-ttu-id="c8a40-122">x</span><span class="sxs-lookup"><span data-stu-id="c8a40-122">x</span></span>     | <span data-ttu-id="c8a40-123">x</span><span class="sxs-lookup"><span data-stu-id="c8a40-123">x</span></span>    | <span data-ttu-id="c8a40-124">x</span><span class="sxs-lookup"><span data-stu-id="c8a40-124">x</span></span>     |



 

<span data-ttu-id="c8a40-125">Cette instruction prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution.</span><span class="sxs-lookup"><span data-stu-id="c8a40-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="c8a40-126">Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c8a40-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="c8a40-127">L’instruction RET consomme un emplacement d’instruction de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="c8a40-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="c8a40-128">Si un nuanceur ne contient pas de sous-routines, l’utilisation de RET à la fin du programme principal est facultative.</span><span class="sxs-lookup"><span data-stu-id="c8a40-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="c8a40-129">Plusieurs instructions return ne sont pas autorisées dans le programme principal ou dans une sous-routine, la première instruction return est traitée comme la fin du programme ou de la sous-routine principale.</span><span class="sxs-lookup"><span data-stu-id="c8a40-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8a40-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8a40-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a40-131">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c8a40-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




