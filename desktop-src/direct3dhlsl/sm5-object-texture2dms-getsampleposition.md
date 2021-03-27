---
title: 'Texture2DMS :: GetSamplePosition, fonction'
description: Retourne la position d’échantillon pour l’exemple d’index fourni.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- GetSamplePosition fonction HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508273"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="edec2-104">Texture2DMS :: GetSamplePosition, fonction</span><span class="sxs-lookup"><span data-stu-id="edec2-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="edec2-105">Retourne la position d’échantillon pour l’exemple d’index fourni.</span><span class="sxs-lookup"><span data-stu-id="edec2-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="edec2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edec2-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="edec2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edec2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edec2-108">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edec2-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edec2-109">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="edec2-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="edec2-110">Index de base zéro d’un emplacement d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="edec2-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edec2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edec2-111">Return value</span></span>

<span data-ttu-id="edec2-112">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="edec2-112">Type: **float2**</span></span>

<span data-ttu-id="edec2-113">Exemple d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="edec2-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="edec2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="edec2-114">Remarks</span></span>

<span data-ttu-id="edec2-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="edec2-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="edec2-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="edec2-116">Vertex</span></span> | <span data-ttu-id="edec2-117">Forme</span><span class="sxs-lookup"><span data-stu-id="edec2-117">Hull</span></span> | <span data-ttu-id="edec2-118">Domain</span><span class="sxs-lookup"><span data-stu-id="edec2-118">Domain</span></span> | <span data-ttu-id="edec2-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="edec2-119">Geometry</span></span> | <span data-ttu-id="edec2-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="edec2-120">Pixel</span></span> | <span data-ttu-id="edec2-121">Compute</span><span class="sxs-lookup"><span data-stu-id="edec2-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="edec2-122">x</span><span class="sxs-lookup"><span data-stu-id="edec2-122">x</span></span>      | <span data-ttu-id="edec2-123">x</span><span class="sxs-lookup"><span data-stu-id="edec2-123">x</span></span>    | <span data-ttu-id="edec2-124">x</span><span class="sxs-lookup"><span data-stu-id="edec2-124">x</span></span>      | <span data-ttu-id="edec2-125">x</span><span class="sxs-lookup"><span data-stu-id="edec2-125">x</span></span>        | <span data-ttu-id="edec2-126">x</span><span class="sxs-lookup"><span data-stu-id="edec2-126">x</span></span>     | <span data-ttu-id="edec2-127">x</span><span class="sxs-lookup"><span data-stu-id="edec2-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="edec2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edec2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edec2-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="edec2-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="edec2-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="edec2-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
