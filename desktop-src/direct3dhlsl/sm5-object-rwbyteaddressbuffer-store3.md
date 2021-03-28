---
title: 'RWByteAddressBuffer :: Store3, fonction'
description: Définit trois valeurs.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Store3 fonction HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313345"
---
# <a name="store3-function"></a><span data-ttu-id="eef35-104">Store3 fonction)</span><span class="sxs-lookup"><span data-stu-id="eef35-104">Store3 function</span></span>

<span data-ttu-id="eef35-105">Définit trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="eef35-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef35-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eef35-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="eef35-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eef35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef35-108">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eef35-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eef35-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="eef35-109">Type: **uint**</span></span>

<span data-ttu-id="eef35-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="eef35-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="eef35-111">*valeurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eef35-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eef35-112">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="eef35-112">Type: **uint3**</span></span>

<span data-ttu-id="eef35-113">Trois valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="eef35-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef35-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eef35-114">Return value</span></span>

<span data-ttu-id="eef35-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eef35-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eef35-116">Notes</span><span class="sxs-lookup"><span data-stu-id="eef35-116">Remarks</span></span>

<span data-ttu-id="eef35-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="eef35-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eef35-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="eef35-118">Vertex</span></span> | <span data-ttu-id="eef35-119">Forme</span><span class="sxs-lookup"><span data-stu-id="eef35-119">Hull</span></span> | <span data-ttu-id="eef35-120">Domain</span><span class="sxs-lookup"><span data-stu-id="eef35-120">Domain</span></span> | <span data-ttu-id="eef35-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="eef35-121">Geometry</span></span> | <span data-ttu-id="eef35-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="eef35-122">Pixel</span></span> | <span data-ttu-id="eef35-123">Compute</span><span class="sxs-lookup"><span data-stu-id="eef35-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="eef35-124">x</span><span class="sxs-lookup"><span data-stu-id="eef35-124">x</span></span>     | <span data-ttu-id="eef35-125">x</span><span class="sxs-lookup"><span data-stu-id="eef35-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eef35-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eef35-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef35-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="eef35-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="eef35-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="eef35-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




