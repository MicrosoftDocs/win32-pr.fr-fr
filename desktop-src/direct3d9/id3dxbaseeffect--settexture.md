---
description: Définit une texture.
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'ID3DXBaseEffect :: SetTexture, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520300"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="d0341-103">ID3DXBaseEffect :: SetTexture, méthode</span><span class="sxs-lookup"><span data-stu-id="d0341-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="d0341-104">Définit une texture.</span><span class="sxs-lookup"><span data-stu-id="d0341-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0341-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0341-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="d0341-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0341-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0341-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0341-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d0341-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d0341-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="d0341-109">Unique identifier.</span></span> <span data-ttu-id="d0341-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d0341-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0341-111">*pTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0341-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0341-112">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="d0341-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="d0341-113">Objet texture.</span><span class="sxs-lookup"><span data-stu-id="d0341-113">Texture object.</span></span> <span data-ttu-id="d0341-114">Consultez [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="d0341-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0341-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0341-115">Return value</span></span>

<span data-ttu-id="d0341-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0341-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0341-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0341-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0341-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d0341-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0341-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0341-119">Requirements</span></span>



| <span data-ttu-id="d0341-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0341-120">Requirement</span></span> | <span data-ttu-id="d0341-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0341-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0341-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0341-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d0341-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0341-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d0341-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0341-124">Library</span></span><br/> | <dl> <span data-ttu-id="d0341-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0341-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d0341-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0341-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0341-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d0341-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="d0341-128">**GetTexture**</span><span class="sxs-lookup"><span data-stu-id="d0341-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
