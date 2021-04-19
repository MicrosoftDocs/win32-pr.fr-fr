---
description: Définit un vecteur.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'ID3DXBaseEffect :: SetVector, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538363"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="4210e-103">ID3DXBaseEffect :: SetVector, méthode</span><span class="sxs-lookup"><span data-stu-id="4210e-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="4210e-104">Définit un vecteur.</span><span class="sxs-lookup"><span data-stu-id="4210e-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4210e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4210e-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="4210e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4210e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4210e-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4210e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4210e-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4210e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4210e-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="4210e-109">Unique identifier.</span></span> <span data-ttu-id="4210e-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="4210e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4210e-111">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4210e-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4210e-112">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="4210e-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4210e-113">Pointeur vers un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="4210e-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4210e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4210e-114">Return value</span></span>

<span data-ttu-id="4210e-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4210e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4210e-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4210e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4210e-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4210e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4210e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4210e-118">Remarks</span></span>

<span data-ttu-id="4210e-119">Si le vecteur de destination est plus petit que le vecteur source, les composants supplémentaires du vecteur source sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="4210e-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4210e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4210e-120">Requirements</span></span>



| <span data-ttu-id="4210e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4210e-121">Requirement</span></span> | <span data-ttu-id="4210e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4210e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4210e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4210e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4210e-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4210e-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4210e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4210e-125">Library</span></span><br/> | <dl> <span data-ttu-id="4210e-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4210e-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4210e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4210e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4210e-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="4210e-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="4210e-129">**GetVector**</span><span class="sxs-lookup"><span data-stu-id="4210e-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




