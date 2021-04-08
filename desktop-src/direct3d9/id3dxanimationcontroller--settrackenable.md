---
description: Active ou désactive une piste dans le contrôleur d’animation.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'ID3DXAnimationController :: SetTrackEnable, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043156"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="9e286-103">ID3DXAnimationController :: SetTrackEnable, méthode</span><span class="sxs-lookup"><span data-stu-id="9e286-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="9e286-104">Active ou désactive une piste dans le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="9e286-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e286-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e286-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="9e286-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e286-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e286-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e286-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e286-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e286-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e286-109">Identificateur de la piste à mélanger.</span><span class="sxs-lookup"><span data-stu-id="9e286-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="9e286-110">*Activer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e286-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e286-111">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e286-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e286-112">Activez la valeur.</span><span class="sxs-lookup"><span data-stu-id="9e286-112">Enable value.</span></span> <span data-ttu-id="9e286-113">Affectez la valeur **true** pour activer cette piste dans le contrôleur, ou la valeur **false** pour l’empêcher d’être mélangée.</span><span class="sxs-lookup"><span data-stu-id="9e286-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e286-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e286-114">Return value</span></span>

<span data-ttu-id="9e286-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e286-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e286-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e286-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9e286-117">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9e286-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e286-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9e286-118">Remarks</span></span>

<span data-ttu-id="9e286-119">Pour mélanger une piste avec d’autres pistes, l’indicateur d’activation doit avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="9e286-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="9e286-120">Inversement, l’affectation de la **valeur false** à l’indicateur empêchera la combinaison de la piste avec d’autres pistes.</span><span class="sxs-lookup"><span data-stu-id="9e286-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e286-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e286-121">Requirements</span></span>



| <span data-ttu-id="9e286-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e286-122">Requirement</span></span> | <span data-ttu-id="9e286-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e286-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e286-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e286-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9e286-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e286-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9e286-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e286-126">Library</span></span><br/> | <dl> <span data-ttu-id="9e286-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e286-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e286-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e286-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e286-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="9e286-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
