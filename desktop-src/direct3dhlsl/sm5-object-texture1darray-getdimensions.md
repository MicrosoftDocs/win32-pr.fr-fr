---
title: 'Texture1DArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture1DArray :: GetDimensions,, fonction'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761762"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="57586-105">Texture1DArray :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="57586-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="57586-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="57586-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="57586-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57586-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="57586-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57586-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57586-109">*MipLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57586-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57586-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57586-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57586-111">facultatif.</span><span class="sxs-lookup"><span data-stu-id="57586-111">Optional.</span></span> <span data-ttu-id="57586-112">Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).</span><span class="sxs-lookup"><span data-stu-id="57586-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="57586-113">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57586-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57586-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57586-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57586-115">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="57586-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="57586-116">*Éléments* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57586-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57586-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57586-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57586-118">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="57586-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="57586-119">*NumberOfLevels* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57586-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57586-120">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57586-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57586-121">Nombre de niveaux de mipmap (requiert également *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="57586-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57586-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57586-122">Return value</span></span>

<span data-ttu-id="57586-123">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="57586-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57586-124">Notes</span><span class="sxs-lookup"><span data-stu-id="57586-124">Remarks</span></span>

<span data-ttu-id="57586-125">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="57586-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="57586-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="57586-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="57586-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="57586-127">Vertex</span></span> | <span data-ttu-id="57586-128">Forme</span><span class="sxs-lookup"><span data-stu-id="57586-128">Hull</span></span> | <span data-ttu-id="57586-129">Domain</span><span class="sxs-lookup"><span data-stu-id="57586-129">Domain</span></span> | <span data-ttu-id="57586-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="57586-130">Geometry</span></span> | <span data-ttu-id="57586-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="57586-131">Pixel</span></span> | <span data-ttu-id="57586-132">Compute</span><span class="sxs-lookup"><span data-stu-id="57586-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="57586-133">x</span><span class="sxs-lookup"><span data-stu-id="57586-133">x</span></span>     | <span data-ttu-id="57586-134">x</span><span class="sxs-lookup"><span data-stu-id="57586-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="57586-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57586-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57586-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="57586-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="57586-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="57586-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
