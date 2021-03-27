---
title: 'Buffer :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Buffer :: Operator, fonction'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Fonction d’opérateur écriture directe
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393907"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="8487b-105">Buffer :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="8487b-105">Buffer::Operator  function</span></span>

<span data-ttu-id="8487b-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8487b-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="8487b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8487b-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="8487b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8487b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8487b-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8487b-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8487b-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8487b-110">Type: **uint**</span></span>

<span data-ttu-id="8487b-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="8487b-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8487b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8487b-112">Return value</span></span>

<span data-ttu-id="8487b-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="8487b-113">Type: **R**</span></span>

<span data-ttu-id="8487b-114">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8487b-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="8487b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8487b-115">Remarks</span></span>

<span data-ttu-id="8487b-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8487b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8487b-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="8487b-117">Vertex</span></span> | <span data-ttu-id="8487b-118">Forme</span><span class="sxs-lookup"><span data-stu-id="8487b-118">Hull</span></span> | <span data-ttu-id="8487b-119">Domain</span><span class="sxs-lookup"><span data-stu-id="8487b-119">Domain</span></span> | <span data-ttu-id="8487b-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8487b-120">Geometry</span></span> | <span data-ttu-id="8487b-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="8487b-121">Pixel</span></span> | <span data-ttu-id="8487b-122">Compute</span><span class="sxs-lookup"><span data-stu-id="8487b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8487b-123">x</span><span class="sxs-lookup"><span data-stu-id="8487b-123">x</span></span>     | <span data-ttu-id="8487b-124">x</span><span class="sxs-lookup"><span data-stu-id="8487b-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8487b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8487b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8487b-126">Buffer</span><span class="sxs-lookup"><span data-stu-id="8487b-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="8487b-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8487b-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




