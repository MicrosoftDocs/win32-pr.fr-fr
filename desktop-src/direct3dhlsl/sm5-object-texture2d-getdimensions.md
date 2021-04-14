---
title: 'Texture2D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2D :: GetDimensions,, fonction'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992037"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="1bd58-105">Texture2D :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="1bd58-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="1bd58-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="1bd58-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd58-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bd58-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="1bd58-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bd58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bd58-109">*MipLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bd58-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bd58-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1bd58-110">Type: **uint**</span></span>

<span data-ttu-id="1bd58-111">facultatif.</span><span class="sxs-lookup"><span data-stu-id="1bd58-111">Optional.</span></span> <span data-ttu-id="1bd58-112">Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).</span><span class="sxs-lookup"><span data-stu-id="1bd58-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="1bd58-113">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bd58-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bd58-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1bd58-114">Type: **uint**</span></span>

<span data-ttu-id="1bd58-115">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="1bd58-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="1bd58-116">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bd58-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bd58-117">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1bd58-117">Type: **uint**</span></span>

<span data-ttu-id="1bd58-118">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="1bd58-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="1bd58-119">*NumberOfLevels* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bd58-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bd58-120">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1bd58-120">Type: **uint**</span></span>

<span data-ttu-id="1bd58-121">Nombre de niveaux de mipmap (requiert également *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="1bd58-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bd58-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bd58-122">Return value</span></span>

<span data-ttu-id="1bd58-123">Rien</span><span class="sxs-lookup"><span data-stu-id="1bd58-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="1bd58-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1bd58-124">Remarks</span></span>

<span data-ttu-id="1bd58-125">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1bd58-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="1bd58-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1bd58-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1bd58-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="1bd58-127">Vertex</span></span> | <span data-ttu-id="1bd58-128">Forme</span><span class="sxs-lookup"><span data-stu-id="1bd58-128">Hull</span></span> | <span data-ttu-id="1bd58-129">Domain</span><span class="sxs-lookup"><span data-stu-id="1bd58-129">Domain</span></span> | <span data-ttu-id="1bd58-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1bd58-130">Geometry</span></span> | <span data-ttu-id="1bd58-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="1bd58-131">Pixel</span></span> | <span data-ttu-id="1bd58-132">Compute</span><span class="sxs-lookup"><span data-stu-id="1bd58-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1bd58-133">x</span><span class="sxs-lookup"><span data-stu-id="1bd58-133">x</span></span>     | <span data-ttu-id="1bd58-134">x</span><span class="sxs-lookup"><span data-stu-id="1bd58-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1bd58-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bd58-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd58-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="1bd58-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="1bd58-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1bd58-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




