---
description: 'ID3DXTextureShader :: SetVector, méthode-définit un vecteur 4D.'
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'ID3DXTextureShader :: SetVector, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e917e4ff13cf7c03de264542dc1995364f1dc526
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090157"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="ccc2f-103">ID3DXTextureShader :: SetVector, méthode</span><span class="sxs-lookup"><span data-stu-id="ccc2f-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="ccc2f-104">Définit un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="ccc2f-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc2f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccc2f-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="ccc2f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccc2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc2f-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccc2f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc2f-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc2f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ccc2f-109">Identificateur unique de la constante Vector.</span><span class="sxs-lookup"><span data-stu-id="ccc2f-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="ccc2f-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="ccc2f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccc2f-111">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccc2f-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc2f-112">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccc2f-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ccc2f-113">Pointeur vers un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="ccc2f-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="ccc2f-114">Consultez [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="ccc2f-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc2f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ccc2f-115">Return value</span></span>

<span data-ttu-id="ccc2f-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccc2f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccc2f-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ccc2f-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ccc2f-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ccc2f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc2f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccc2f-119">Requirements</span></span>



| <span data-ttu-id="ccc2f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccc2f-120">Requirement</span></span> | <span data-ttu-id="ccc2f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccc2f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc2f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccc2f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ccc2f-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc2f-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ccc2f-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ccc2f-124">Library</span></span><br/> | <dl> <span data-ttu-id="ccc2f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccc2f-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ccc2f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccc2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc2f-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ccc2f-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




