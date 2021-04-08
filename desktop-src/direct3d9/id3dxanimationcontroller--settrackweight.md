---
description: Définit le poids de la piste. Le poids est utilisé pour déterminer comment fusionner plusieurs pistes.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'ID3DXAnimationController :: SetTrackWeight, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762362"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="eb30f-104">ID3DXAnimationController :: SetTrackWeight, méthode</span><span class="sxs-lookup"><span data-stu-id="eb30f-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="eb30f-105">Définit le poids de la piste.</span><span class="sxs-lookup"><span data-stu-id="eb30f-105">Sets the track weight.</span></span> <span data-ttu-id="eb30f-106">Le poids est utilisé pour déterminer comment fusionner plusieurs pistes.</span><span class="sxs-lookup"><span data-stu-id="eb30f-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb30f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb30f-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="eb30f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb30f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb30f-109">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb30f-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb30f-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb30f-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb30f-111">Identificateur de la piste sur laquelle définir le poids.</span><span class="sxs-lookup"><span data-stu-id="eb30f-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="eb30f-112">*Poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb30f-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb30f-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb30f-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb30f-114">Valeur de poids.</span><span class="sxs-lookup"><span data-stu-id="eb30f-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb30f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb30f-115">Return value</span></span>

<span data-ttu-id="eb30f-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb30f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb30f-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb30f-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eb30f-118">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="eb30f-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb30f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb30f-119">Requirements</span></span>



| <span data-ttu-id="eb30f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb30f-120">Requirement</span></span> | <span data-ttu-id="eb30f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb30f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb30f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb30f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eb30f-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb30f-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="eb30f-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb30f-124">Library</span></span><br/> | <dl> <span data-ttu-id="eb30f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb30f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb30f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb30f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb30f-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="eb30f-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
