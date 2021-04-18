---
description: Définit une clé d’événement qui modifie le poids d’une piste d’animation. Le poids est utilisé comme multiplicateur lors de la combinaison de plusieurs pistes.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController :: KeyTrackWeight, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536445"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="72014-103">ID3DXAnimationController :: KeyTrackWeight, méthode</span><span class="sxs-lookup"><span data-stu-id="72014-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="72014-104">Définit une clé d’événement qui modifie le poids d’une piste d’animation. Le poids est utilisé comme multiplicateur lors de la combinaison de plusieurs pistes.</span><span class="sxs-lookup"><span data-stu-id="72014-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="72014-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72014-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="72014-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72014-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72014-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72014-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72014-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72014-109">Identificateur de la piste à modifier.</span><span class="sxs-lookup"><span data-stu-id="72014-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="72014-110">*NewWeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72014-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72014-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72014-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72014-112">Nouveau poids de la piste.</span><span class="sxs-lookup"><span data-stu-id="72014-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="72014-113">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72014-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72014-114">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72014-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72014-115">Clé de temps globale.</span><span class="sxs-lookup"><span data-stu-id="72014-115">Global time key.</span></span> <span data-ttu-id="72014-116">Spécifie l’heure globale à laquelle la modification doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="72014-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="72014-117">*Durée* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72014-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72014-118">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72014-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72014-119">Durée de transition, qui spécifie le délai d’exécution de la transition lisse.</span><span class="sxs-lookup"><span data-stu-id="72014-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="72014-120">*Transition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72014-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72014-121">Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="72014-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="72014-122">Spécifie le type de transition utilisé pour la transition entre les poids.</span><span class="sxs-lookup"><span data-stu-id="72014-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="72014-123">Consultez [**\_ type D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="72014-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72014-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72014-124">Return value</span></span>

<span data-ttu-id="72014-125">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="72014-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="72014-126">Descripteur d’événement pour l’événement Priority Blend.</span><span class="sxs-lookup"><span data-stu-id="72014-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="72014-127">La **valeur null** est retournée si un ou plusieurs des paramètres d’entrée ne sont pas valides ou si aucun événement libre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="72014-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="72014-128">Notes</span><span class="sxs-lookup"><span data-stu-id="72014-128">Remarks</span></span>

<span data-ttu-id="72014-129">Le poids est utilisé comme un multiplicateur pour déterminer la proportion de cette piste à mélanger avec d’autres pistes.</span><span class="sxs-lookup"><span data-stu-id="72014-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="72014-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72014-130">Requirements</span></span>



| <span data-ttu-id="72014-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72014-131">Requirement</span></span> | <span data-ttu-id="72014-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="72014-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72014-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="72014-133">Header</span></span><br/>  | <dl> <span data-ttu-id="72014-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="72014-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="72014-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72014-135">Library</span></span><br/> | <dl> <span data-ttu-id="72014-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72014-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72014-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72014-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72014-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="72014-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
