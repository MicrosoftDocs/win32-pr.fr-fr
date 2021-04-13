---
description: Obtient un tableau de vecteurs.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'ID3DXBaseEffect :: GetVectorArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322626"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="8b1e4-103">ID3DXBaseEffect :: GetVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="8b1e4-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="8b1e4-104">Obtient un tableau de vecteurs.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b1e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b1e4-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="8b1e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b1e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b1e4-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b1e4-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b1e4-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8b1e4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8b1e4-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-109">Unique identifier.</span></span> <span data-ttu-id="8b1e4-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8b1e4-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b1e4-111">*pVector* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8b1e4-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b1e4-112">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b1e4-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8b1e4-113">Retourne un tableau de vecteurs à virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="8b1e4-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b1e4-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b1e4-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b1e4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b1e4-116">Nombre de vecteurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b1e4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b1e4-117">Return value</span></span>

<span data-ttu-id="8b1e4-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b1e4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b1e4-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8b1e4-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b1e4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8b1e4-121">Remarks</span></span>

<span data-ttu-id="8b1e4-122">Si les vecteurs de destination sont plus grands que les vecteurs sources, seuls les composants initiaux de chaque vecteur de destination seront remplis, et les autres composants de vecteurs de destination seront définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1e4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b1e4-123">Requirements</span></span>



| <span data-ttu-id="8b1e4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b1e4-124">Requirement</span></span> | <span data-ttu-id="8b1e4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b1e4-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1e4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b1e4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8b1e4-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b1e4-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8b1e4-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b1e4-128">Library</span></span><br/> | <dl> <span data-ttu-id="8b1e4-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b1e4-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8b1e4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b1e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1e4-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8b1e4-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8b1e4-132">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="8b1e4-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
