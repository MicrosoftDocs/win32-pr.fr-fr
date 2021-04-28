---
description: 'ID3DXBaseEffect :: SetBool, méthode-définit une valeur BOOL.'
ms.assetid: bb7c4860-50a0-416a-b9e0-5a2bec113e3c
title: 'ID3DXBaseEffect :: SetBool, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5045c26f521da289899c8f8bc0d97b7eaf01826f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097517"
---
# <a name="id3dxbaseeffectsetbool-method"></a><span data-ttu-id="c5ae7-103">ID3DXBaseEffect :: SetBool, méthode</span><span class="sxs-lookup"><span data-stu-id="c5ae7-103">ID3DXBaseEffect::SetBool method</span></span>

<span data-ttu-id="c5ae7-104">Définit une valeur BOOL.</span><span class="sxs-lookup"><span data-stu-id="c5ae7-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ae7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5ae7-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="c5ae7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5ae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ae7-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5ae7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ae7-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ae7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c5ae7-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="c5ae7-109">Unique identifier.</span></span> <span data-ttu-id="c5ae7-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c5ae7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5ae7-111">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5ae7-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ae7-112">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ae7-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5ae7-113">Valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="c5ae7-113">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ae7-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5ae7-114">Return value</span></span>

<span data-ttu-id="c5ae7-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5ae7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5ae7-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5ae7-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5ae7-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c5ae7-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ae7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5ae7-118">Requirements</span></span>



| <span data-ttu-id="c5ae7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5ae7-119">Requirement</span></span> | <span data-ttu-id="c5ae7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5ae7-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ae7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5ae7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c5ae7-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae7-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c5ae7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5ae7-123">Library</span></span><br/> | <dl> <span data-ttu-id="c5ae7-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae7-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5ae7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5ae7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ae7-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c5ae7-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c5ae7-127">**GetBool**</span><span class="sxs-lookup"><span data-stu-id="c5ae7-127">**GetBool**</span></span>](id3dxbaseeffect--getbool.md)
</dt> </dl>

 

 
