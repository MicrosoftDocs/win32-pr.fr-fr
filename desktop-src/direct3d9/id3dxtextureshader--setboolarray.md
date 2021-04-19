---
description: Définit un tableau de valeurs BOOL.
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'ID3DXTextureShader :: SetBoolArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523223"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="1d26a-103">ID3DXTextureShader :: SetBoolArray, méthode</span><span class="sxs-lookup"><span data-stu-id="1d26a-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="1d26a-104">Définit un tableau de valeurs BOOL.</span><span class="sxs-lookup"><span data-stu-id="1d26a-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d26a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d26a-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="1d26a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d26a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d26a-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d26a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d26a-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1d26a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1d26a-109">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="1d26a-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="1d26a-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="1d26a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d26a-111">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d26a-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d26a-112">Type : **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d26a-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d26a-113">Tableau de valeurs BOOL.</span><span class="sxs-lookup"><span data-stu-id="1d26a-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="1d26a-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d26a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d26a-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d26a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d26a-116">Nombre de valeurs BOOL dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1d26a-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d26a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d26a-117">Return value</span></span>

<span data-ttu-id="1d26a-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d26a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d26a-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d26a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1d26a-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1d26a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d26a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d26a-121">Requirements</span></span>



| <span data-ttu-id="1d26a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d26a-122">Requirement</span></span> | <span data-ttu-id="1d26a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d26a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d26a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d26a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d26a-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d26a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1d26a-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d26a-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d26a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d26a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1d26a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d26a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d26a-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="1d26a-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
