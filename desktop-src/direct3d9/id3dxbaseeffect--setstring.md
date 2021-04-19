---
description: Définit une chaîne.
ms.assetid: 7e8eef70-85ee-461d-bf8c-44cda5f184cd
title: 'ID3DXBaseEffect :: SetString, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a7c4f86c6b7fa78c869eb1d5bd49634ec4b496d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529585"
---
# <a name="id3dxbaseeffectsetstring-method"></a><span data-ttu-id="1ca02-103">ID3DXBaseEffect :: SetString, méthode</span><span class="sxs-lookup"><span data-stu-id="1ca02-103">ID3DXBaseEffect::SetString method</span></span>

<span data-ttu-id="1ca02-104">Définit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1ca02-104">Sets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ca02-105">Syntax</span></span>


```C++
HRESULT SetString(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pString
);
```



## <a name="parameters"></a><span data-ttu-id="1ca02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ca02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca02-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca02-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca02-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca02-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1ca02-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="1ca02-109">Unique identifier.</span></span> <span data-ttu-id="1ca02-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1ca02-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca02-111">*pString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca02-111">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca02-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca02-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ca02-113">Chaîne à définir.</span><span class="sxs-lookup"><span data-stu-id="1ca02-113">String to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca02-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ca02-114">Return value</span></span>

<span data-ttu-id="1ca02-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ca02-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ca02-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ca02-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ca02-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1ca02-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ca02-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ca02-118">Requirements</span></span>



| <span data-ttu-id="1ca02-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ca02-119">Requirement</span></span> | <span data-ttu-id="1ca02-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ca02-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca02-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ca02-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1ca02-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ca02-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1ca02-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ca02-123">Library</span></span><br/> | <dl> <span data-ttu-id="1ca02-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ca02-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1ca02-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ca02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca02-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1ca02-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="1ca02-127">**GetString**</span><span class="sxs-lookup"><span data-stu-id="1ca02-127">**GetString**</span></span>](id3dxbaseeffect--getstring.md)
</dt> </dl>

 

 
