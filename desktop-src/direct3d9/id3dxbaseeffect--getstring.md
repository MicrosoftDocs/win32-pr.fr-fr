---
description: Obtient une chaîne.
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'ID3DXBaseEffect :: GetString, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525094"
---
# <a name="id3dxbaseeffectgetstring-method"></a><span data-ttu-id="8e327-103">ID3DXBaseEffect :: GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="8e327-103">ID3DXBaseEffect::GetString method</span></span>

<span data-ttu-id="8e327-104">Obtient une chaîne.</span><span class="sxs-lookup"><span data-stu-id="8e327-104">Gets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e327-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e327-105">Syntax</span></span>


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="8e327-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e327-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e327-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e327-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8e327-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8e327-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="8e327-109">Unique identifier.</span></span> <span data-ttu-id="8e327-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8e327-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e327-111">*ppString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8e327-111">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e327-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e327-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8e327-113">Retourne une chaîne identifiée par hParameter.</span><span class="sxs-lookup"><span data-stu-id="8e327-113">Returns a string identified by hParameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e327-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e327-114">Return value</span></span>

<span data-ttu-id="8e327-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e327-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e327-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e327-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8e327-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8e327-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e327-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e327-118">Requirements</span></span>



| <span data-ttu-id="8e327-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e327-119">Requirement</span></span> | <span data-ttu-id="8e327-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e327-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e327-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e327-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8e327-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e327-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8e327-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e327-123">Library</span></span><br/> | <dl> <span data-ttu-id="8e327-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e327-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8e327-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e327-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e327-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8e327-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8e327-127">**SetString**</span><span class="sxs-lookup"><span data-stu-id="8e327-127">**SetString**</span></span>](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
