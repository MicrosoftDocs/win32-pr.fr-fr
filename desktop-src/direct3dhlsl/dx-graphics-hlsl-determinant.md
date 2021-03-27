---
title: déterminantes
description: Retourne le déterminant de la matrice carrée à virgule flottante spécifiée.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- HLSL déterminant
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971730"
---
# <a name="determinant"></a><span data-ttu-id="72d55-104">déterminantes</span><span class="sxs-lookup"><span data-stu-id="72d55-104">determinant</span></span>

<span data-ttu-id="72d55-105">Retourne le déterminant de la matrice carrée à virgule flottante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="72d55-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="72d55-106">*RET* determine (*m*)</span><span class="sxs-lookup"><span data-stu-id="72d55-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="72d55-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d55-107">Parameters</span></span>



| <span data-ttu-id="72d55-108">Élément</span><span class="sxs-lookup"><span data-stu-id="72d55-108">Item</span></span>                                                   | <span data-ttu-id="72d55-109">Description</span><span class="sxs-lookup"><span data-stu-id="72d55-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="72d55-110"><span id="m"></span><span id="M"></span>*lecteur*</span><span class="sxs-lookup"><span data-stu-id="72d55-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="72d55-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="72d55-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="72d55-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="72d55-112">Return Value</span></span>

<span data-ttu-id="72d55-113">Valeur scalaire à virgule flottante qui représente le déterminant du paramètre *m* .</span><span class="sxs-lookup"><span data-stu-id="72d55-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="72d55-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="72d55-114">Type Description</span></span>



| <span data-ttu-id="72d55-115">Nom</span><span class="sxs-lookup"><span data-stu-id="72d55-115">Name</span></span>  | [<span data-ttu-id="72d55-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="72d55-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="72d55-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="72d55-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="72d55-118">Taille</span><span class="sxs-lookup"><span data-stu-id="72d55-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="72d55-119">*m*</span><span class="sxs-lookup"><span data-stu-id="72d55-119">*m*</span></span>   | [<span data-ttu-id="72d55-120">**matrice**</span><span class="sxs-lookup"><span data-stu-id="72d55-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="72d55-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="72d55-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="72d55-122">Any (nombre de lignes = nombre de colonnes)</span><span class="sxs-lookup"><span data-stu-id="72d55-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="72d55-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="72d55-123">*ret*</span></span> | [<span data-ttu-id="72d55-124">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="72d55-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="72d55-125">**float**</span><span class="sxs-lookup"><span data-stu-id="72d55-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="72d55-126">1</span><span class="sxs-lookup"><span data-stu-id="72d55-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="72d55-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="72d55-127">Minimum Shader Model</span></span>

<span data-ttu-id="72d55-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="72d55-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="72d55-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="72d55-129">Shader Model</span></span>                                                                       | <span data-ttu-id="72d55-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="72d55-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="72d55-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="72d55-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="72d55-132">Oui</span><span class="sxs-lookup"><span data-stu-id="72d55-132">yes</span></span>                   |
| [<span data-ttu-id="72d55-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72d55-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="72d55-134">vs \_ 1 \_ 1 et PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="72d55-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="72d55-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d55-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d55-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="72d55-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

