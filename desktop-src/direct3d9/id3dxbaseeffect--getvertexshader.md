---
description: Obtient un nuanceur de sommets.
ms.assetid: ab58b465-7b10-46eb-88c0-c5229cb09481
title: 'ID3DXBaseEffect :: GetVertexShader, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ad6bb7cbf7c483ccaffa83b0e828c867026957fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116171"
---
# <a name="id3dxbaseeffectgetvertexshader-method"></a><span data-ttu-id="1f19b-103">ID3DXBaseEffect :: GetVertexShader, méthode</span><span class="sxs-lookup"><span data-stu-id="1f19b-103">ID3DXBaseEffect::GetVertexShader method</span></span>

<span data-ttu-id="1f19b-104">Obtient un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="1f19b-104">Gets a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f19b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f19b-105">Syntax</span></span>


```C++
HRESULT GetVertexShader(
  [in]  D3DXHANDLE              hParameter,
  [out] LPDIRECT3DVERTEXSHADER9 *ppVShader
);
```



## <a name="parameters"></a><span data-ttu-id="1f19b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f19b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f19b-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f19b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f19b-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1f19b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1f19b-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="1f19b-109">Unique identifier.</span></span> <span data-ttu-id="1f19b-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1f19b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f19b-111">*ppVShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f19b-111">*ppVShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f19b-112">Type : **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span><span class="sxs-lookup"><span data-stu-id="1f19b-112">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span></span>

<span data-ttu-id="1f19b-113">Retourne un objet de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="1f19b-113">Returns a vertex shader object.</span></span> <span data-ttu-id="1f19b-114">Consultez [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="1f19b-114">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f19b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f19b-115">Return value</span></span>

<span data-ttu-id="1f19b-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f19b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f19b-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f19b-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1f19b-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1f19b-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f19b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f19b-119">Requirements</span></span>



| <span data-ttu-id="1f19b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f19b-120">Requirement</span></span> | <span data-ttu-id="1f19b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f19b-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f19b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f19b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1f19b-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f19b-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1f19b-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f19b-124">Library</span></span><br/> | <dl> <span data-ttu-id="1f19b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f19b-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1f19b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f19b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f19b-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1f19b-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
