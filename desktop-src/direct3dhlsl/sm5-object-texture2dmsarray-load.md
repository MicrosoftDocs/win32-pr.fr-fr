---
title: 'Texture2DMSArray :: Load (int, int), fonction'
description: 'Obtient une valeur. | Texture2DMSArray :: Load (int, int), fonction'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953745"
---
# <a name="texture2dmsarrayloadintint-function"></a><span data-ttu-id="3287e-105">Texture2DMSArray :: Load (int, int), fonction</span><span class="sxs-lookup"><span data-stu-id="3287e-105">Texture2DMSArray::Load(int,int) function</span></span>

<span data-ttu-id="3287e-106">Obtient une valeur.</span><span class="sxs-lookup"><span data-stu-id="3287e-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3287e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3287e-107">Syntax</span></span>

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="3287e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3287e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3287e-109">*Coord* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3287e-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3287e-110">Type : **Int3**</span><span class="sxs-lookup"><span data-stu-id="3287e-110">Type: **int3**</span></span>

<span data-ttu-id="3287e-111">Emplacement d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3287e-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="3287e-112">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3287e-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3287e-113">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3287e-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3287e-114">Exemple d’index.</span><span class="sxs-lookup"><span data-stu-id="3287e-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3287e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3287e-115">Return value</span></span>

<span data-ttu-id="3287e-116">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="3287e-116">Type: **T**</span></span>

<span data-ttu-id="3287e-117">Une valeur, dont le type correspond au type de modèle de texture.</span><span class="sxs-lookup"><span data-stu-id="3287e-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3287e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3287e-118">Remarks</span></span>

<span data-ttu-id="3287e-119">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3287e-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="3287e-120">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3287e-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3287e-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="3287e-121">Vertex</span></span> | <span data-ttu-id="3287e-122">Forme</span><span class="sxs-lookup"><span data-stu-id="3287e-122">Hull</span></span> | <span data-ttu-id="3287e-123">Domain</span><span class="sxs-lookup"><span data-stu-id="3287e-123">Domain</span></span> | <span data-ttu-id="3287e-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3287e-124">Geometry</span></span> | <span data-ttu-id="3287e-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="3287e-125">Pixel</span></span> | <span data-ttu-id="3287e-126">Compute</span><span class="sxs-lookup"><span data-stu-id="3287e-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3287e-127">x</span><span class="sxs-lookup"><span data-stu-id="3287e-127">x</span></span>     | <span data-ttu-id="3287e-128">x</span><span class="sxs-lookup"><span data-stu-id="3287e-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3287e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3287e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3287e-130">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="3287e-130">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="3287e-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3287e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
