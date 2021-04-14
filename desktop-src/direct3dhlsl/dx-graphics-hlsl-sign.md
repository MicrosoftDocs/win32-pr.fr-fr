---
title: sign
description: Retourne le signe de x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- signer le langage HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991005"
---
# <a name="sign"></a><span data-ttu-id="508e3-104">sign</span><span class="sxs-lookup"><span data-stu-id="508e3-104">sign</span></span>

<span data-ttu-id="508e3-105">Retourne le signe de *x*.</span><span class="sxs-lookup"><span data-stu-id="508e3-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="508e3-106">signe *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="508e3-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="508e3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="508e3-107">Parameters</span></span>



| <span data-ttu-id="508e3-108">Élément</span><span class="sxs-lookup"><span data-stu-id="508e3-108">Item</span></span>                                                   | <span data-ttu-id="508e3-109">Description</span><span class="sxs-lookup"><span data-stu-id="508e3-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="508e3-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="508e3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="508e3-111">\[dans \] la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="508e3-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="508e3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="508e3-112">Return Value</span></span>

<span data-ttu-id="508e3-113">Retourne-1 si *x* est inférieur à zéro ; 0 si *x* est égal à zéro ; et 1 si *x* est supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="508e3-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="508e3-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="508e3-114">Type Description</span></span>



| <span data-ttu-id="508e3-115">Nom</span><span class="sxs-lookup"><span data-stu-id="508e3-115">Name</span></span>  | [<span data-ttu-id="508e3-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="508e3-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="508e3-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="508e3-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="508e3-118">Taille</span><span class="sxs-lookup"><span data-stu-id="508e3-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="508e3-119">*x*</span><span class="sxs-lookup"><span data-stu-id="508e3-119">*x*</span></span>   | <span data-ttu-id="508e3-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="508e3-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="508e3-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="508e3-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="508e3-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="508e3-122">any</span></span>                            |
| <span data-ttu-id="508e3-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="508e3-123">*ret*</span></span> | <span data-ttu-id="508e3-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="508e3-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="508e3-125">**int**</span><span class="sxs-lookup"><span data-stu-id="508e3-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="508e3-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="508e3-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="508e3-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="508e3-127">Minimum Shader Model</span></span>

<span data-ttu-id="508e3-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="508e3-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="508e3-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="508e3-129">Shader Model</span></span>                                                                       | <span data-ttu-id="508e3-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="508e3-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="508e3-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="508e3-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="508e3-132">Oui</span><span class="sxs-lookup"><span data-stu-id="508e3-132">yes</span></span>                         |
| [<span data-ttu-id="508e3-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="508e3-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="508e3-134">Oui (vs \_ 1 \_ 1 et PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="508e3-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="508e3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="508e3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508e3-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="508e3-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

