---
title: Registre d’adresses
description: Le Registre a0 est un registre d’adresses.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840466"
---
# <a name="address-register"></a><span data-ttu-id="40932-103">Registre d’adresses</span><span class="sxs-lookup"><span data-stu-id="40932-103">Address Register</span></span>

<span data-ttu-id="40932-104">Le Registre a0 est un registre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="40932-104">The a0 register is an address register.</span></span> <span data-ttu-id="40932-105">Un registre unique est disponible dans la version vs \_ 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="40932-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="40932-106">Le registre d’adresses, désigné par a0. x dans vs \_ 1 \_ 1, peut être utilisé comme décalage d’entier signé pour l’adressage relatif dans le fichier de registre de constante.</span><span class="sxs-lookup"><span data-stu-id="40932-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="40932-107">Pour les versions vs \_ 2 \_ et supérieures, les quatre composants (. x,. y,. z,. w) sont disponibles pour l’adressage relatif.</span><span class="sxs-lookup"><span data-stu-id="40932-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="40932-108">Le registre d’adresses ne peut pas être lu par un nuanceur de sommets, il ne peut être utilisé que pour l’adressage relatif d’un registre de constante.</span><span class="sxs-lookup"><span data-stu-id="40932-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="40932-109">La lecture des valeurs en dehors de la plage légale retourne (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="40932-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="40932-110">Le registre d’adresses ne peut être qu’une destination pour l’instruction [MOV-vs](mov---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="40932-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="40932-111">Si un nombre à virgule flottante est déplacé dans un registre d’entiers, une conversion d’arrondi à la valeur la plus proche se produit.</span><span class="sxs-lookup"><span data-stu-id="40932-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="40932-112">Tous les nuanceurs doivent initialiser le registre d’adresses avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="40932-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="40932-113">Pour la version de vs \_ 2 \_ 0 et les versions ultérieures, l’instruction [Mova-vs](mova---vs.md) peut déplacer une valeur à virgule flottante vers un registre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="40932-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="40932-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="40932-114">Vertex shader versions</span></span> | <span data-ttu-id="40932-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="40932-115">1\_1</span></span> | <span data-ttu-id="40932-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="40932-116">2\_0</span></span> | <span data-ttu-id="40932-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="40932-117">2\_sw</span></span> | <span data-ttu-id="40932-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="40932-118">2\_x</span></span> | <span data-ttu-id="40932-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="40932-119">3\_0</span></span> | <span data-ttu-id="40932-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="40932-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="40932-121">Registre d’adresses</span><span class="sxs-lookup"><span data-stu-id="40932-121">Address Register</span></span>       | <span data-ttu-id="40932-122">x</span><span class="sxs-lookup"><span data-stu-id="40932-122">x</span></span>    | <span data-ttu-id="40932-123">x</span><span class="sxs-lookup"><span data-stu-id="40932-123">x</span></span>    | <span data-ttu-id="40932-124">x</span><span class="sxs-lookup"><span data-stu-id="40932-124">x</span></span>     | <span data-ttu-id="40932-125">x</span><span class="sxs-lookup"><span data-stu-id="40932-125">x</span></span>    | <span data-ttu-id="40932-126">x</span><span class="sxs-lookup"><span data-stu-id="40932-126">x</span></span>    | <span data-ttu-id="40932-127">x</span><span class="sxs-lookup"><span data-stu-id="40932-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="40932-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40932-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40932-129">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="40932-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




