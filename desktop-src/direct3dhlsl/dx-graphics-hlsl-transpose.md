---
title: permuter
description: Transpose la matrice d’entrée spécifiée.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- transposer le langage HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382066"
---
# <a name="transpose"></a><span data-ttu-id="edb0d-104">permuter</span><span class="sxs-lookup"><span data-stu-id="edb0d-104">transpose</span></span>

<span data-ttu-id="edb0d-105">Transpose la matrice d’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="edb0d-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="edb0d-106">RET transposer (*x*)</span><span class="sxs-lookup"><span data-stu-id="edb0d-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="edb0d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edb0d-107">Parameters</span></span>



| <span data-ttu-id="edb0d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="edb0d-108">Item</span></span>                                                   | <span data-ttu-id="edb0d-109">Description</span><span class="sxs-lookup"><span data-stu-id="edb0d-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="edb0d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="edb0d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="edb0d-111">\[dans \] la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="edb0d-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="edb0d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="edb0d-112">Return Value</span></span>

<span data-ttu-id="edb0d-113">Valeur transposée du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="edb0d-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb0d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="edb0d-114">Remarks</span></span>

<span data-ttu-id="edb0d-115">Si les dimensions de la matrice source sont des *colonnes* de *lignes* , la matrice résultante est celle des *lignes* de *colonnes* .</span><span class="sxs-lookup"><span data-stu-id="edb0d-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="edb0d-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="edb0d-116">Type Description</span></span>



| <span data-ttu-id="edb0d-117">Nom</span><span class="sxs-lookup"><span data-stu-id="edb0d-117">Name</span></span> | [<span data-ttu-id="edb0d-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="edb0d-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="edb0d-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="edb0d-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="edb0d-120">Taille</span><span class="sxs-lookup"><span data-stu-id="edb0d-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb0d-121">*x*</span><span class="sxs-lookup"><span data-stu-id="edb0d-121">*x*</span></span>  | [<span data-ttu-id="edb0d-122">**matrice**</span><span class="sxs-lookup"><span data-stu-id="edb0d-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="edb0d-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="edb0d-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="edb0d-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="edb0d-124">any</span></span>                                                                                    |
| <span data-ttu-id="edb0d-125">Av</span><span class="sxs-lookup"><span data-stu-id="edb0d-125">ret</span></span>  | [<span data-ttu-id="edb0d-126">**matrice**</span><span class="sxs-lookup"><span data-stu-id="edb0d-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="edb0d-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="edb0d-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="edb0d-128">Rows = même nombre de colonnes en entrée *x*, Columns = même nombre de lignes comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="edb0d-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="edb0d-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="edb0d-129">Minimum Shader Model</span></span>

<span data-ttu-id="edb0d-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="edb0d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="edb0d-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="edb0d-131">Shader Model</span></span>                                                                       | <span data-ttu-id="edb0d-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="edb0d-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="edb0d-133">[Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="edb0d-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="edb0d-134">Oui</span><span class="sxs-lookup"><span data-stu-id="edb0d-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="edb0d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edb0d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb0d-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="edb0d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

