---
title: 'Buffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | Buffer :: GetDimensions,, fonction'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
keywords:
- GetDimensions, fonction HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973918"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="81848-105">Buffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="81848-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="81848-106">Obtient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="81848-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="81848-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81848-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="81848-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81848-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81848-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="81848-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81848-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="81848-110">Type: **uint**</span></span>

<span data-ttu-id="81848-111">Longueur, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="81848-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81848-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81848-112">Return value</span></span>

<span data-ttu-id="81848-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="81848-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81848-114">Notes</span><span class="sxs-lookup"><span data-stu-id="81848-114">Remarks</span></span>

<span data-ttu-id="81848-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="81848-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="81848-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="81848-116">Vertex</span></span> | <span data-ttu-id="81848-117">Forme</span><span class="sxs-lookup"><span data-stu-id="81848-117">Hull</span></span> | <span data-ttu-id="81848-118">Domain</span><span class="sxs-lookup"><span data-stu-id="81848-118">Domain</span></span> | <span data-ttu-id="81848-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="81848-119">Geometry</span></span> | <span data-ttu-id="81848-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="81848-120">Pixel</span></span> | <span data-ttu-id="81848-121">Compute</span><span class="sxs-lookup"><span data-stu-id="81848-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="81848-122">x</span><span class="sxs-lookup"><span data-stu-id="81848-122">x</span></span>      | <span data-ttu-id="81848-123">x</span><span class="sxs-lookup"><span data-stu-id="81848-123">x</span></span>    | <span data-ttu-id="81848-124">x</span><span class="sxs-lookup"><span data-stu-id="81848-124">x</span></span>      | <span data-ttu-id="81848-125">x</span><span class="sxs-lookup"><span data-stu-id="81848-125">x</span></span>        | <span data-ttu-id="81848-126">x</span><span class="sxs-lookup"><span data-stu-id="81848-126">x</span></span>     | <span data-ttu-id="81848-127">x</span><span class="sxs-lookup"><span data-stu-id="81848-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="81848-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81848-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81848-129">Buffer</span><span class="sxs-lookup"><span data-stu-id="81848-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="81848-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="81848-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




