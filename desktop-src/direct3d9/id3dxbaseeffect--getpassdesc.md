---
description: Obtient une description de l’étape.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect :: GetPassDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538549"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="a6e32-103">ID3DXBaseEffect :: GetPassDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="a6e32-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="a6e32-104">Obtient une description de l’étape.</span><span class="sxs-lookup"><span data-stu-id="a6e32-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6e32-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a6e32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6e32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e32-107">*hPass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a6e32-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e32-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a6e32-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a6e32-109">Handle de réussite.</span><span class="sxs-lookup"><span data-stu-id="a6e32-109">Pass handle.</span></span> <span data-ttu-id="a6e32-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a6e32-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e32-111">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a6e32-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e32-112">Type : **[ **D3DXPASS \_ desc**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6e32-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="a6e32-113">Retourne une description de la passe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a6e32-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="a6e32-114">Consultez [**D3DXPASS \_ desc**](d3dxpass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="a6e32-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e32-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6e32-115">Return value</span></span>

<span data-ttu-id="a6e32-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6e32-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6e32-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6e32-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a6e32-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a6e32-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6e32-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a6e32-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a6e32-120">Si un effet est créé avec [D3DXFX qui \_ ne peut pas être \_ cloné](d3dxfx.md), cette méthode retournera les pointeurs **null** (dans [**D3DXPASS \_ desc**](d3dxpass-desc.md)) aux fonctions de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a6e32-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6e32-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6e32-121">Requirements</span></span>



| <span data-ttu-id="a6e32-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6e32-122">Requirement</span></span> | <span data-ttu-id="a6e32-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6e32-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e32-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6e32-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a6e32-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e32-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a6e32-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a6e32-126">Library</span></span><br/> | <dl> <span data-ttu-id="a6e32-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6e32-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a6e32-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6e32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e32-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a6e32-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




