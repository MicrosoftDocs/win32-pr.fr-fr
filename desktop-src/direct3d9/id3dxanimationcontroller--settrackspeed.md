---
description: Définit la vitesse de la piste. La vitesse de la piste est similaire à un multiplicateur qui est utilisé pour accélérer ou ralentir la lecture de la piste.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'ID3DXAnimationController :: SetTrackSpeed, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323358"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="d4f80-104">ID3DXAnimationController :: SetTrackSpeed, méthode</span><span class="sxs-lookup"><span data-stu-id="d4f80-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="d4f80-105">Définit la vitesse de la piste.</span><span class="sxs-lookup"><span data-stu-id="d4f80-105">Sets the track speed.</span></span> <span data-ttu-id="d4f80-106">La vitesse de la piste est similaire à un multiplicateur qui est utilisé pour accélérer ou ralentir la lecture de la piste.</span><span class="sxs-lookup"><span data-stu-id="d4f80-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f80-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4f80-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="d4f80-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4f80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f80-109">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4f80-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f80-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4f80-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4f80-111">Identificateur de la piste sur laquelle définir la vitesse.</span><span class="sxs-lookup"><span data-stu-id="d4f80-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="d4f80-112">*Vitesse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4f80-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f80-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4f80-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4f80-114">Nouvelle vitesse.</span><span class="sxs-lookup"><span data-stu-id="d4f80-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f80-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4f80-115">Return value</span></span>

<span data-ttu-id="d4f80-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4f80-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4f80-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4f80-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4f80-118">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d4f80-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f80-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4f80-119">Requirements</span></span>



| <span data-ttu-id="d4f80-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4f80-120">Requirement</span></span> | <span data-ttu-id="d4f80-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4f80-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f80-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4f80-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d4f80-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f80-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d4f80-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4f80-124">Library</span></span><br/> | <dl> <span data-ttu-id="d4f80-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4f80-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4f80-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4f80-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f80-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d4f80-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
