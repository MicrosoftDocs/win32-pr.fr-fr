---
description: Obtient une valeur BOOL.
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: 'ID3DXBaseEffect :: GetBool, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0476c62733379a7e92aca55c3cdc2c31a3526de2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528577"
---
# <a name="id3dxbaseeffectgetbool-method"></a><span data-ttu-id="74784-103">ID3DXBaseEffect :: GetBool, méthode</span><span class="sxs-lookup"><span data-stu-id="74784-103">ID3DXBaseEffect::GetBool method</span></span>

<span data-ttu-id="74784-104">Obtient une valeur BOOL.</span><span class="sxs-lookup"><span data-stu-id="74784-104">Gets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="74784-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74784-105">Syntax</span></span>


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a><span data-ttu-id="74784-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74784-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74784-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74784-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="74784-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="74784-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="74784-109">Unique identifier.</span></span> <span data-ttu-id="74784-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="74784-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="74784-111">*PB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="74784-111">*pb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74784-112">Type : **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="74784-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="74784-113">Retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="74784-113">Returns a Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74784-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74784-114">Return value</span></span>

<span data-ttu-id="74784-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74784-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74784-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74784-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74784-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="74784-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="74784-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74784-118">Requirements</span></span>



| <span data-ttu-id="74784-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74784-119">Requirement</span></span> | <span data-ttu-id="74784-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="74784-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74784-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="74784-121">Header</span></span><br/>  | <dl> <span data-ttu-id="74784-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="74784-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="74784-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="74784-123">Library</span></span><br/> | <dl> <span data-ttu-id="74784-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74784-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="74784-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74784-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74784-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="74784-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="74784-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="74784-127">**SetBool**</span></span>](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
