---
description: Définit un nombre à virgule flottante.
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'ID3DXTextureShader :: SetFloat, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85923fe20731b4482f70c439cb9df75712ab09f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525906"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="085ce-103">ID3DXTextureShader :: SetFloat, méthode</span><span class="sxs-lookup"><span data-stu-id="085ce-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="085ce-104">Définit un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="085ce-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="085ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="085ce-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="085ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="085ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085ce-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="085ce-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085ce-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="085ce-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="085ce-109">Identificateur unique de la constante.</span><span class="sxs-lookup"><span data-stu-id="085ce-109">Unique identifier to the constant.</span></span> <span data-ttu-id="085ce-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="085ce-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="085ce-111">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="085ce-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085ce-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="085ce-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="085ce-113">Nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="085ce-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="085ce-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="085ce-114">Return value</span></span>

<span data-ttu-id="085ce-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="085ce-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="085ce-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="085ce-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="085ce-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="085ce-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="085ce-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="085ce-118">Requirements</span></span>



| <span data-ttu-id="085ce-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="085ce-119">Requirement</span></span> | <span data-ttu-id="085ce-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="085ce-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="085ce-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="085ce-121">Header</span></span><br/>  | <dl> <span data-ttu-id="085ce-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="085ce-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="085ce-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="085ce-123">Library</span></span><br/> | <dl> <span data-ttu-id="085ce-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="085ce-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="085ce-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="085ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085ce-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="085ce-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
