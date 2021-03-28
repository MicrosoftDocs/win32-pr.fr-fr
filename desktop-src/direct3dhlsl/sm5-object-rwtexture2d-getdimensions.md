---
title: 'RWTexture2D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | RWTexture2D :: GetDimensions,, fonction'
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116147"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="b50dc-105">RWTexture2D :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="b50dc-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="b50dc-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b50dc-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50dc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b50dc-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="b50dc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b50dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b50dc-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b50dc-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b50dc-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b50dc-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b50dc-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="b50dc-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="b50dc-112">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b50dc-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b50dc-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b50dc-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b50dc-114">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="b50dc-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b50dc-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b50dc-115">Return value</span></span>

<span data-ttu-id="b50dc-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b50dc-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b50dc-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b50dc-117">Remarks</span></span>

<span data-ttu-id="b50dc-118">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b50dc-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="b50dc-119">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b50dc-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b50dc-120">Sommet</span><span class="sxs-lookup"><span data-stu-id="b50dc-120">Vertex</span></span> | <span data-ttu-id="b50dc-121">Forme</span><span class="sxs-lookup"><span data-stu-id="b50dc-121">Hull</span></span> | <span data-ttu-id="b50dc-122">Domain</span><span class="sxs-lookup"><span data-stu-id="b50dc-122">Domain</span></span> | <span data-ttu-id="b50dc-123">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b50dc-123">Geometry</span></span> | <span data-ttu-id="b50dc-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="b50dc-124">Pixel</span></span> | <span data-ttu-id="b50dc-125">Compute</span><span class="sxs-lookup"><span data-stu-id="b50dc-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b50dc-126">x</span><span class="sxs-lookup"><span data-stu-id="b50dc-126">x</span></span>     | <span data-ttu-id="b50dc-127">x</span><span class="sxs-lookup"><span data-stu-id="b50dc-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b50dc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b50dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50dc-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="b50dc-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="b50dc-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b50dc-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
