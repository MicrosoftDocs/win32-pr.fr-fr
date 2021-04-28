---
description: 'ID3DXBaseEffect :: SetIntArray, méthode-définit un tableau d’entiers.'
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'ID3DXBaseEffect :: SetIntArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093757"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="434e2-103">ID3DXBaseEffect :: SetIntArray, méthode</span><span class="sxs-lookup"><span data-stu-id="434e2-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="434e2-104">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="434e2-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="434e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="434e2-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="434e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="434e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434e2-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="434e2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e2-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="434e2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="434e2-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="434e2-109">Unique identifier.</span></span> <span data-ttu-id="434e2-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="434e2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="434e2-111">*PN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="434e2-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e2-112">Type : **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="434e2-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="434e2-113">Tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="434e2-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="434e2-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="434e2-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e2-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="434e2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="434e2-116">Nombre d’entiers dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="434e2-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434e2-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="434e2-117">Return value</span></span>

<span data-ttu-id="434e2-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="434e2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="434e2-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="434e2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="434e2-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="434e2-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="434e2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="434e2-121">Requirements</span></span>



| <span data-ttu-id="434e2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="434e2-122">Requirement</span></span> | <span data-ttu-id="434e2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="434e2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="434e2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="434e2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="434e2-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="434e2-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="434e2-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="434e2-126">Library</span></span><br/> | <dl> <span data-ttu-id="434e2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="434e2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="434e2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="434e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434e2-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="434e2-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="434e2-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="434e2-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
