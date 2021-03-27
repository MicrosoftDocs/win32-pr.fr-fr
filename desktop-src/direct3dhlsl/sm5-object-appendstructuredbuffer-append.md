---
title: 'AppendStructuredBuffer :: Append, fonction'
description: Ajoute une valeur à la fin de la mémoire tampon.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Fonction Append, HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103940527"
---
# <a name="append-function"></a><span data-ttu-id="2527e-104">Append, fonction</span><span class="sxs-lookup"><span data-stu-id="2527e-104">Append function</span></span>

<span data-ttu-id="2527e-105">Ajoute une valeur à la fin de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2527e-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2527e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2527e-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="2527e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2527e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2527e-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2527e-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2527e-109">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="2527e-109">Type: **T**</span></span>

<span data-ttu-id="2527e-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="2527e-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2527e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2527e-111">Return value</span></span>

<span data-ttu-id="2527e-112">None</span><span class="sxs-lookup"><span data-stu-id="2527e-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="2527e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2527e-113">Remarks</span></span>

<span data-ttu-id="2527e-114">T peut être n’importe quel type de données, y compris les structures.</span><span class="sxs-lookup"><span data-stu-id="2527e-114">T can be any data type including structures.</span></span>

<span data-ttu-id="2527e-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2527e-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2527e-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="2527e-116">Vertex</span></span> | <span data-ttu-id="2527e-117">Forme</span><span class="sxs-lookup"><span data-stu-id="2527e-117">Hull</span></span> | <span data-ttu-id="2527e-118">Domain</span><span class="sxs-lookup"><span data-stu-id="2527e-118">Domain</span></span> | <span data-ttu-id="2527e-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2527e-119">Geometry</span></span> | <span data-ttu-id="2527e-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="2527e-120">Pixel</span></span> | <span data-ttu-id="2527e-121">Compute</span><span class="sxs-lookup"><span data-stu-id="2527e-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2527e-122">x</span><span class="sxs-lookup"><span data-stu-id="2527e-122">x</span></span>      | <span data-ttu-id="2527e-123">x</span><span class="sxs-lookup"><span data-stu-id="2527e-123">x</span></span>    | <span data-ttu-id="2527e-124">x</span><span class="sxs-lookup"><span data-stu-id="2527e-124">x</span></span>      | <span data-ttu-id="2527e-125">x</span><span class="sxs-lookup"><span data-stu-id="2527e-125">x</span></span>        | <span data-ttu-id="2527e-126">x</span><span class="sxs-lookup"><span data-stu-id="2527e-126">x</span></span>     | <span data-ttu-id="2527e-127">x</span><span class="sxs-lookup"><span data-stu-id="2527e-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2527e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2527e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2527e-129">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="2527e-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="2527e-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2527e-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




