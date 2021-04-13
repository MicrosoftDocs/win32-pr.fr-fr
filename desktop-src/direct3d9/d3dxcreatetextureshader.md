---
description: Crée un objet de nuanceur de texture à partir du nuanceur compilé.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: D3DXCreateTextureShader, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322938"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="dbdbf-103">D3DXCreateTextureShader fonction)</span><span class="sxs-lookup"><span data-stu-id="dbdbf-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="dbdbf-104">Crée un objet de nuanceur de texture à partir du nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="dbdbf-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbdbf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbdbf-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="dbdbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbdbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbdbf-107">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dbdbf-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbdbf-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dbdbf-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dbdbf-109">Pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="dbdbf-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="dbdbf-110">*ppTextureShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbdbf-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbdbf-111">Type : **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbdbf-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="dbdbf-112">Retourne un objet [**ID3DXTextureShader**](id3dxtextureshader.md) qui peut être utilisé pour remplir de façon procédurale le contenu d’une texture à l’aide des fonctions [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .</span><span class="sxs-lookup"><span data-stu-id="dbdbf-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbdbf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbdbf-113">Return value</span></span>

<span data-ttu-id="dbdbf-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbdbf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbdbf-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbdbf-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dbdbf-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dbdbf-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbdbf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbdbf-117">Requirements</span></span>



| <span data-ttu-id="dbdbf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbdbf-118">Requirement</span></span> | <span data-ttu-id="dbdbf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbdbf-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbdbf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbdbf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dbdbf-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbdbf-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dbdbf-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dbdbf-122">Library</span></span><br/> | <dl> <span data-ttu-id="dbdbf-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbdbf-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dbdbf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbdbf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbdbf-125">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="dbdbf-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
