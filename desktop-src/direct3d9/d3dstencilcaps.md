---
description: Indicateurs de capacité du stencil du pilote.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343054"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="d237c-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="d237c-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="d237c-104">Indicateurs de capacité du stencil du pilote.</span><span class="sxs-lookup"><span data-stu-id="d237c-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="d237c-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="d237c-105">\#define</span></span>                 | <span data-ttu-id="d237c-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d237c-106">Value</span></span>       | <span data-ttu-id="d237c-107">Description</span><span class="sxs-lookup"><span data-stu-id="d237c-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d237c-108">D3DSTENCILCAPS \_ conserver</span><span class="sxs-lookup"><span data-stu-id="d237c-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="d237c-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="d237c-109">0x00000001L</span></span> | <span data-ttu-id="d237c-110">Ne mettez pas à jour l’entrée dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="d237c-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="d237c-111">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d237c-111">This is the default value.</span></span>                             |
| <span data-ttu-id="d237c-112">D3DSTENCILCAPS \_ zéro</span><span class="sxs-lookup"><span data-stu-id="d237c-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="d237c-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="d237c-113">0x00000002L</span></span> | <span data-ttu-id="d237c-114">Affectez à l’entrée de tampon stencil la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="d237c-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="d237c-115">D3DSTENCILCAPS \_ remplacer</span><span class="sxs-lookup"><span data-stu-id="d237c-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="d237c-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="d237c-116">0x00000004L</span></span> | <span data-ttu-id="d237c-117">Remplacez l’entrée stencil-tampon par la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="d237c-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="d237c-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="d237c-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="d237c-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="d237c-119">0x00000008L</span></span> | <span data-ttu-id="d237c-120">Incrémentez l’entrée de mémoire tampon du stencil, en la conservant à la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="d237c-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="d237c-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="d237c-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="d237c-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="d237c-122">0x00000010L</span></span> | <span data-ttu-id="d237c-123">Décrémenter l’entrée de mémoire tampon du stencil, en la mettant à zéro.</span><span class="sxs-lookup"><span data-stu-id="d237c-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="d237c-124">D3DSTENCILCAPS \_ inversé</span><span class="sxs-lookup"><span data-stu-id="d237c-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="d237c-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="d237c-125">0x00000020L</span></span> | <span data-ttu-id="d237c-126">Inversez les bits dans l’entrée de mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="d237c-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="d237c-127">\_Incr D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="d237c-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="d237c-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="d237c-128">0x00000040L</span></span> | <span data-ttu-id="d237c-129">Incrémente l’entrée de mémoire tampon du stencil, en renvoyant à zéro si la nouvelle valeur dépasse la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="d237c-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="d237c-130">D3DSTENCILCAPS \_ DECR (</span><span class="sxs-lookup"><span data-stu-id="d237c-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="d237c-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="d237c-131">0x00000080L</span></span> | <span data-ttu-id="d237c-132">Décrémente l’entrée de mémoire tampon du stencil, en renvoyant à la valeur maximale si la nouvelle valeur est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="d237c-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="d237c-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="d237c-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="d237c-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="d237c-134">0x00000100L</span></span> | <span data-ttu-id="d237c-135">L’appareil prend en charge le stencil à deux côtés.</span><span class="sxs-lookup"><span data-stu-id="d237c-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="d237c-136">Les entrées de mémoire tampon de stencil sont des valeurs entières comprises entre 0 et 2 ⁿ-1, où n est la profondeur en bits de la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="d237c-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="d237c-137">Ces constantes sont utilisées par le membre StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="d237c-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="d237c-138">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="d237c-138">Constant Information</span></span>



| <span data-ttu-id="d237c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d237c-139">Requirement</span></span>                         | <span data-ttu-id="d237c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="d237c-140">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="d237c-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="d237c-141">Header</span></span>                   | <span data-ttu-id="d237c-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d237c-142">d3d9caps.h</span></span> |
| <span data-ttu-id="d237c-143">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="d237c-143">Minimum operating system</span></span> | <span data-ttu-id="d237c-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d237c-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d237c-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d237c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d237c-146">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="d237c-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



