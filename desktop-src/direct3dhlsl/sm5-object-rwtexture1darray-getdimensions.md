---
title: 'RWTexture1DArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | RWTexture1DArray :: GetDimensions,, fonction'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211522"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="f7430-105">RWTexture1DArray :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="f7430-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="f7430-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="f7430-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7430-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7430-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="f7430-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7430-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7430-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f7430-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7430-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7430-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f7430-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="f7430-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="f7430-112">*Éléments* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f7430-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7430-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7430-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f7430-114">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f7430-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7430-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f7430-115">Return value</span></span>

<span data-ttu-id="f7430-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f7430-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7430-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f7430-117">Remarks</span></span>

<span data-ttu-id="f7430-118">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f7430-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="f7430-119">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="f7430-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f7430-120">Sommet</span><span class="sxs-lookup"><span data-stu-id="f7430-120">Vertex</span></span> | <span data-ttu-id="f7430-121">Forme</span><span class="sxs-lookup"><span data-stu-id="f7430-121">Hull</span></span> | <span data-ttu-id="f7430-122">Domain</span><span class="sxs-lookup"><span data-stu-id="f7430-122">Domain</span></span> | <span data-ttu-id="f7430-123">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f7430-123">Geometry</span></span> | <span data-ttu-id="f7430-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="f7430-124">Pixel</span></span> | <span data-ttu-id="f7430-125">Compute</span><span class="sxs-lookup"><span data-stu-id="f7430-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f7430-126">x</span><span class="sxs-lookup"><span data-stu-id="f7430-126">x</span></span>     | <span data-ttu-id="f7430-127">x</span><span class="sxs-lookup"><span data-stu-id="f7430-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f7430-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7430-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7430-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="f7430-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="f7430-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f7430-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
