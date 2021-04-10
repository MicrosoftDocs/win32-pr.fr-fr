---
description: Définit un tableau de vecteurs.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'ID3DXBaseEffect :: SetVectorArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4c5deace65608ee547b8fdcc4fb236b11d38c810
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953924"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a><span data-ttu-id="06db1-103">ID3DXBaseEffect :: SetVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="06db1-103">ID3DXBaseEffect::SetVectorArray method</span></span>

<span data-ttu-id="06db1-104">Définit un tableau de vecteurs.</span><span class="sxs-lookup"><span data-stu-id="06db1-104">Sets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="06db1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06db1-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="06db1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06db1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06db1-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06db1-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06db1-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="06db1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="06db1-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="06db1-109">Unique identifier.</span></span> <span data-ttu-id="06db1-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="06db1-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="06db1-111">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06db1-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06db1-112">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="06db1-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="06db1-113">Tableau de vecteurs à virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="06db1-113">Array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="06db1-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06db1-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06db1-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06db1-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06db1-116">Nombre de vecteurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="06db1-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06db1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06db1-117">Return value</span></span>

<span data-ttu-id="06db1-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06db1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06db1-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06db1-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06db1-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="06db1-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="06db1-121">Notes</span><span class="sxs-lookup"><span data-stu-id="06db1-121">Remarks</span></span>

<span data-ttu-id="06db1-122">Si les vecteurs de destination sont plus petits que les vecteurs sources, les composants supplémentaires des vecteurs sources seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="06db1-122">If the destination vectors are smaller than the source vectors, the additional components of the source vectors will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="06db1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06db1-123">Requirements</span></span>



| <span data-ttu-id="06db1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06db1-124">Requirement</span></span> | <span data-ttu-id="06db1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="06db1-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06db1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="06db1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="06db1-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="06db1-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="06db1-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06db1-128">Library</span></span><br/> | <dl> <span data-ttu-id="06db1-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06db1-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="06db1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06db1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06db1-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="06db1-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="06db1-132">**GetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="06db1-132">**GetVectorArray**</span></span>](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
