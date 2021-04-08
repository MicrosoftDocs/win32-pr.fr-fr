---
description: Obtient une texture.
ms.assetid: e009ccc2-4491-4976-9460-7478b2bd34c2
title: 'ID3DXBaseEffect :: GetTexture, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 25ef71df1f9dcd84bbe6726fd3a13f9ec09eff17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761942"
---
# <a name="id3dxbaseeffectgettexture-method"></a><span data-ttu-id="06447-103">ID3DXBaseEffect :: GetTexture, méthode</span><span class="sxs-lookup"><span data-stu-id="06447-103">ID3DXBaseEffect::GetTexture method</span></span>

<span data-ttu-id="06447-104">Obtient une texture.</span><span class="sxs-lookup"><span data-stu-id="06447-104">Gets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="06447-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06447-105">Syntax</span></span>


```C++
HRESULT GetTexture(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DBASETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="06447-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06447-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06447-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06447-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06447-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="06447-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="06447-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="06447-109">Unique identifier.</span></span> <span data-ttu-id="06447-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="06447-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="06447-111">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06447-111">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06447-112">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="06447-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="06447-113">Retourne un objet de texture.</span><span class="sxs-lookup"><span data-stu-id="06447-113">Returns a texture object.</span></span> <span data-ttu-id="06447-114">Consultez [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="06447-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06447-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06447-115">Return value</span></span>

<span data-ttu-id="06447-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06447-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06447-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06447-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06447-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="06447-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="06447-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06447-119">Requirements</span></span>



| <span data-ttu-id="06447-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06447-120">Requirement</span></span> | <span data-ttu-id="06447-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="06447-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06447-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="06447-122">Header</span></span><br/>  | <dl> <span data-ttu-id="06447-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="06447-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="06447-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06447-124">Library</span></span><br/> | <dl> <span data-ttu-id="06447-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06447-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="06447-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06447-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06447-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="06447-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="06447-128">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="06447-128">**SetTexture**</span></span>](id3dxbaseeffect--settexture.md)
</dt> </dl>

 

 
