---
title: abs
description: Retourne la valeur absolue de la valeur spécifiée.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- langage HLSL ABS
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971770"
---
# <a name="abs"></a><span data-ttu-id="5d377-104">abs</span><span class="sxs-lookup"><span data-stu-id="5d377-104">abs</span></span>

<span data-ttu-id="5d377-105">Retourne la valeur absolue de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5d377-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="5d377-106">RET ABS (*x*)</span><span class="sxs-lookup"><span data-stu-id="5d377-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="5d377-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d377-107">Parameters</span></span>



| <span data-ttu-id="5d377-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5d377-108">Item</span></span>                                                   | <span data-ttu-id="5d377-109">Description</span><span class="sxs-lookup"><span data-stu-id="5d377-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="5d377-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="5d377-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5d377-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5d377-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5d377-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5d377-112">Return Value</span></span>

<span data-ttu-id="5d377-113">Valeur absolue du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="5d377-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="5d377-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="5d377-114">Type Description</span></span>



| <span data-ttu-id="5d377-115">Nom</span><span class="sxs-lookup"><span data-stu-id="5d377-115">Name</span></span>  | [<span data-ttu-id="5d377-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="5d377-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5d377-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="5d377-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="5d377-118">Taille</span><span class="sxs-lookup"><span data-stu-id="5d377-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5d377-119">*x*</span><span class="sxs-lookup"><span data-stu-id="5d377-119">*x*</span></span>   | <span data-ttu-id="5d377-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="5d377-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="5d377-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5d377-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="5d377-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="5d377-122">any</span></span>                            |
| <span data-ttu-id="5d377-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="5d377-123">*ret*</span></span> | <span data-ttu-id="5d377-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="5d377-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="5d377-125">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="5d377-125">same as input *x*</span></span>                                                              | <span data-ttu-id="5d377-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="5d377-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5d377-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5d377-127">Minimum Shader Model</span></span>

<span data-ttu-id="5d377-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5d377-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5d377-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5d377-129">Shader Model</span></span>                                                                       | <span data-ttu-id="5d377-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5d377-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="5d377-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="5d377-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5d377-132">Oui</span><span class="sxs-lookup"><span data-stu-id="5d377-132">yes</span></span>                   |
| [<span data-ttu-id="5d377-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d377-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5d377-134">vs \_ 1 \_ 1 et PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="5d377-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="5d377-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d377-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d377-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5d377-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

