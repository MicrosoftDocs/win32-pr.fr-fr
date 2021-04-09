---
description: Obtient l’animation définie pour le suivi donné.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'ID3DXAnimationController :: GetTrackAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953920"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a><span data-ttu-id="ee7c5-103">ID3DXAnimationController :: GetTrackAnimationSet, méthode</span><span class="sxs-lookup"><span data-stu-id="ee7c5-103">ID3DXAnimationController::GetTrackAnimationSet method</span></span>

<span data-ttu-id="ee7c5-104">Obtient l’animation définie pour le suivi donné.</span><span class="sxs-lookup"><span data-stu-id="ee7c5-104">Gets the animation set for the given track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee7c5-105">Syntax</span></span>


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="ee7c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee7c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee7c5-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee7c5-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7c5-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee7c5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee7c5-109">Identificateur de suivi.</span><span class="sxs-lookup"><span data-stu-id="ee7c5-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ee7c5-110">*ppAnimSet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ee7c5-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7c5-111">Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee7c5-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="ee7c5-112">Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie pour la piste donnée.</span><span class="sxs-lookup"><span data-stu-id="ee7c5-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set for the given track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee7c5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee7c5-113">Return value</span></span>

<span data-ttu-id="ee7c5-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee7c5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee7c5-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee7c5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ee7c5-116">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ee7c5-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7c5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee7c5-117">Requirements</span></span>



| <span data-ttu-id="ee7c5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee7c5-118">Requirement</span></span> | <span data-ttu-id="ee7c5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee7c5-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7c5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee7c5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ee7c5-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee7c5-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ee7c5-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee7c5-122">Library</span></span><br/> | <dl> <span data-ttu-id="ee7c5-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee7c5-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee7c5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee7c5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7c5-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ee7c5-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
