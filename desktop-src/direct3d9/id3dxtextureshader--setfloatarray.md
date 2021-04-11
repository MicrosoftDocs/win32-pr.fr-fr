---
description: Définit un tableau de nombres à virgule flottante.
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
ms.openlocfilehash: 5dbd39e8a4acfa004fb623d578e5922d477884fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211787"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="4306c-103">ID3DXTextureShader :: SetFloatArray, méthode</span><span class="sxs-lookup"><span data-stu-id="4306c-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="4306c-104">Définit un tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="4306c-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4306c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4306c-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="4306c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4306c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4306c-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4306c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4306c-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4306c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4306c-109">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="4306c-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="4306c-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="4306c-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="4306c-111">*PF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4306c-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4306c-112">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4306c-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4306c-113">Tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="4306c-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="4306c-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4306c-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4306c-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4306c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4306c-116">Nombre de valeurs à virgule flottante dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="4306c-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4306c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4306c-117">Return value</span></span>

<span data-ttu-id="4306c-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4306c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4306c-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4306c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4306c-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4306c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4306c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4306c-121">Requirements</span></span>



| <span data-ttu-id="4306c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4306c-122">Requirement</span></span> | <span data-ttu-id="4306c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4306c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4306c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4306c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4306c-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4306c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4306c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4306c-126">Library</span></span><br/> | <dl> <span data-ttu-id="4306c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4306c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4306c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4306c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4306c-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="4306c-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
