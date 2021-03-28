---
title: 'Texture2DMS :: Load (int, int), fonction'
description: 'Obtient une valeur. | Texture2DMS :: Load (int, int), fonction'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Charger la fonction DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974167"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="ab650-105">Texture2DMS :: Load (int, int), fonction</span><span class="sxs-lookup"><span data-stu-id="ab650-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="ab650-106">Obtient une valeur.</span><span class="sxs-lookup"><span data-stu-id="ab650-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab650-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab650-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="ab650-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab650-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab650-109">*Coord* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab650-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab650-110">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="ab650-110">Type: **int2**</span></span>

<span data-ttu-id="ab650-111">Emplacement d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ab650-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="ab650-112">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab650-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab650-113">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab650-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab650-114">Exemple d’index.</span><span class="sxs-lookup"><span data-stu-id="ab650-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab650-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab650-115">Return value</span></span>

<span data-ttu-id="ab650-116">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="ab650-116">Type: **T**</span></span>

<span data-ttu-id="ab650-117">Une valeur, dont le type correspond au type de modèle de texture.</span><span class="sxs-lookup"><span data-stu-id="ab650-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab650-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ab650-118">Remarks</span></span>

<span data-ttu-id="ab650-119">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ab650-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="ab650-120">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ab650-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ab650-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="ab650-121">Vertex</span></span> | <span data-ttu-id="ab650-122">Forme</span><span class="sxs-lookup"><span data-stu-id="ab650-122">Hull</span></span> | <span data-ttu-id="ab650-123">Domain</span><span class="sxs-lookup"><span data-stu-id="ab650-123">Domain</span></span> | <span data-ttu-id="ab650-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ab650-124">Geometry</span></span> | <span data-ttu-id="ab650-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="ab650-125">Pixel</span></span> | <span data-ttu-id="ab650-126">Compute</span><span class="sxs-lookup"><span data-stu-id="ab650-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ab650-127">x</span><span class="sxs-lookup"><span data-stu-id="ab650-127">x</span></span>     | <span data-ttu-id="ab650-128">x</span><span class="sxs-lookup"><span data-stu-id="ab650-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ab650-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab650-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab650-130">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="ab650-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="ab650-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ab650-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
