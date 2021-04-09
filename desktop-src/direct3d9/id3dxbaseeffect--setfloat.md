---
description: Définit une valeur à virgule flottante.
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'ID3DXBaseEffect :: SetFloat, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af955748fff66e67e0e2f5650b869a746168de54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870078"
---
# <a name="id3dxbaseeffectsetfloat-method"></a><span data-ttu-id="0e566-103">ID3DXBaseEffect :: SetFloat, méthode</span><span class="sxs-lookup"><span data-stu-id="0e566-103">ID3DXBaseEffect::SetFloat method</span></span>

<span data-ttu-id="0e566-104">Définit une valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0e566-104">Sets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e566-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e566-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="0e566-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e566-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e566-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e566-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0e566-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0e566-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="0e566-109">Unique identifier.</span></span> <span data-ttu-id="0e566-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0e566-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e566-111">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e566-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e566-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e566-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e566-113">Valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0e566-113">Floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e566-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e566-114">Return value</span></span>

<span data-ttu-id="0e566-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e566-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e566-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e566-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e566-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0e566-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e566-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e566-118">Requirements</span></span>



| <span data-ttu-id="0e566-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e566-119">Requirement</span></span> | <span data-ttu-id="0e566-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e566-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e566-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e566-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0e566-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e566-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0e566-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e566-123">Library</span></span><br/> | <dl> <span data-ttu-id="0e566-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e566-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0e566-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e566-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e566-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0e566-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0e566-127">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="0e566-127">**GetFloat**</span></span>](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
