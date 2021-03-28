---
title: 'StructuredBuffer :: Operator, fonction'
description: Retourne une variable de ressource en lecture seule d’un StructuredBuffer.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
keywords:
- Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102717"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="3e56c-104">StructuredBuffer :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="3e56c-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="3e56c-105">Retourne une variable de ressource en lecture seule d’un [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3e56c-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e56c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e56c-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="3e56c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e56c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e56c-108">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e56c-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e56c-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3e56c-109">Type: **uint**</span></span>

<span data-ttu-id="3e56c-110">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="3e56c-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e56c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e56c-111">Return value</span></span>

<span data-ttu-id="3e56c-112">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="3e56c-112">Type: **R**</span></span>

<span data-ttu-id="3e56c-113">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e56c-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e56c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3e56c-114">Remarks</span></span>

<span data-ttu-id="3e56c-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3e56c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3e56c-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="3e56c-116">Vertex</span></span> | <span data-ttu-id="3e56c-117">Forme</span><span class="sxs-lookup"><span data-stu-id="3e56c-117">Hull</span></span> | <span data-ttu-id="3e56c-118">Domain</span><span class="sxs-lookup"><span data-stu-id="3e56c-118">Domain</span></span> | <span data-ttu-id="3e56c-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3e56c-119">Geometry</span></span> | <span data-ttu-id="3e56c-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="3e56c-120">Pixel</span></span> | <span data-ttu-id="3e56c-121">Compute</span><span class="sxs-lookup"><span data-stu-id="3e56c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3e56c-122">x</span><span class="sxs-lookup"><span data-stu-id="3e56c-122">x</span></span>      | <span data-ttu-id="3e56c-123">x</span><span class="sxs-lookup"><span data-stu-id="3e56c-123">x</span></span>    | <span data-ttu-id="3e56c-124">x</span><span class="sxs-lookup"><span data-stu-id="3e56c-124">x</span></span>      | <span data-ttu-id="3e56c-125">x</span><span class="sxs-lookup"><span data-stu-id="3e56c-125">x</span></span>        | <span data-ttu-id="3e56c-126">x</span><span class="sxs-lookup"><span data-stu-id="3e56c-126">x</span></span>     | <span data-ttu-id="3e56c-127">x</span><span class="sxs-lookup"><span data-stu-id="3e56c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3e56c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e56c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e56c-129">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="3e56c-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="3e56c-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3e56c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




