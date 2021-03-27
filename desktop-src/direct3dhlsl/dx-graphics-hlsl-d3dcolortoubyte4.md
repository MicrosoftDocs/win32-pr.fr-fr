---
title: D3DCOLORtoUBYTE4
description: Convertit un vecteur 4D à virgule flottante défini par un D3DCOLOR en UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- HLSL D3DCOLORtoUBYTE4
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508105"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="d7bc1-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="d7bc1-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="d7bc1-105">Convertit un vecteur 4D à virgule flottante défini par un D3DCOLOR en UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d7bc1-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="d7bc1-106">*RET* D3DCOLORtoUBYTE4 (*x*)</span><span class="sxs-lookup"><span data-stu-id="d7bc1-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="d7bc1-107">Cette fonction Swizzles et met à l’échelle les composants du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="d7bc1-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="d7bc1-108">Utilisez cette fonction pour compenser l’absence de prise en charge de UBYTE4 dans un matériel.</span><span class="sxs-lookup"><span data-stu-id="d7bc1-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7bc1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7bc1-109">Parameters</span></span>



| <span data-ttu-id="d7bc1-110">Élément</span><span class="sxs-lookup"><span data-stu-id="d7bc1-110">Item</span></span>                                                   | <span data-ttu-id="d7bc1-111">Description</span><span class="sxs-lookup"><span data-stu-id="d7bc1-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="d7bc1-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d7bc1-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d7bc1-113">\[dans \] le Vector4 à virgule flottante à convertir.</span><span class="sxs-lookup"><span data-stu-id="d7bc1-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d7bc1-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7bc1-114">Return Value</span></span>

<span data-ttu-id="d7bc1-115">Représentation UBYTE4 du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="d7bc1-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d7bc1-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="d7bc1-116">Type Description</span></span>



| <span data-ttu-id="d7bc1-117">Nom</span><span class="sxs-lookup"><span data-stu-id="d7bc1-117">Name</span></span>  | [<span data-ttu-id="d7bc1-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d7bc1-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d7bc1-120">Taille</span><span class="sxs-lookup"><span data-stu-id="d7bc1-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d7bc1-121">*x*</span><span class="sxs-lookup"><span data-stu-id="d7bc1-121">*x*</span></span>   | [<span data-ttu-id="d7bc1-122">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d7bc1-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d7bc1-124">4</span><span class="sxs-lookup"><span data-stu-id="d7bc1-124">4</span></span>    |
| <span data-ttu-id="d7bc1-125">*Av*</span><span class="sxs-lookup"><span data-stu-id="d7bc1-125">*ret*</span></span> | [<span data-ttu-id="d7bc1-126">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d7bc1-127">**entier**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="d7bc1-128">4</span><span class="sxs-lookup"><span data-stu-id="d7bc1-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7bc1-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d7bc1-129">Minimum Shader Model</span></span>

<span data-ttu-id="d7bc1-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d7bc1-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d7bc1-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d7bc1-131">Shader Model</span></span>                                                                       | <span data-ttu-id="d7bc1-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d7bc1-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d7bc1-133">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="d7bc1-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d7bc1-134">Oui</span><span class="sxs-lookup"><span data-stu-id="d7bc1-134">yes</span></span>       |
| [<span data-ttu-id="d7bc1-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7bc1-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d7bc1-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d7bc1-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="d7bc1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7bc1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bc1-138">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d7bc1-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

