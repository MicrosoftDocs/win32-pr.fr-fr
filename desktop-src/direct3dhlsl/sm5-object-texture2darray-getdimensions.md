---
title: 'Texture2DArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2DArray :: GetDimensions,, fonction'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973907"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="fb36f-105">Texture2DArray :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="fb36f-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="fb36f-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="fb36f-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb36f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb36f-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="fb36f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb36f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb36f-109">*MipLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb36f-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb36f-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb36f-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb36f-111">facultatif.</span><span class="sxs-lookup"><span data-stu-id="fb36f-111">Optional.</span></span> <span data-ttu-id="fb36f-112">Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).</span><span class="sxs-lookup"><span data-stu-id="fb36f-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="fb36f-113">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb36f-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb36f-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb36f-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb36f-115">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="fb36f-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="fb36f-116">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb36f-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb36f-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb36f-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb36f-118">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="fb36f-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="fb36f-119">*Éléments* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb36f-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb36f-120">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb36f-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb36f-121">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="fb36f-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="fb36f-122">*NumberOfLevels* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb36f-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb36f-123">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb36f-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb36f-124">Nombre de niveaux de mipmap (requiert également *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="fb36f-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb36f-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb36f-125">Return value</span></span>

<span data-ttu-id="fb36f-126">Rien</span><span class="sxs-lookup"><span data-stu-id="fb36f-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="fb36f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="fb36f-127">Remarks</span></span>

<span data-ttu-id="fb36f-128">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fb36f-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="fb36f-129">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="fb36f-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fb36f-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="fb36f-130">Vertex</span></span> | <span data-ttu-id="fb36f-131">Forme</span><span class="sxs-lookup"><span data-stu-id="fb36f-131">Hull</span></span> | <span data-ttu-id="fb36f-132">Domain</span><span class="sxs-lookup"><span data-stu-id="fb36f-132">Domain</span></span> | <span data-ttu-id="fb36f-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="fb36f-133">Geometry</span></span> | <span data-ttu-id="fb36f-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="fb36f-134">Pixel</span></span> | <span data-ttu-id="fb36f-135">Compute</span><span class="sxs-lookup"><span data-stu-id="fb36f-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fb36f-136">x</span><span class="sxs-lookup"><span data-stu-id="fb36f-136">x</span></span>     | <span data-ttu-id="fb36f-137">x</span><span class="sxs-lookup"><span data-stu-id="fb36f-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fb36f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb36f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb36f-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fb36f-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="fb36f-140">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="fb36f-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
