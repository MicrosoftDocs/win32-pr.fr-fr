---
description: Obtient un État littéral d’un paramètre. Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler :: GetLiteral, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531778"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="d0f0e-104">ID3DXEffectCompiler :: GetLiteral, méthode</span><span class="sxs-lookup"><span data-stu-id="d0f0e-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="d0f0e-105">Obtient un État littéral d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="d0f0e-106">Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f0e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0f0e-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="d0f0e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0f0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f0e-109">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0f0e-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f0e-110">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d0f0e-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d0f0e-111">Identificateur unique d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="d0f0e-112">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d0f0e-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0f0e-113">*pLiteral* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d0f0e-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f0e-114">Type : **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0f0e-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d0f0e-115">Retourne la valeur true si le paramètre est un littéral et la valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f0e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0f0e-116">Return value</span></span>

<span data-ttu-id="d0f0e-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0f0e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0f0e-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0f0e-119">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f0e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d0f0e-120">Remarks</span></span>

<span data-ttu-id="d0f0e-121">Cette méthode change uniquement si le paramètre est un littéral ou non.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="d0f0e-122">Pour modifier la valeur d’un paramètre, utilisez une méthode comme [**ID3DXBaseEffect :: SetBool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect :: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="d0f0e-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f0e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0f0e-123">Requirements</span></span>



| <span data-ttu-id="d0f0e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0f0e-124">Requirement</span></span> | <span data-ttu-id="d0f0e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0f0e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f0e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0f0e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0f0e-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f0e-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d0f0e-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0f0e-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0f0e-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0f0e-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d0f0e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0f0e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f0e-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="d0f0e-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="d0f0e-132">Utilisations et littéraux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d0f0e-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="d0f0e-133">**ID3DXEffectCompiler::SetLiteral**</span><span class="sxs-lookup"><span data-stu-id="d0f0e-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
