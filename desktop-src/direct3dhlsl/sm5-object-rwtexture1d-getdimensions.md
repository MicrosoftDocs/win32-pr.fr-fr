---
title: 'RWTexture1D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | RWTexture1D :: GetDimensions,, fonction'
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973911"
---
# <a name="rwtexture1dgetdimensions-function"></a><span data-ttu-id="92de1-105">RWTexture1D :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="92de1-105">RWTexture1D::GetDimensions function</span></span>

<span data-ttu-id="92de1-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="92de1-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="92de1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92de1-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a><span data-ttu-id="92de1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92de1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92de1-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92de1-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92de1-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92de1-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92de1-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="92de1-111">The resource width, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92de1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92de1-112">Return value</span></span>

<span data-ttu-id="92de1-113">Rien</span><span class="sxs-lookup"><span data-stu-id="92de1-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="92de1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="92de1-114">Remarks</span></span>

<span data-ttu-id="92de1-115">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="92de1-115">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



<span data-ttu-id="92de1-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="92de1-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="92de1-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="92de1-117">Vertex</span></span> | <span data-ttu-id="92de1-118">Forme</span><span class="sxs-lookup"><span data-stu-id="92de1-118">Hull</span></span> | <span data-ttu-id="92de1-119">Domain</span><span class="sxs-lookup"><span data-stu-id="92de1-119">Domain</span></span> | <span data-ttu-id="92de1-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="92de1-120">Geometry</span></span> | <span data-ttu-id="92de1-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="92de1-121">Pixel</span></span> | <span data-ttu-id="92de1-122">Compute</span><span class="sxs-lookup"><span data-stu-id="92de1-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="92de1-123">x</span><span class="sxs-lookup"><span data-stu-id="92de1-123">x</span></span>     | <span data-ttu-id="92de1-124">x</span><span class="sxs-lookup"><span data-stu-id="92de1-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="92de1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92de1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92de1-126">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="92de1-126">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="92de1-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="92de1-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
