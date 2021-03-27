---
title: length
description: Retourne la longueur du vecteur à virgule flottante spécifié.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- de longueur HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727853"
---
# <a name="length"></a><span data-ttu-id="e53c3-104">length</span><span class="sxs-lookup"><span data-stu-id="e53c3-104">length</span></span>

<span data-ttu-id="e53c3-105">Retourne la longueur du vecteur à virgule flottante spécifié.</span><span class="sxs-lookup"><span data-stu-id="e53c3-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="e53c3-106">longueur *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="e53c3-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="e53c3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e53c3-107">Parameters</span></span>



| <span data-ttu-id="e53c3-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e53c3-108">Item</span></span>                                                   | <span data-ttu-id="e53c3-109">Description</span><span class="sxs-lookup"><span data-stu-id="e53c3-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="e53c3-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e53c3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e53c3-111">Vecteur à virgule flottante spécifié.</span><span class="sxs-lookup"><span data-stu-id="e53c3-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e53c3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e53c3-112">Return Value</span></span>

<span data-ttu-id="e53c3-113">Scalaire à virgule flottante qui représente la longueur du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="e53c3-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="e53c3-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="e53c3-114">Type Description</span></span>



| <span data-ttu-id="e53c3-115">Nom</span><span class="sxs-lookup"><span data-stu-id="e53c3-115">Name</span></span>  | [<span data-ttu-id="e53c3-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="e53c3-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e53c3-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="e53c3-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e53c3-118">Taille</span><span class="sxs-lookup"><span data-stu-id="e53c3-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e53c3-119">*x*</span><span class="sxs-lookup"><span data-stu-id="e53c3-119">*x*</span></span>   | [<span data-ttu-id="e53c3-120">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="e53c3-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e53c3-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="e53c3-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e53c3-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="e53c3-122">any</span></span>  |
| <span data-ttu-id="e53c3-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="e53c3-123">*ret*</span></span> | [<span data-ttu-id="e53c3-124">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="e53c3-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e53c3-125">**float**</span><span class="sxs-lookup"><span data-stu-id="e53c3-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e53c3-126">1</span><span class="sxs-lookup"><span data-stu-id="e53c3-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e53c3-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e53c3-127">Minimum Shader Model</span></span>

<span data-ttu-id="e53c3-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="e53c3-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e53c3-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e53c3-129">Shader Model</span></span>                                                                       | <span data-ttu-id="e53c3-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e53c3-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e53c3-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="e53c3-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e53c3-132">Oui</span><span class="sxs-lookup"><span data-stu-id="e53c3-132">yes</span></span>                 |
| [<span data-ttu-id="e53c3-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e53c3-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e53c3-134">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="e53c3-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e53c3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e53c3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53c3-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e53c3-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

