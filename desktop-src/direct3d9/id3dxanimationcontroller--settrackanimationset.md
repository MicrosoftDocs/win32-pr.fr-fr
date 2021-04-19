---
description: Applique l’animation définie à la piste spécifiée.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController :: SetTrackAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531788"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="f4a16-103">ID3DXAnimationController :: SetTrackAnimationSet, méthode</span><span class="sxs-lookup"><span data-stu-id="f4a16-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="f4a16-104">Applique l’animation définie à la piste spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f4a16-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a16-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4a16-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="f4a16-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4a16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a16-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4a16-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a16-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4a16-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4a16-109">Identificateur de la piste à laquelle l’ensemble d’animations est appliqué.</span><span class="sxs-lookup"><span data-stu-id="f4a16-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="f4a16-110">*pAnimSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4a16-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a16-111">Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="f4a16-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="f4a16-112">Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie à ajouter à la piste.</span><span class="sxs-lookup"><span data-stu-id="f4a16-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a16-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4a16-113">Return value</span></span>

<span data-ttu-id="f4a16-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4a16-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4a16-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4a16-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f4a16-116">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f4a16-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4a16-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f4a16-117">Remarks</span></span>

<span data-ttu-id="f4a16-118">Cette méthode définit l’animation définie sur la piste spécifiée pour mélanger.</span><span class="sxs-lookup"><span data-stu-id="f4a16-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="f4a16-119">L’animation définie pour chaque piste est fusionnée en fonction du poids de la piste et de la vitesse de l’appel de [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .</span><span class="sxs-lookup"><span data-stu-id="f4a16-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a16-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4a16-120">Requirements</span></span>



| <span data-ttu-id="f4a16-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4a16-121">Requirement</span></span> | <span data-ttu-id="f4a16-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4a16-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a16-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4a16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f4a16-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a16-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f4a16-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4a16-125">Library</span></span><br/> | <dl> <span data-ttu-id="f4a16-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4a16-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4a16-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4a16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a16-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f4a16-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
