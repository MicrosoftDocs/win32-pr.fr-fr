---
description: Définit une clé d’événement qui modifie le taux de lecture d’une piste d’animation.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController :: KeyTrackSpeed, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543572"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="ad391-103">ID3DXAnimationController :: KeyTrackSpeed, méthode</span><span class="sxs-lookup"><span data-stu-id="ad391-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="ad391-104">Définit une clé d’événement qui modifie le taux de lecture d’une piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="ad391-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad391-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad391-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="ad391-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad391-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad391-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad391-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad391-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad391-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad391-109">Identificateur de la piste à modifier.</span><span class="sxs-lookup"><span data-stu-id="ad391-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ad391-110">*NewSpeed* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad391-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad391-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad391-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad391-112">Nouvelle vitesse de la piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="ad391-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="ad391-113">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad391-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad391-114">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad391-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad391-115">Clé de temps globale.</span><span class="sxs-lookup"><span data-stu-id="ad391-115">Global time key.</span></span> <span data-ttu-id="ad391-116">Spécifie l’heure globale à laquelle la modification doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="ad391-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="ad391-117">*Durée* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad391-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad391-118">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad391-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad391-119">Durée de transition, qui spécifie le délai d’exécution de la transition lisse.</span><span class="sxs-lookup"><span data-stu-id="ad391-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="ad391-120">*Transition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad391-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad391-121">Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ad391-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="ad391-122">Spécifie le type de transition utilisé pour la transition entre les vitesses.</span><span class="sxs-lookup"><span data-stu-id="ad391-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="ad391-123">Consultez [**\_ type D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="ad391-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad391-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad391-124">Return value</span></span>

<span data-ttu-id="ad391-125">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="ad391-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="ad391-126">Descripteur d’événement pour l’événement Priority Blend.</span><span class="sxs-lookup"><span data-stu-id="ad391-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="ad391-127">La **valeur null** est retournée si un ou plusieurs des paramètres d’entrée ne sont pas valides ou si aucun événement libre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="ad391-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad391-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad391-128">Requirements</span></span>



| <span data-ttu-id="ad391-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad391-129">Requirement</span></span> | <span data-ttu-id="ad391-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad391-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad391-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad391-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ad391-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad391-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ad391-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad391-133">Library</span></span><br/> | <dl> <span data-ttu-id="ad391-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad391-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad391-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad391-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad391-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ad391-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
