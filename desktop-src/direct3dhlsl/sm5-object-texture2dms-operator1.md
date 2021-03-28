---
title: 'Texture2DMS :: Operator, fonction'
description: Récupère une valeur de la ressource à l’emplacement fourni à l’exemple d’index 0.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104971851"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="9b619-104">Texture2DMS :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="9b619-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="9b619-105">Récupère une valeur de la ressource à l’emplacement fourni à l’exemple d’index 0.</span><span class="sxs-lookup"><span data-stu-id="9b619-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b619-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b619-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="9b619-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b619-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b619-108">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b619-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b619-109">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="9b619-109">Type: **uint2**</span></span>

<span data-ttu-id="9b619-110">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="9b619-110">The index position.</span></span> <span data-ttu-id="9b619-111">Contient les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="9b619-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b619-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b619-112">Return value</span></span>

<span data-ttu-id="9b619-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="9b619-113">Type: **R**</span></span>

<span data-ttu-id="9b619-114">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9b619-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b619-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9b619-115">Remarks</span></span>

<span data-ttu-id="9b619-116">Pour sélectionner un exemple particulier, reportez-vous à [**exemple. \[Opérateur \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9b619-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="9b619-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9b619-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9b619-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="9b619-118">Vertex</span></span> | <span data-ttu-id="9b619-119">Forme</span><span class="sxs-lookup"><span data-stu-id="9b619-119">Hull</span></span> | <span data-ttu-id="9b619-120">Domain</span><span class="sxs-lookup"><span data-stu-id="9b619-120">Domain</span></span> | <span data-ttu-id="9b619-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9b619-121">Geometry</span></span> | <span data-ttu-id="9b619-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="9b619-122">Pixel</span></span> | <span data-ttu-id="9b619-123">Compute</span><span class="sxs-lookup"><span data-stu-id="9b619-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b619-124">x</span><span class="sxs-lookup"><span data-stu-id="9b619-124">x</span></span>      | <span data-ttu-id="9b619-125">x</span><span class="sxs-lookup"><span data-stu-id="9b619-125">x</span></span>    | <span data-ttu-id="9b619-126">x</span><span class="sxs-lookup"><span data-stu-id="9b619-126">x</span></span>      | <span data-ttu-id="9b619-127">x</span><span class="sxs-lookup"><span data-stu-id="9b619-127">x</span></span>        | <span data-ttu-id="9b619-128">x</span><span class="sxs-lookup"><span data-stu-id="9b619-128">x</span></span>     | <span data-ttu-id="9b619-129">x</span><span class="sxs-lookup"><span data-stu-id="9b619-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9b619-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b619-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b619-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="9b619-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="9b619-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9b619-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




