---
description: Définit un tableau d’entiers.
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
ms.openlocfilehash: f76ff0d7f4bcc68d7cce85f3d02f2bc207a5f4b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523166"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="2f972-103">ID3DXBaseEffect :: SetIntArray, méthode</span><span class="sxs-lookup"><span data-stu-id="2f972-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="2f972-104">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="2f972-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f972-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f972-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2f972-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f972-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f972-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f972-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f972-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2f972-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2f972-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="2f972-109">Unique identifier.</span></span> <span data-ttu-id="2f972-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2f972-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f972-111">*PN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f972-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f972-112">Type : **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f972-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f972-113">Tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="2f972-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2f972-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f972-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f972-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f972-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f972-116">Nombre d’entiers dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2f972-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f972-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f972-117">Return value</span></span>

<span data-ttu-id="2f972-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f972-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f972-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f972-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2f972-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2f972-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f972-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f972-121">Requirements</span></span>



| <span data-ttu-id="2f972-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f972-122">Requirement</span></span> | <span data-ttu-id="2f972-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f972-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f972-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f972-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2f972-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f972-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2f972-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f972-126">Library</span></span><br/> | <dl> <span data-ttu-id="2f972-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f972-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f972-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f972-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f972-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2f972-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2f972-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="2f972-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
