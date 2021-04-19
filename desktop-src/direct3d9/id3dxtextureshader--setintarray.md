---
description: Définit un tableau d’entiers.
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'ID3DXTextureShader :: SetIntArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532450"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="d47f4-103">ID3DXTextureShader :: SetIntArray, méthode</span><span class="sxs-lookup"><span data-stu-id="d47f4-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="d47f4-104">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="d47f4-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47f4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d47f4-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d47f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d47f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47f4-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d47f4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47f4-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d47f4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d47f4-109">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="d47f4-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="d47f4-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d47f4-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d47f4-111">*PN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d47f4-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47f4-112">Type : **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d47f4-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d47f4-113">Tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="d47f4-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="d47f4-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d47f4-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47f4-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d47f4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d47f4-116">Nombre d’entiers dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d47f4-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47f4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d47f4-117">Return value</span></span>

<span data-ttu-id="d47f4-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d47f4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d47f4-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d47f4-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d47f4-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d47f4-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47f4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d47f4-121">Requirements</span></span>



| <span data-ttu-id="d47f4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d47f4-122">Requirement</span></span> | <span data-ttu-id="d47f4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d47f4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47f4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d47f4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d47f4-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d47f4-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d47f4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d47f4-126">Library</span></span><br/> | <dl> <span data-ttu-id="d47f4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d47f4-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d47f4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d47f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47f4-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d47f4-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
