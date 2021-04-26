---
title: entrée dcl_usage (SM1, SM2, SM3-vs ASM)
description: Déclarez l’association entre une utilisation d’élément de vertex et un index d’utilisation pour un registre d’entrée de nuanceur de sommets.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44bd976d05c0734ca2e498b5de405564f689e20d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998386"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="48223-103">\_entrée d’utilisation DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="48223-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="48223-104">Déclarez l’association entre une utilisation d’élément de vertex et un index d’utilisation pour un registre d’entrée de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="48223-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="48223-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48223-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="48223-106">\_index d’utilisation de l’utilisation de DCL \[ \_ \]\#</span><span class="sxs-lookup"><span data-stu-id="48223-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="48223-107">Où :</span><span class="sxs-lookup"><span data-stu-id="48223-107">Where:</span></span>

-   <span data-ttu-id="48223-108">l' \_ utilisation de la configuration DCL identifie la manière dont les données du Registre sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="48223-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="48223-109">Il s’agit de la même valeur que les membres de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sans le préfixe D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="48223-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="48223-110">l' \_ index d’utilisation est un index d’entiers facultatif compris entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="48223-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="48223-111">Il modifie les données d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="48223-111">It modifies the usage data.</span></span> <span data-ttu-id="48223-112">L’index correspond à l’index d’utilisation dans une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="48223-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="48223-113">Voir la [déclaration de vertex (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="48223-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="48223-114">L’index est ajouté à la valeur d’utilisation (DCL \_ ) sans espace.</span><span class="sxs-lookup"><span data-stu-id="48223-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="48223-115">S’il n’est pas fourni, il est supposé être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="48223-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="48223-116">v \# est un [Registre d’entrée](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="48223-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="48223-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="48223-117">Remarks</span></span>



| <span data-ttu-id="48223-118">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="48223-118">Vertex shader versions</span></span> | <span data-ttu-id="48223-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="48223-119">1\_1</span></span> | <span data-ttu-id="48223-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48223-120">2\_0</span></span> | <span data-ttu-id="48223-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48223-121">2\_x</span></span> | <span data-ttu-id="48223-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="48223-122">2\_sw</span></span> | <span data-ttu-id="48223-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48223-123">3\_0</span></span> | <span data-ttu-id="48223-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="48223-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="48223-125">utilisation de DCL \_</span><span class="sxs-lookup"><span data-stu-id="48223-125">dcl\_usage</span></span>             | <span data-ttu-id="48223-126">x</span><span class="sxs-lookup"><span data-stu-id="48223-126">x</span></span>    | <span data-ttu-id="48223-127">x</span><span class="sxs-lookup"><span data-stu-id="48223-127">x</span></span>    | <span data-ttu-id="48223-128">x</span><span class="sxs-lookup"><span data-stu-id="48223-128">x</span></span>    | <span data-ttu-id="48223-129">x</span><span class="sxs-lookup"><span data-stu-id="48223-129">x</span></span>     | <span data-ttu-id="48223-130">x</span><span class="sxs-lookup"><span data-stu-id="48223-130">x</span></span>    | <span data-ttu-id="48223-131">x</span><span class="sxs-lookup"><span data-stu-id="48223-131">x</span></span>     |



 

<span data-ttu-id="48223-132">Toutes les \_ instructions d’utilisation de la DCL doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="48223-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48223-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="48223-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48223-134">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="48223-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
