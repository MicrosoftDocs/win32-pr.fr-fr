---
description: 'ID3DXTextureShader :: SetVectorArray, méthode-définit un tableau de vecteurs 4D.'
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'ID3DXTextureShader :: SetVectorArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0878594baa8828c9cca4eca8dd2c20f225fb530e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090187"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="8d9dd-103">ID3DXTextureShader :: SetVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="8d9dd-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="8d9dd-104">Définit un tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="8d9dd-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d9dd-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="8d9dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d9dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9dd-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d9dd-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9dd-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9dd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8d9dd-109">Identificateur unique du tableau de constantes vectorielles.</span><span class="sxs-lookup"><span data-stu-id="8d9dd-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="8d9dd-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="8d9dd-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d9dd-111">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d9dd-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9dd-112">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d9dd-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8d9dd-113">Tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="8d9dd-113">Array of 4D vectors.</span></span> <span data-ttu-id="8d9dd-114">Consultez [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="8d9dd-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d9dd-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d9dd-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9dd-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9dd-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d9dd-117">Nombre de vecteurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8d9dd-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9dd-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d9dd-118">Return value</span></span>

<span data-ttu-id="8d9dd-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d9dd-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d9dd-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d9dd-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d9dd-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8d9dd-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9dd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d9dd-122">Requirements</span></span>



| <span data-ttu-id="8d9dd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d9dd-123">Requirement</span></span> | <span data-ttu-id="8d9dd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d9dd-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9dd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d9dd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8d9dd-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9dd-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8d9dd-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d9dd-127">Library</span></span><br/> | <dl> <span data-ttu-id="8d9dd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9dd-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8d9dd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d9dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9dd-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8d9dd-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
