---
title: RWStructuredBuffer ::D fonction ecrementCounter (HTTPServ. h)
description: Décrémente le compteur masqué de l’objet.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter fonction HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974635"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="1240e-104">DecrementCounter fonction)</span><span class="sxs-lookup"><span data-stu-id="1240e-104">DecrementCounter function</span></span>

<span data-ttu-id="1240e-105">Décrémente le compteur masqué de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1240e-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1240e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1240e-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="1240e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1240e-107">Parameters</span></span>

<span data-ttu-id="1240e-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1240e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1240e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1240e-109">Return value</span></span>

<span data-ttu-id="1240e-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1240e-110">Type: **uint**</span></span>

<span data-ttu-id="1240e-111">Valeur de compteur après décrémentation.</span><span class="sxs-lookup"><span data-stu-id="1240e-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1240e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1240e-112">Remarks</span></span>

<span data-ttu-id="1240e-113">La vue d’accès non ordonnée liée doit avoir un compteur de l' [**\_ \_ \_ \_ indicateur UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) défini au cours de creationfor cette méthode pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="1240e-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="1240e-114">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1240e-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1240e-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="1240e-115">Vertex</span></span> | <span data-ttu-id="1240e-116">Forme</span><span class="sxs-lookup"><span data-stu-id="1240e-116">Hull</span></span> | <span data-ttu-id="1240e-117">Domain</span><span class="sxs-lookup"><span data-stu-id="1240e-117">Domain</span></span> | <span data-ttu-id="1240e-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1240e-118">Geometry</span></span> | <span data-ttu-id="1240e-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="1240e-119">Pixel</span></span> | <span data-ttu-id="1240e-120">Compute</span><span class="sxs-lookup"><span data-stu-id="1240e-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1240e-121">x</span><span class="sxs-lookup"><span data-stu-id="1240e-121">x</span></span>     | <span data-ttu-id="1240e-122">x</span><span class="sxs-lookup"><span data-stu-id="1240e-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="1240e-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1240e-123">Requirements</span></span>



| <span data-ttu-id="1240e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1240e-124">Requirement</span></span> | <span data-ttu-id="1240e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1240e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1240e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1240e-126">Header</span></span><br/> | <dl> <span data-ttu-id="1240e-127"><dt>HTTPServ. h</dt></span><span class="sxs-lookup"><span data-stu-id="1240e-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1240e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1240e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1240e-129">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="1240e-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="1240e-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1240e-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

