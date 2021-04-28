---
description: 'ID3DXAnimationSet :: GetCallback, méthode-obtient des informations sur un rappel spécifique dans l’ensemble d’animations.'
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
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097537"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="b8e24-103">ID3DXAnimationSet :: GetCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="b8e24-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="b8e24-104">Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="b8e24-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8e24-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="b8e24-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8e24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e24-107">*Position* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8e24-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e24-108">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8e24-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8e24-109">Position à partir de laquelle rechercher les rappels.</span><span class="sxs-lookup"><span data-stu-id="b8e24-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="b8e24-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b8e24-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e24-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8e24-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8e24-112">Indicateurs de recherche de rappel.</span><span class="sxs-lookup"><span data-stu-id="b8e24-112">Callback search flags.</span></span> <span data-ttu-id="b8e24-113">Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs d' [**\_ \_ indicateurs de recherche D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b8e24-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8e24-114">*pCallbackPosition* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b8e24-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e24-115">Type : **[ **double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8e24-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b8e24-116">Pointeur vers la position du rappel.</span><span class="sxs-lookup"><span data-stu-id="b8e24-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="b8e24-117">*ppCallbackData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b8e24-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e24-118">Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8e24-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b8e24-119">Adresse du pointeur de données de rappel.</span><span class="sxs-lookup"><span data-stu-id="b8e24-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e24-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8e24-120">Return value</span></span>

<span data-ttu-id="b8e24-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8e24-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8e24-122">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="b8e24-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="b8e24-123">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8e24-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="b8e24-124">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="b8e24-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e24-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8e24-125">Requirements</span></span>



| <span data-ttu-id="b8e24-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8e24-126">Requirement</span></span> | <span data-ttu-id="b8e24-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8e24-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e24-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8e24-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b8e24-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e24-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b8e24-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8e24-130">Library</span></span><br/> | <dl> <span data-ttu-id="b8e24-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8e24-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8e24-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8e24-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e24-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b8e24-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
