---
description: Définit une valeur BOOL.
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'ID3DXTextureShader :: SetBool, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fbc2d2841957e75a8bc3adaf40ce0fdf5e2a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762253"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="62098-103">ID3DXTextureShader :: SetBool, méthode</span><span class="sxs-lookup"><span data-stu-id="62098-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="62098-104">Définit une valeur BOOL.</span><span class="sxs-lookup"><span data-stu-id="62098-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="62098-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62098-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="62098-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62098-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62098-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62098-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="62098-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="62098-109">Identificateur unique de la constante.</span><span class="sxs-lookup"><span data-stu-id="62098-109">Unique identifier to the constant.</span></span> <span data-ttu-id="62098-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="62098-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="62098-111">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62098-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62098-112">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62098-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62098-113">Valeur BOOL.</span><span class="sxs-lookup"><span data-stu-id="62098-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62098-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62098-114">Return value</span></span>

<span data-ttu-id="62098-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62098-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62098-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62098-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62098-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="62098-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="62098-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62098-118">Requirements</span></span>



| <span data-ttu-id="62098-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62098-119">Requirement</span></span> | <span data-ttu-id="62098-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="62098-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62098-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="62098-121">Header</span></span><br/>  | <dl> <span data-ttu-id="62098-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="62098-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="62098-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62098-123">Library</span></span><br/> | <dl> <span data-ttu-id="62098-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62098-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="62098-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62098-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62098-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="62098-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
