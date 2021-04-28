---
description: 'ID3DXTextureShader :: SetFloatArray, méthode-définit un tableau de nombres à virgule flottante.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'ID3DXTextureShader :: SetFloatArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090247"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="d4e2a-103">ID3DXTextureShader :: SetFloatArray, méthode</span><span class="sxs-lookup"><span data-stu-id="d4e2a-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="d4e2a-104">Définit un tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d4e2a-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e2a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4e2a-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d4e2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e2a-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4e2a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e2a-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d4e2a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d4e2a-109">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="d4e2a-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="d4e2a-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d4e2a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4e2a-111">*PF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4e2a-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e2a-112">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4e2a-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d4e2a-113">Tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d4e2a-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="d4e2a-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4e2a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e2a-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4e2a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4e2a-116">Nombre de valeurs à virgule flottante dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d4e2a-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e2a-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4e2a-117">Return value</span></span>

<span data-ttu-id="d4e2a-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4e2a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4e2a-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4e2a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d4e2a-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d4e2a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e2a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4e2a-121">Requirements</span></span>



| <span data-ttu-id="d4e2a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4e2a-122">Requirement</span></span> | <span data-ttu-id="d4e2a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e2a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e2a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4e2a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4e2a-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4e2a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d4e2a-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4e2a-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4e2a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4e2a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d4e2a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4e2a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e2a-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d4e2a-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
