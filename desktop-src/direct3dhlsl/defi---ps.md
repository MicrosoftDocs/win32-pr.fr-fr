---
title: DEFAUT-PS
description: Définit une valeur de constante entière, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102077"
---
# <a name="defi---ps"></a><span data-ttu-id="52f45-103">DEFAUT-PS</span><span class="sxs-lookup"><span data-stu-id="52f45-103">defi - ps</span></span>

<span data-ttu-id="52f45-104">Définit une valeur de constante entière, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="52f45-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52f45-105">Syntax</span></span>



| <span data-ttu-id="52f45-106">detest DST, integerValue</span><span class="sxs-lookup"><span data-stu-id="52f45-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="52f45-107">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="52f45-107">dst is the destination register.</span></span>
-   <span data-ttu-id="52f45-108">integerValue est une valeur entière constante.</span><span class="sxs-lookup"><span data-stu-id="52f45-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f45-109">Notes</span><span class="sxs-lookup"><span data-stu-id="52f45-109">Remarks</span></span>



| <span data-ttu-id="52f45-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="52f45-110">Pixel shader versions</span></span> | <span data-ttu-id="52f45-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="52f45-111">1\_1</span></span> | <span data-ttu-id="52f45-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="52f45-112">1\_2</span></span> | <span data-ttu-id="52f45-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="52f45-113">1\_3</span></span> | <span data-ttu-id="52f45-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="52f45-114">1\_4</span></span> | <span data-ttu-id="52f45-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52f45-115">2\_0</span></span> | <span data-ttu-id="52f45-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="52f45-116">2\_x</span></span> | <span data-ttu-id="52f45-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="52f45-117">2\_sw</span></span> | <span data-ttu-id="52f45-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52f45-118">3\_0</span></span> | <span data-ttu-id="52f45-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="52f45-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="52f45-120">signatures</span><span class="sxs-lookup"><span data-stu-id="52f45-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="52f45-121">x</span><span class="sxs-lookup"><span data-stu-id="52f45-121">x</span></span>    | <span data-ttu-id="52f45-122">x</span><span class="sxs-lookup"><span data-stu-id="52f45-122">x</span></span>     | <span data-ttu-id="52f45-123">x</span><span class="sxs-lookup"><span data-stu-id="52f45-123">x</span></span>    | <span data-ttu-id="52f45-124">x</span><span class="sxs-lookup"><span data-stu-id="52f45-124">x</span></span>     |



 

<span data-ttu-id="52f45-125">L’instruction de définition définit une constante de nuanceur dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="52f45-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="52f45-126">Celles-ci sont appelées constantes immédiates.</span><span class="sxs-lookup"><span data-stu-id="52f45-126">These are called immediate constants.</span></span> <span data-ttu-id="52f45-127">Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="52f45-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="52f45-128">Il existe deux façons de définir une constante dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="52f45-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="52f45-129">Utilisez la définition de définition pour définir la constante directement à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="52f45-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="52f45-130">Utilisez les méthodes de l’API pour définir une constante.</span><span class="sxs-lookup"><span data-stu-id="52f45-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="52f45-131">Utilisez [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) pour définir une constante booléenne.</span><span class="sxs-lookup"><span data-stu-id="52f45-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="52f45-132">Utilisez [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) pour définir une constante à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="52f45-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="52f45-133">Utilisez [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) pour définir une constante entière.</span><span class="sxs-lookup"><span data-stu-id="52f45-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52f45-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52f45-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f45-135">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="52f45-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 