---
description: Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet :: GetCallback, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211947"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="3699c-103">ID3DXAnimationSet :: GetCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="3699c-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="3699c-104">Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="3699c-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3699c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3699c-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="3699c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3699c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3699c-107">*Position* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3699c-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3699c-108">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3699c-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3699c-109">Position à partir de laquelle rechercher les rappels.</span><span class="sxs-lookup"><span data-stu-id="3699c-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="3699c-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3699c-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3699c-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3699c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3699c-112">Indicateurs de recherche de rappel.</span><span class="sxs-lookup"><span data-stu-id="3699c-112">Callback search flags.</span></span> <span data-ttu-id="3699c-113">Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs d' [**\_ \_ indicateurs de recherche D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3699c-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3699c-114">*pCallbackPosition* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3699c-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3699c-115">Type : **[ **double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3699c-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3699c-116">Pointeur vers la position du rappel.</span><span class="sxs-lookup"><span data-stu-id="3699c-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="3699c-117">*ppCallbackData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3699c-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3699c-118">Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3699c-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3699c-119">Adresse du pointeur de données de rappel.</span><span class="sxs-lookup"><span data-stu-id="3699c-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3699c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3699c-120">Return value</span></span>

<span data-ttu-id="3699c-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3699c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3699c-122">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="3699c-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="3699c-123">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3699c-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="3699c-124">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="3699c-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3699c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3699c-125">Requirements</span></span>



| <span data-ttu-id="3699c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3699c-126">Requirement</span></span> | <span data-ttu-id="3699c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3699c-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3699c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3699c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3699c-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3699c-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3699c-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3699c-130">Library</span></span><br/> | <dl> <span data-ttu-id="3699c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3699c-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3699c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3699c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3699c-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="3699c-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
