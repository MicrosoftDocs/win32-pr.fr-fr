---
title: 'Texture2DMSArray :: GetSamplePosition, fonction'
description: 'Obtient la position de l’échantillon spécifié. | Texture2DMSArray :: GetSamplePosition, fonction'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211628"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="28067-105">Texture2DMSArray :: GetSamplePosition, fonction</span><span class="sxs-lookup"><span data-stu-id="28067-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="28067-106">Obtient la position de l’échantillon spécifié.</span><span class="sxs-lookup"><span data-stu-id="28067-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="28067-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28067-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="28067-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28067-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28067-109">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28067-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28067-110">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="28067-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="28067-111">Index de base zéro d’un emplacement d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="28067-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28067-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28067-112">Return value</span></span>

<span data-ttu-id="28067-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="28067-113">Type: **float2**</span></span>

<span data-ttu-id="28067-114">Exemple d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="28067-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="28067-115">Notes</span><span class="sxs-lookup"><span data-stu-id="28067-115">Remarks</span></span>

<span data-ttu-id="28067-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="28067-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="28067-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="28067-117">Vertex</span></span> | <span data-ttu-id="28067-118">Forme</span><span class="sxs-lookup"><span data-stu-id="28067-118">Hull</span></span> | <span data-ttu-id="28067-119">Domain</span><span class="sxs-lookup"><span data-stu-id="28067-119">Domain</span></span> | <span data-ttu-id="28067-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="28067-120">Geometry</span></span> | <span data-ttu-id="28067-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="28067-121">Pixel</span></span> | <span data-ttu-id="28067-122">Compute</span><span class="sxs-lookup"><span data-stu-id="28067-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="28067-123">x</span><span class="sxs-lookup"><span data-stu-id="28067-123">x</span></span>      | <span data-ttu-id="28067-124">x</span><span class="sxs-lookup"><span data-stu-id="28067-124">x</span></span>    | <span data-ttu-id="28067-125">x</span><span class="sxs-lookup"><span data-stu-id="28067-125">x</span></span>      | <span data-ttu-id="28067-126">x</span><span class="sxs-lookup"><span data-stu-id="28067-126">x</span></span>        | <span data-ttu-id="28067-127">x</span><span class="sxs-lookup"><span data-stu-id="28067-127">x</span></span>     | <span data-ttu-id="28067-128">x</span><span class="sxs-lookup"><span data-stu-id="28067-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="28067-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28067-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28067-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="28067-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="28067-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="28067-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
