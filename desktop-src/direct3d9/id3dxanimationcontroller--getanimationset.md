---
description: Obtient un jeu d’animations.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'ID3DXAnimationController :: GetAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116250"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="54b15-103">ID3DXAnimationController :: GetAnimationSet, méthode</span><span class="sxs-lookup"><span data-stu-id="54b15-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="54b15-104">Obtient un jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="54b15-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54b15-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="54b15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54b15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b15-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54b15-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b15-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b15-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b15-109">Index de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="54b15-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="54b15-110">*ppAnimSet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54b15-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b15-111">Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="54b15-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="54b15-112">Pointeur vers le jeu d’animations [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="54b15-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b15-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54b15-113">Return value</span></span>

<span data-ttu-id="54b15-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54b15-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54b15-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54b15-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="54b15-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="54b15-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b15-117">Notes</span><span class="sxs-lookup"><span data-stu-id="54b15-117">Remarks</span></span>

<span data-ttu-id="54b15-118">Le contrôleur d’animation contient un tableau d’ensembles d’animations.</span><span class="sxs-lookup"><span data-stu-id="54b15-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="54b15-119">Cette méthode retourne l’une d’entre elles à l’index donné.</span><span class="sxs-lookup"><span data-stu-id="54b15-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b15-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54b15-120">Requirements</span></span>



| <span data-ttu-id="54b15-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54b15-121">Requirement</span></span> | <span data-ttu-id="54b15-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="54b15-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54b15-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="54b15-123">Header</span></span><br/>  | <dl> <span data-ttu-id="54b15-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="54b15-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="54b15-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54b15-125">Library</span></span><br/> | <dl> <span data-ttu-id="54b15-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54b15-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54b15-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54b15-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b15-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="54b15-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
