---
description: Recherche la technique suivante valide, en commençant par la technique qui suit la technique spécifiée.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect :: FindNextValidTechnique, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394144"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="724a4-103">ID3DXEffect :: FindNextValidTechnique, méthode</span><span class="sxs-lookup"><span data-stu-id="724a4-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="724a4-104">Recherche la technique suivante valide, en commençant par la technique qui suit la technique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="724a4-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="724a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="724a4-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="724a4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="724a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724a4-107">*hTechnique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="724a4-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724a4-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="724a4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="724a4-109">Identificateur unique d’une technique.</span><span class="sxs-lookup"><span data-stu-id="724a4-109">Unique identifier to a technique.</span></span> <span data-ttu-id="724a4-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="724a4-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="724a4-111">Spécifiez **null** pour ce paramètre pour rechercher la première technique valide.</span><span class="sxs-lookup"><span data-stu-id="724a4-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="724a4-112">*pTechnique* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="724a4-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="724a4-113">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="724a4-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="724a4-114">Pointeur vers un identificateur pour la technique suivante.</span><span class="sxs-lookup"><span data-stu-id="724a4-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="724a4-115">La **valeur null** est retournée s’il s’agit de la dernière technique.</span><span class="sxs-lookup"><span data-stu-id="724a4-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="724a4-116">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="724a4-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724a4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="724a4-117">Return value</span></span>

<span data-ttu-id="724a4-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="724a4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="724a4-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="724a4-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="724a4-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="724a4-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="724a4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="724a4-121">Requirements</span></span>



| <span data-ttu-id="724a4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="724a4-122">Requirement</span></span> | <span data-ttu-id="724a4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="724a4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="724a4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="724a4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="724a4-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="724a4-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="724a4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="724a4-126">Library</span></span><br/> | <dl> <span data-ttu-id="724a4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="724a4-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="724a4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="724a4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724a4-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="724a4-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="724a4-130">**D3DXTECHNIQUE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="724a4-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="724a4-131">**ID3DXEffect::ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="724a4-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




