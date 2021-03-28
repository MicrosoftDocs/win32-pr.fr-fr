---
title: 'Texture1D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture1D :: GetDimensions,, fonction'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530706"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="4feb3-105">Texture1D :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="4feb3-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="4feb3-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="4feb3-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4feb3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4feb3-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="4feb3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4feb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4feb3-109">*MipLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4feb3-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4feb3-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4feb3-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4feb3-111">facultatif.</span><span class="sxs-lookup"><span data-stu-id="4feb3-111">Optional.</span></span> <span data-ttu-id="4feb3-112">Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).</span><span class="sxs-lookup"><span data-stu-id="4feb3-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="4feb3-113">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4feb3-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4feb3-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4feb3-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4feb3-115">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="4feb3-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="4feb3-116">*NumberOfLevels* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4feb3-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4feb3-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4feb3-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4feb3-118">Nombre de niveaux de mipmap (requiert également *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="4feb3-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4feb3-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4feb3-119">Return value</span></span>

<span data-ttu-id="4feb3-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4feb3-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4feb3-121">Notes</span><span class="sxs-lookup"><span data-stu-id="4feb3-121">Remarks</span></span>

<span data-ttu-id="4feb3-122">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4feb3-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="4feb3-123">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4feb3-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4feb3-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="4feb3-124">Vertex</span></span> | <span data-ttu-id="4feb3-125">Forme</span><span class="sxs-lookup"><span data-stu-id="4feb3-125">Hull</span></span> | <span data-ttu-id="4feb3-126">Domain</span><span class="sxs-lookup"><span data-stu-id="4feb3-126">Domain</span></span> | <span data-ttu-id="4feb3-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4feb3-127">Geometry</span></span> | <span data-ttu-id="4feb3-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="4feb3-128">Pixel</span></span> | <span data-ttu-id="4feb3-129">Compute</span><span class="sxs-lookup"><span data-stu-id="4feb3-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4feb3-130">x</span><span class="sxs-lookup"><span data-stu-id="4feb3-130">x</span></span>     | <span data-ttu-id="4feb3-131">x</span><span class="sxs-lookup"><span data-stu-id="4feb3-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4feb3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4feb3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4feb3-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4feb3-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="4feb3-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4feb3-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
