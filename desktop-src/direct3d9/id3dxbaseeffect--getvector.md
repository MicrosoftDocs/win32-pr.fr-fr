---
description: Obtient un vecteur.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'ID3DXBaseEffect :: GetVector, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322629"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="517b7-103">ID3DXBaseEffect :: GetVector, méthode</span><span class="sxs-lookup"><span data-stu-id="517b7-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="517b7-104">Obtient un vecteur.</span><span class="sxs-lookup"><span data-stu-id="517b7-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="517b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="517b7-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="517b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="517b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="517b7-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="517b7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="517b7-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="517b7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="517b7-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="517b7-109">Unique identifier.</span></span> <span data-ttu-id="517b7-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="517b7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="517b7-111">*pVector* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="517b7-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="517b7-112">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="517b7-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="517b7-113">Retourne un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="517b7-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="517b7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="517b7-114">Return value</span></span>

<span data-ttu-id="517b7-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="517b7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="517b7-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="517b7-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="517b7-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="517b7-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="517b7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="517b7-118">Remarks</span></span>

<span data-ttu-id="517b7-119">Si le vecteur de destination est plus grand que le vecteur source, seuls les composants initiaux du vecteur de destination seront remplis, et les composants restants seront définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="517b7-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="517b7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="517b7-120">Requirements</span></span>



| <span data-ttu-id="517b7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="517b7-121">Requirement</span></span> | <span data-ttu-id="517b7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="517b7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="517b7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="517b7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="517b7-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="517b7-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="517b7-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="517b7-125">Library</span></span><br/> | <dl> <span data-ttu-id="517b7-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="517b7-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="517b7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="517b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517b7-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="517b7-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="517b7-129">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="517b7-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




