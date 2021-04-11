---
description: Définit une matrice non transposée.
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'ID3DXTextureShader :: SetMatrix, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c52fa8d363200222197ac40563fb0dd66e71f7a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116198"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="58ae9-103">ID3DXTextureShader :: SetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="58ae9-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="58ae9-104">Définit une matrice non transposée.</span><span class="sxs-lookup"><span data-stu-id="58ae9-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ae9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58ae9-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="58ae9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58ae9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ae9-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ae9-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ae9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="58ae9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="58ae9-109">Identificateur unique de la matrice de constantes.</span><span class="sxs-lookup"><span data-stu-id="58ae9-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="58ae9-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="58ae9-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="58ae9-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ae9-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ae9-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="58ae9-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58ae9-113">Pointeur désignant une matrice non transposée.</span><span class="sxs-lookup"><span data-stu-id="58ae9-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="58ae9-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="58ae9-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ae9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58ae9-115">Return value</span></span>

<span data-ttu-id="58ae9-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58ae9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58ae9-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58ae9-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="58ae9-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="58ae9-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="58ae9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="58ae9-119">Remarks</span></span>

<span data-ttu-id="58ae9-120">Une matrice non transposée contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="58ae9-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ae9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ae9-121">Requirements</span></span>



| <span data-ttu-id="58ae9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ae9-122">Requirement</span></span> | <span data-ttu-id="58ae9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ae9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ae9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="58ae9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="58ae9-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ae9-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="58ae9-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58ae9-126">Library</span></span><br/> | <dl> <span data-ttu-id="58ae9-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ae9-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="58ae9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ae9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ae9-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="58ae9-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




