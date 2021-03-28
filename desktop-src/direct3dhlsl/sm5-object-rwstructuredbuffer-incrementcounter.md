---
title: 'RWStructuredBuffer :: IncrementCounter, fonction (HTTPServ. h)'
description: Incrémente le compteur masqué de l’objet.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter fonction HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323174"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="05f45-104">IncrementCounter fonction)</span><span class="sxs-lookup"><span data-stu-id="05f45-104">IncrementCounter function</span></span>

<span data-ttu-id="05f45-105">Incrémente le compteur masqué de l’objet.</span><span class="sxs-lookup"><span data-stu-id="05f45-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f45-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05f45-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="05f45-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05f45-107">Parameters</span></span>

<span data-ttu-id="05f45-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="05f45-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05f45-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05f45-109">Return value</span></span>

<span data-ttu-id="05f45-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="05f45-110">Type: **uint**</span></span>

<span data-ttu-id="05f45-111">Valeur de compteur pré-incrémentée.</span><span class="sxs-lookup"><span data-stu-id="05f45-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f45-112">Notes</span><span class="sxs-lookup"><span data-stu-id="05f45-112">Remarks</span></span>

<span data-ttu-id="05f45-113">Pour que cette méthode fonctionne, la vue d’accès non triée liée doit avoir un [**\_ \_ \_ \_ compteur d’indicateur UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) défini lors de la création.</span><span class="sxs-lookup"><span data-stu-id="05f45-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="05f45-114">Une ressource structurée peut être indexée en fonction des noms de composants des structures.</span><span class="sxs-lookup"><span data-stu-id="05f45-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="05f45-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="05f45-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="05f45-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="05f45-116">Vertex</span></span> | <span data-ttu-id="05f45-117">Forme</span><span class="sxs-lookup"><span data-stu-id="05f45-117">Hull</span></span> | <span data-ttu-id="05f45-118">Domain</span><span class="sxs-lookup"><span data-stu-id="05f45-118">Domain</span></span> | <span data-ttu-id="05f45-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="05f45-119">Geometry</span></span> | <span data-ttu-id="05f45-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="05f45-120">Pixel</span></span> | <span data-ttu-id="05f45-121">Compute</span><span class="sxs-lookup"><span data-stu-id="05f45-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="05f45-122">x</span><span class="sxs-lookup"><span data-stu-id="05f45-122">x</span></span>     | <span data-ttu-id="05f45-123">x</span><span class="sxs-lookup"><span data-stu-id="05f45-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="05f45-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="05f45-124">Requirements</span></span>



| <span data-ttu-id="05f45-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05f45-125">Requirement</span></span> | <span data-ttu-id="05f45-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="05f45-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05f45-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="05f45-127">Header</span></span><br/> | <dl> <span data-ttu-id="05f45-128"><dt>HTTPServ. h</dt></span><span class="sxs-lookup"><span data-stu-id="05f45-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f45-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05f45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f45-130">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="05f45-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="05f45-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="05f45-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

