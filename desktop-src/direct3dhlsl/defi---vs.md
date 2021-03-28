---
title: signatures-vs
description: Définit une valeur de constante entière, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508061"
---
# <a name="defi---vs"></a><span data-ttu-id="e24c9-103">signatures-vs</span><span class="sxs-lookup"><span data-stu-id="e24c9-103">defi - vs</span></span>

<span data-ttu-id="e24c9-104">Définit une valeur de constante entière, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e24c9-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e24c9-105">Syntax</span></span>



| <span data-ttu-id="e24c9-106">detest DST, integerValue0, integerValue1, integerValue2, integerValue3</span><span class="sxs-lookup"><span data-stu-id="e24c9-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="e24c9-107">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="e24c9-107">dst is the destination register.</span></span>
-   <span data-ttu-id="e24c9-108">integerValue \# est une valeur entière constante.</span><span class="sxs-lookup"><span data-stu-id="e24c9-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e24c9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e24c9-109">Remarks</span></span>



| <span data-ttu-id="e24c9-110">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e24c9-110">Vertex shader versions</span></span> | <span data-ttu-id="e24c9-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="e24c9-111">1\_1</span></span> | <span data-ttu-id="e24c9-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e24c9-112">2\_0</span></span> | <span data-ttu-id="e24c9-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e24c9-113">2\_x</span></span> | <span data-ttu-id="e24c9-114">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e24c9-114">2\_sw</span></span> | <span data-ttu-id="e24c9-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e24c9-115">3\_0</span></span> | <span data-ttu-id="e24c9-116">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e24c9-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e24c9-117">signatures</span><span class="sxs-lookup"><span data-stu-id="e24c9-117">defi</span></span>                   |      | <span data-ttu-id="e24c9-118">x</span><span class="sxs-lookup"><span data-stu-id="e24c9-118">x</span></span>    | <span data-ttu-id="e24c9-119">x</span><span class="sxs-lookup"><span data-stu-id="e24c9-119">x</span></span>    | <span data-ttu-id="e24c9-120">x</span><span class="sxs-lookup"><span data-stu-id="e24c9-120">x</span></span>     | <span data-ttu-id="e24c9-121">x</span><span class="sxs-lookup"><span data-stu-id="e24c9-121">x</span></span>    | <span data-ttu-id="e24c9-122">x</span><span class="sxs-lookup"><span data-stu-id="e24c9-122">x</span></span>     |



 

<span data-ttu-id="e24c9-123">L’instruction de définition définit une constante de nuanceur entière dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e24c9-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="e24c9-124">Celles-ci sont appelées constantes immédiates.</span><span class="sxs-lookup"><span data-stu-id="e24c9-124">These are called immediate constants.</span></span> <span data-ttu-id="e24c9-125">Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetVertexShaderConstantI.</span><span class="sxs-lookup"><span data-stu-id="e24c9-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="e24c9-126">Il existe deux façons de définir une constante entière dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e24c9-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="e24c9-127">Utilisez la définition de type pour définir le vecteur de constante entier directement à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e24c9-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="e24c9-128">Utilisez les méthodes de l’API pour définir une constante.</span><span class="sxs-lookup"><span data-stu-id="e24c9-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="e24c9-129">Utilisez [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) pour définir une constante entière.</span><span class="sxs-lookup"><span data-stu-id="e24c9-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e24c9-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e24c9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e24c9-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e24c9-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="e24c9-132">def-vs</span><span class="sxs-lookup"><span data-stu-id="e24c9-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="e24c9-133">defb-vs</span><span class="sxs-lookup"><span data-stu-id="e24c9-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 