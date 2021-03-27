---
title: 'RWTexture3D :: Operator, fonction'
description: Retourne une variable de ressource d’un RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
keywords:
- Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104971839"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="daa30-104">RWTexture3D :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="daa30-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="daa30-105">Retourne une variable de ressource d’un [**RWTexture3D**](sm5-object-rwtexture3d.md).</span><span class="sxs-lookup"><span data-stu-id="daa30-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="daa30-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daa30-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="daa30-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daa30-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa30-108">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="daa30-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daa30-109">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="daa30-109">Type: **uint3**</span></span>

<span data-ttu-id="daa30-110">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="daa30-110">The index position.</span></span> <span data-ttu-id="daa30-111">Contient les coordonnées (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="daa30-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daa30-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="daa30-112">Return value</span></span>

<span data-ttu-id="daa30-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="daa30-113">Type: **R**</span></span>

<span data-ttu-id="daa30-114">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="daa30-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="daa30-115">Notes</span><span class="sxs-lookup"><span data-stu-id="daa30-115">Remarks</span></span>

<span data-ttu-id="daa30-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="daa30-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="daa30-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="daa30-117">Vertex</span></span> | <span data-ttu-id="daa30-118">Forme</span><span class="sxs-lookup"><span data-stu-id="daa30-118">Hull</span></span> | <span data-ttu-id="daa30-119">Domain</span><span class="sxs-lookup"><span data-stu-id="daa30-119">Domain</span></span> | <span data-ttu-id="daa30-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="daa30-120">Geometry</span></span> | <span data-ttu-id="daa30-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="daa30-121">Pixel</span></span> | <span data-ttu-id="daa30-122">Compute</span><span class="sxs-lookup"><span data-stu-id="daa30-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="daa30-123">x</span><span class="sxs-lookup"><span data-stu-id="daa30-123">x</span></span>     | <span data-ttu-id="daa30-124">x</span><span class="sxs-lookup"><span data-stu-id="daa30-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="daa30-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daa30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa30-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="daa30-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="daa30-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="daa30-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




