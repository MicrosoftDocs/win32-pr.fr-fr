---
title: CheckAccessFullyMapped fonction)
description: Détermine si toutes les valeurs d’un échantillon, d’un regroupement ou d’une opération de chargement ont accédé à des vignettes mappées dans une ressource en mosaïque.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped fonction HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729372"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="30d0d-104">CheckAccessFullyMapped fonction)</span><span class="sxs-lookup"><span data-stu-id="30d0d-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="30d0d-105">Détermine si toutes les valeurs d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="30d0d-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="30d0d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30d0d-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="30d0d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30d0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30d0d-108">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30d0d-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d0d-109">Type : **uint \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="30d0d-109">Type: **uint\_only**</span></span>

<span data-ttu-id="30d0d-110">Valeur d’État retournée à partir d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** .</span><span class="sxs-lookup"><span data-stu-id="30d0d-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="30d0d-111">Étant donné que vous ne pouvez pas accéder directement à cette valeur d’État, vous devez la passer à **CheckAccessFullyMapped**.</span><span class="sxs-lookup"><span data-stu-id="30d0d-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30d0d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30d0d-112">Return value</span></span>

<span data-ttu-id="30d0d-113">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="30d0d-113">Type: **bool**</span></span>

<span data-ttu-id="30d0d-114">Retourne une valeur **booléenne** qui indique si toutes les valeurs d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="30d0d-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="30d0d-115">Retourne la **valeur true** si toutes les valeurs de l’opération ont accédé à des vignettes mappées ; Sinon, retourne **false** si des valeurs ont été extraites d’une vignette non mappée.</span><span class="sxs-lookup"><span data-stu-id="30d0d-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="30d0d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="30d0d-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="30d0d-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="30d0d-117">Minimum Shader Model</span></span>

<span data-ttu-id="30d0d-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="30d0d-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="30d0d-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="30d0d-119">Shader Model</span></span>                                                                | <span data-ttu-id="30d0d-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="30d0d-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="30d0d-121">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="30d0d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="30d0d-122">Oui</span><span class="sxs-lookup"><span data-stu-id="30d0d-122">yes</span></span>       |



 

<span data-ttu-id="30d0d-123">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="30d0d-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="30d0d-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="30d0d-124">Vertex</span></span> | <span data-ttu-id="30d0d-125">Forme</span><span class="sxs-lookup"><span data-stu-id="30d0d-125">Hull</span></span> | <span data-ttu-id="30d0d-126">Domain</span><span class="sxs-lookup"><span data-stu-id="30d0d-126">Domain</span></span> | <span data-ttu-id="30d0d-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="30d0d-127">Geometry</span></span> | <span data-ttu-id="30d0d-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="30d0d-128">Pixel</span></span> | <span data-ttu-id="30d0d-129">Compute</span><span class="sxs-lookup"><span data-stu-id="30d0d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="30d0d-130">x</span><span class="sxs-lookup"><span data-stu-id="30d0d-130">x</span></span>     | <span data-ttu-id="30d0d-131">x</span><span class="sxs-lookup"><span data-stu-id="30d0d-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="30d0d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30d0d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d0d-133">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="30d0d-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 