---
description: Clone, ou copie, un contrôleur d’animation.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'ID3DXAnimationController :: CloneAnimationController, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323297"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="4651f-103">ID3DXAnimationController :: CloneAnimationController, méthode</span><span class="sxs-lookup"><span data-stu-id="4651f-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="4651f-104">Clone, ou copie, un contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="4651f-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4651f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4651f-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="4651f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4651f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4651f-107">*MaxNumAnimationOutputs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4651f-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4651f-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4651f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4651f-109">Nombre maximal de sorties d’animation que le contrôleur peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4651f-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="4651f-110">*MaxNumAnimationSets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4651f-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4651f-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4651f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4651f-112">Nombre maximal de jeux d’animations que le contrôleur peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4651f-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="4651f-113">*MaxNumTracks* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4651f-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4651f-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4651f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4651f-115">Nombre maximal de pistes que le contrôleur peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4651f-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="4651f-116">*MaxNumEvents* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4651f-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4651f-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4651f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4651f-118">Nombre maximal d’événements que le contrôleur peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4651f-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="4651f-119">*ppAnimController* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4651f-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4651f-120">Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="4651f-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="4651f-121">Adresse d’un pointeur vers le contrôleur d’animation [**ID3DXAnimationController**](id3dxanimationcontroller.md) cloné.</span><span class="sxs-lookup"><span data-stu-id="4651f-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4651f-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4651f-122">Return value</span></span>

<span data-ttu-id="4651f-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4651f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4651f-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4651f-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4651f-125">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4651f-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4651f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4651f-126">Requirements</span></span>



| <span data-ttu-id="4651f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4651f-127">Requirement</span></span> | <span data-ttu-id="4651f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4651f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4651f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4651f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4651f-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4651f-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4651f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4651f-131">Library</span></span><br/> | <dl> <span data-ttu-id="4651f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4651f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4651f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4651f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4651f-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4651f-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
