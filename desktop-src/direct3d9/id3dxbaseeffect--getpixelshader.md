---
description: Obtient un nuanceur de pixels.
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: 'ID3DXBaseEffect :: GetPixelShader, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e555bac2e20ebab1cb0aec3d313cab8ad05e833e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537286"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a><span data-ttu-id="75d66-103">ID3DXBaseEffect :: GetPixelShader, méthode</span><span class="sxs-lookup"><span data-stu-id="75d66-103">ID3DXBaseEffect::GetPixelShader method</span></span>

<span data-ttu-id="75d66-104">Obtient un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="75d66-104">Gets a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d66-105">Syntax</span></span>


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a><span data-ttu-id="75d66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d66-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75d66-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d66-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="75d66-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="75d66-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="75d66-109">Unique identifier.</span></span> <span data-ttu-id="75d66-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="75d66-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="75d66-111">*ppPShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75d66-111">*ppPShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75d66-112">Type : **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span><span class="sxs-lookup"><span data-stu-id="75d66-112">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span></span>

<span data-ttu-id="75d66-113">Retourne un objet nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="75d66-113">Returns a pixel shader object.</span></span> <span data-ttu-id="75d66-114">Consultez l’objet [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) .</span><span class="sxs-lookup"><span data-stu-id="75d66-114">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d66-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75d66-115">Return value</span></span>

<span data-ttu-id="75d66-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75d66-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75d66-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75d66-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="75d66-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="75d66-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d66-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75d66-119">Requirements</span></span>



| <span data-ttu-id="75d66-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75d66-120">Requirement</span></span> | <span data-ttu-id="75d66-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="75d66-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d66-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="75d66-122">Header</span></span><br/>  | <dl> <span data-ttu-id="75d66-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d66-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="75d66-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75d66-124">Library</span></span><br/> | <dl> <span data-ttu-id="75d66-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75d66-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="75d66-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d66-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d66-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="75d66-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
