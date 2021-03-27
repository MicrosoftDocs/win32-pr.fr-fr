---
title: all
description: Détermine si tous les composants de la valeur spécifiée sont non nuls.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- tous les langages HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971798"
---
# <a name="all"></a><span data-ttu-id="1e217-104">all</span><span class="sxs-lookup"><span data-stu-id="1e217-104">all</span></span>

<span data-ttu-id="1e217-105">Détermine si tous les composants de la valeur spécifiée sont non nuls.</span><span class="sxs-lookup"><span data-stu-id="1e217-105">Determines if all components of the specified value are non-zero.</span></span>



| <span data-ttu-id="1e217-106">*RET* tout (*x*)</span><span class="sxs-lookup"><span data-stu-id="1e217-106">*ret* all(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="1e217-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e217-107">Parameters</span></span>



| <span data-ttu-id="1e217-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1e217-108">Item</span></span>                                                   | <span data-ttu-id="1e217-109">Description</span><span class="sxs-lookup"><span data-stu-id="1e217-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1e217-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="1e217-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1e217-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1e217-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1e217-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e217-112">Return Value</span></span>

<span data-ttu-id="1e217-113">**True** si tous les composants du paramètre *x* sont non null ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="1e217-113">**True** if all components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e217-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1e217-114">Remarks</span></span>

<span data-ttu-id="1e217-115">Cette fonction est similaire à [**toute**](dx-graphics-hlsl-any.md) fonction intrinsèque HLSL.</span><span class="sxs-lookup"><span data-stu-id="1e217-115">This function is similar to the [**any**](dx-graphics-hlsl-any.md) HLSL intrinsic function.</span></span> <span data-ttu-id="1e217-116">La fonction **any** détermine si tous les composants de la valeur spécifiée sont non nuls, tandis que la fonction **All** détermine si tous les composants de la valeur spécifiée sont non nuls.</span><span class="sxs-lookup"><span data-stu-id="1e217-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="1e217-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="1e217-117">Type Description</span></span>



| <span data-ttu-id="1e217-118">Nom</span><span class="sxs-lookup"><span data-stu-id="1e217-118">Name</span></span>  | [<span data-ttu-id="1e217-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="1e217-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1e217-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="1e217-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="1e217-121">Taille</span><span class="sxs-lookup"><span data-stu-id="1e217-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="1e217-122">*x*</span><span class="sxs-lookup"><span data-stu-id="1e217-122">*x*</span></span>   | <span data-ttu-id="1e217-123">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="1e217-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="1e217-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1e217-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="1e217-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="1e217-125">any</span></span>  |
| <span data-ttu-id="1e217-126">*Av*</span><span class="sxs-lookup"><span data-stu-id="1e217-126">*ret*</span></span> | [<span data-ttu-id="1e217-127">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="1e217-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="1e217-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e217-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="1e217-129">1</span><span class="sxs-lookup"><span data-stu-id="1e217-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1e217-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1e217-130">Minimum Shader Model</span></span>

<span data-ttu-id="1e217-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1e217-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1e217-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1e217-132">Shader Model</span></span>                                                                       | <span data-ttu-id="1e217-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1e217-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="1e217-134">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="1e217-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1e217-135">Oui</span><span class="sxs-lookup"><span data-stu-id="1e217-135">yes</span></span>                   |
| [<span data-ttu-id="1e217-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e217-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1e217-137">vs \_ 1 \_ 1 et PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="1e217-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1e217-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e217-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e217-139">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1e217-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

