---
description: Définit le poids de fusion des priorités pour la piste d’animation spécifiée.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController :: SetTrackPriority, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525308"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="43f04-103">ID3DXAnimationController :: SetTrackPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="43f04-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="43f04-104">Définit le poids de fusion des priorités pour la piste d’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="43f04-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f04-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43f04-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="43f04-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43f04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f04-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43f04-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f04-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f04-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f04-109">Identificateur de suivi.</span><span class="sxs-lookup"><span data-stu-id="43f04-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="43f04-110">*Priorité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43f04-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f04-111">Type : **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="43f04-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="43f04-112">Suivre la priorité.</span><span class="sxs-lookup"><span data-stu-id="43f04-112">Track priority.</span></span> <span data-ttu-id="43f04-113">Ce paramètre doit être défini sur l’une des constantes du [**\_ type D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="43f04-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f04-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43f04-114">Return value</span></span>

<span data-ttu-id="43f04-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43f04-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43f04-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43f04-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="43f04-117">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="43f04-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f04-118">Notes</span><span class="sxs-lookup"><span data-stu-id="43f04-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="43f04-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="43f04-119">Requirements</span></span>



| <span data-ttu-id="43f04-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43f04-120">Requirement</span></span> | <span data-ttu-id="43f04-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="43f04-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43f04-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="43f04-122">Header</span></span><br/>  | <dl> <span data-ttu-id="43f04-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f04-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="43f04-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43f04-124">Library</span></span><br/> | <dl> <span data-ttu-id="43f04-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43f04-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43f04-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43f04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f04-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="43f04-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
