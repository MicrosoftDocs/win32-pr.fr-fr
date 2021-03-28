---
title: RET-vs
description: Retour à partir d’une sous-routine ou d’une fonction main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313651"
---
# <a name="ret---vs"></a><span data-ttu-id="fab66-103">RET-vs</span><span class="sxs-lookup"><span data-stu-id="fab66-103">ret - vs</span></span>

<span data-ttu-id="fab66-104">Retour à partir d’une sous-routine ou d’une fonction main.</span><span class="sxs-lookup"><span data-stu-id="fab66-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fab66-105">Syntax</span></span>



| <span data-ttu-id="fab66-106">Av</span><span class="sxs-lookup"><span data-stu-id="fab66-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="fab66-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fab66-107">Remarks</span></span>



| <span data-ttu-id="fab66-108">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="fab66-108">Vertex shader versions</span></span> | <span data-ttu-id="fab66-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="fab66-109">1\_1</span></span> | <span data-ttu-id="fab66-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fab66-110">2\_0</span></span> | <span data-ttu-id="fab66-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fab66-111">2\_x</span></span> | <span data-ttu-id="fab66-112">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fab66-112">2\_sw</span></span> | <span data-ttu-id="fab66-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fab66-113">3\_0</span></span> | <span data-ttu-id="fab66-114">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fab66-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="fab66-115">Av</span><span class="sxs-lookup"><span data-stu-id="fab66-115">ret</span></span>                    |      | <span data-ttu-id="fab66-116">x</span><span class="sxs-lookup"><span data-stu-id="fab66-116">x</span></span>    | <span data-ttu-id="fab66-117">x</span><span class="sxs-lookup"><span data-stu-id="fab66-117">x</span></span>    | <span data-ttu-id="fab66-118">x</span><span class="sxs-lookup"><span data-stu-id="fab66-118">x</span></span>     | <span data-ttu-id="fab66-119">x</span><span class="sxs-lookup"><span data-stu-id="fab66-119">x</span></span>    | <span data-ttu-id="fab66-120">x</span><span class="sxs-lookup"><span data-stu-id="fab66-120">x</span></span>     |



 

<span data-ttu-id="fab66-121">Cette instruction prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution.</span><span class="sxs-lookup"><span data-stu-id="fab66-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="fab66-122">Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fab66-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="fab66-123">L’instruction RET consomme un emplacement d’instruction de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="fab66-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="fab66-124">Si un nuanceur ne contient pas de sous-routines, l’utilisation de RET à la fin du programme principal est facultative.</span><span class="sxs-lookup"><span data-stu-id="fab66-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="fab66-125">Plusieurs instructions return ne sont pas autorisées dans le programme principal ou dans une sous-routine, la première instruction return est traitée comme la fin du programme ou de la sous-routine principale.</span><span class="sxs-lookup"><span data-stu-id="fab66-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fab66-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fab66-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab66-127">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="fab66-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




