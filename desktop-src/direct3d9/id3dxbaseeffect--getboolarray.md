---
description: Obtient un tableau de valeurs BOOL.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'ID3DXBaseEffect :: GetBoolArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523858"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="b1c8b-103">ID3DXBaseEffect :: GetBoolArray, méthode</span><span class="sxs-lookup"><span data-stu-id="b1c8b-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="b1c8b-104">Obtient un tableau de valeurs BOOL.</span><span class="sxs-lookup"><span data-stu-id="b1c8b-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1c8b-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b1c8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1c8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1c8b-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1c8b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1c8b-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b1c8b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b1c8b-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="b1c8b-109">Unique identifier.</span></span> <span data-ttu-id="b1c8b-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b1c8b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1c8b-111">*PB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b1c8b-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1c8b-112">Type : **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1c8b-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1c8b-113">Retourne un tableau de valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="b1c8b-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="b1c8b-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1c8b-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1c8b-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1c8b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1c8b-116">Nombre de valeurs booléennes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b1c8b-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1c8b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1c8b-117">Return value</span></span>

<span data-ttu-id="b1c8b-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1c8b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1c8b-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1c8b-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1c8b-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b1c8b-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1c8b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1c8b-121">Requirements</span></span>



| <span data-ttu-id="b1c8b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1c8b-122">Requirement</span></span> | <span data-ttu-id="b1c8b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1c8b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c8b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1c8b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b1c8b-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1c8b-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b1c8b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b1c8b-126">Library</span></span><br/> | <dl> <span data-ttu-id="b1c8b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1c8b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b1c8b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1c8b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1c8b-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b1c8b-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b1c8b-130">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="b1c8b-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
