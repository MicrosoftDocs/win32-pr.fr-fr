---
title: 'RWByteAddressBuffer :: fonction de la fonction'
description: Définit deux valeurs.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Fonction de fonction du langage HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104030480"
---
# <a name="store2-function"></a><span data-ttu-id="18b82-104">Fonction de la Banque de fonctions</span><span class="sxs-lookup"><span data-stu-id="18b82-104">Store2 function</span></span>

<span data-ttu-id="18b82-105">Définit deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="18b82-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b82-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18b82-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="18b82-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18b82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b82-108">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18b82-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b82-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="18b82-109">Type: **uint**</span></span>

<span data-ttu-id="18b82-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="18b82-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="18b82-111">*valeurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18b82-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b82-112">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="18b82-112">Type: **uint2**</span></span>

<span data-ttu-id="18b82-113">Deux valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="18b82-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b82-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="18b82-114">Return value</span></span>

<span data-ttu-id="18b82-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="18b82-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b82-116">Notes</span><span class="sxs-lookup"><span data-stu-id="18b82-116">Remarks</span></span>

<span data-ttu-id="18b82-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="18b82-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="18b82-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="18b82-118">Vertex</span></span> | <span data-ttu-id="18b82-119">Forme</span><span class="sxs-lookup"><span data-stu-id="18b82-119">Hull</span></span> | <span data-ttu-id="18b82-120">Domain</span><span class="sxs-lookup"><span data-stu-id="18b82-120">Domain</span></span> | <span data-ttu-id="18b82-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="18b82-121">Geometry</span></span> | <span data-ttu-id="18b82-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="18b82-122">Pixel</span></span> | <span data-ttu-id="18b82-123">Compute</span><span class="sxs-lookup"><span data-stu-id="18b82-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="18b82-124">x</span><span class="sxs-lookup"><span data-stu-id="18b82-124">x</span></span>     | <span data-ttu-id="18b82-125">x</span><span class="sxs-lookup"><span data-stu-id="18b82-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="18b82-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18b82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b82-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="18b82-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="18b82-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="18b82-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




