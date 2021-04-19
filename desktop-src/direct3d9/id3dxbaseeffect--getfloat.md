---
description: Obtient une valeur à virgule flottante.
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: 'ID3DXBaseEffect :: GetFloat, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528576"
---
# <a name="id3dxbaseeffectgetfloat-method"></a><span data-ttu-id="d1226-103">ID3DXBaseEffect :: GetFloat, méthode</span><span class="sxs-lookup"><span data-stu-id="d1226-103">ID3DXBaseEffect::GetFloat method</span></span>

<span data-ttu-id="d1226-104">Obtient une valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d1226-104">Gets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1226-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1226-105">Syntax</span></span>


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a><span data-ttu-id="d1226-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1226-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1226-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1226-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d1226-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d1226-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="d1226-109">Unique identifier.</span></span> <span data-ttu-id="d1226-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d1226-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1226-111">*PF* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d1226-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1226-112">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1226-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1226-113">Retourne une valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d1226-113">Returns a floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1226-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1226-114">Return value</span></span>

<span data-ttu-id="d1226-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1226-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1226-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1226-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1226-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d1226-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1226-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1226-118">Requirements</span></span>



| <span data-ttu-id="d1226-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1226-119">Requirement</span></span> | <span data-ttu-id="d1226-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1226-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1226-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1226-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d1226-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1226-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d1226-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1226-123">Library</span></span><br/> | <dl> <span data-ttu-id="d1226-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1226-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d1226-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1226-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1226-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d1226-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="d1226-127">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="d1226-127">**SetFloat**</span></span>](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
