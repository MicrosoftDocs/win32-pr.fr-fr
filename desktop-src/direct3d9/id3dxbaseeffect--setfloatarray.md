---
description: Définit un tableau de valeurs à virgule flottante.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'ID3DXBaseEffect :: SetFloatArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211679"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="fb5db-103">ID3DXBaseEffect :: SetFloatArray, méthode</span><span class="sxs-lookup"><span data-stu-id="fb5db-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="fb5db-104">Définit un tableau de valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="fb5db-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb5db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb5db-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="fb5db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb5db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb5db-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb5db-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb5db-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fb5db-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fb5db-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="fb5db-109">Unique identifier.</span></span> <span data-ttu-id="fb5db-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fb5db-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb5db-111">*PF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb5db-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb5db-112">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb5db-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fb5db-113">Tableau de valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="fb5db-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="fb5db-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb5db-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb5db-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb5db-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb5db-116">Nombre de valeurs à virgule flottante dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="fb5db-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb5db-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb5db-117">Return value</span></span>

<span data-ttu-id="fb5db-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb5db-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb5db-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb5db-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb5db-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fb5db-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb5db-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb5db-121">Requirements</span></span>



| <span data-ttu-id="fb5db-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb5db-122">Requirement</span></span> | <span data-ttu-id="fb5db-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb5db-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb5db-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb5db-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb5db-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb5db-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fb5db-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb5db-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb5db-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb5db-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fb5db-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb5db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb5db-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fb5db-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fb5db-130">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="fb5db-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
