---
description: Obtient un tableau d’entiers.
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: 'ID3DXBaseEffect :: GetIntArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f13c6b8717c2108920d7b914da20b99f0451f5d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323337"
---
# <a name="id3dxbaseeffectgetintarray-method"></a><span data-ttu-id="ee949-103">ID3DXBaseEffect :: GetIntArray, méthode</span><span class="sxs-lookup"><span data-stu-id="ee949-103">ID3DXBaseEffect::GetIntArray method</span></span>

<span data-ttu-id="ee949-104">Obtient un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="ee949-104">Gets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee949-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee949-105">Syntax</span></span>


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ee949-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee949-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee949-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee949-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ee949-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ee949-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="ee949-109">Unique identifier.</span></span> <span data-ttu-id="ee949-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ee949-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee949-111">*PN* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ee949-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee949-112">Type : **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee949-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee949-113">Retourne un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="ee949-113">Returns an array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="ee949-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee949-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee949-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee949-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee949-116">Nombre d’entiers dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ee949-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee949-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee949-117">Return value</span></span>

<span data-ttu-id="ee949-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee949-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee949-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee949-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee949-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ee949-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee949-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee949-121">Requirements</span></span>



| <span data-ttu-id="ee949-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee949-122">Requirement</span></span> | <span data-ttu-id="ee949-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee949-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee949-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee949-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ee949-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee949-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ee949-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee949-126">Library</span></span><br/> | <dl> <span data-ttu-id="ee949-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee949-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ee949-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee949-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee949-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ee949-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ee949-130">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="ee949-130">**SetIntArray**</span></span>](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 
