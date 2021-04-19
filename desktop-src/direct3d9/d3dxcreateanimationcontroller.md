---
description: Crée un objet contrôleur d’animation.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: D3DXCreateAnimationController, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535812"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="87e32-103">D3DXCreateAnimationController fonction)</span><span class="sxs-lookup"><span data-stu-id="87e32-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="87e32-104">Crée un objet contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="87e32-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87e32-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="87e32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87e32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e32-107">*MaxNumAnimationOutputs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87e32-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e32-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87e32-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87e32-109">Nombre maximal de sorties d’animation que le contrôleur peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="87e32-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="87e32-110">*MaxNumAnimationSets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87e32-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e32-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87e32-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87e32-112">Nombre maximal de jeux d’animations pouvant être mélangés.</span><span class="sxs-lookup"><span data-stu-id="87e32-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="87e32-113">*MaxNumTracks* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87e32-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e32-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87e32-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87e32-115">Nombre maximal de jeux d’animations pouvant être mélangés simultanément.</span><span class="sxs-lookup"><span data-stu-id="87e32-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="87e32-116">*MaxNumEvents* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87e32-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e32-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87e32-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87e32-118">Nombre maximal d’événements en attente pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="87e32-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="87e32-119">*ppAnimController* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="87e32-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e32-120">Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="87e32-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="87e32-121">Pointeur vers l’objet de contrôleur d’animation créé.</span><span class="sxs-lookup"><span data-stu-id="87e32-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="87e32-122">Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="87e32-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e32-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87e32-123">Return value</span></span>

<span data-ttu-id="87e32-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87e32-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87e32-125">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87e32-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="87e32-126">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="87e32-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e32-127">Notes</span><span class="sxs-lookup"><span data-stu-id="87e32-127">Remarks</span></span>

<span data-ttu-id="87e32-128">Un contrôleur d’animation contrôle un mélangeur d’animation.</span><span class="sxs-lookup"><span data-stu-id="87e32-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="87e32-129">Le contrôleur ajoute des méthodes permettant de modifier les paramètres de fusion dans le temps pour permettre des transitions lisses.</span><span class="sxs-lookup"><span data-stu-id="87e32-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e32-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87e32-130">Requirements</span></span>



| <span data-ttu-id="87e32-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87e32-131">Requirement</span></span> | <span data-ttu-id="87e32-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="87e32-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e32-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="87e32-133">Header</span></span><br/>  | <dl> <span data-ttu-id="87e32-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e32-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="87e32-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87e32-135">Library</span></span><br/> | <dl> <span data-ttu-id="87e32-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87e32-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87e32-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87e32-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e32-138">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="87e32-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
