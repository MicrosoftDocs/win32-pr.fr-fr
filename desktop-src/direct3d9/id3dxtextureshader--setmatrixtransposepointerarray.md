---
description: Définit un tableau de pointeurs vers des matrices transposées.
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'ID3DXTextureShader :: SetMatrixTransposePointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd7c81dcb0fd9b9354c2536a91abaebfe8e4315b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542162"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="8c0f5-103">ID3DXTextureShader :: SetMatrixTransposePointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="8c0f5-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="8c0f5-104">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c0f5-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="8c0f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c0f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0f5-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c0f5-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f5-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8c0f5-109">Identificateur unique du tableau de constantes de matrice.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="8c0f5-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="8c0f5-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c0f5-111">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c0f5-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f5-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="8c0f5-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="8c0f5-113">Tableau de pointeurs vers les matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="8c0f5-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="8c0f5-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c0f5-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c0f5-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f5-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f5-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c0f5-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0f5-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c0f5-118">Return value</span></span>

<span data-ttu-id="8c0f5-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c0f5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c0f5-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c0f5-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0f5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8c0f5-122">Remarks</span></span>

<span data-ttu-id="8c0f5-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="8c0f5-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0f5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c0f5-124">Requirements</span></span>



| <span data-ttu-id="8c0f5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c0f5-125">Requirement</span></span> | <span data-ttu-id="8c0f5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c0f5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0f5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c0f5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8c0f5-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f5-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8c0f5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c0f5-129">Library</span></span><br/> | <dl> <span data-ttu-id="8c0f5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f5-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8c0f5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c0f5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0f5-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8c0f5-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
