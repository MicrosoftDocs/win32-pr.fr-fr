---
description: 'ID3DXTextureShader :: SetMatrixTransposePointerArray, méthode-définit un tableau de pointeurs vers des matrices transposées.'
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
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090147"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="86a15-103">ID3DXTextureShader :: SetMatrixTransposePointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="86a15-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="86a15-104">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="86a15-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86a15-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="86a15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86a15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a15-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86a15-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a15-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="86a15-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="86a15-109">Identificateur unique du tableau de constantes de matrice.</span><span class="sxs-lookup"><span data-stu-id="86a15-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="86a15-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="86a15-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="86a15-111">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86a15-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a15-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="86a15-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="86a15-113">Tableau de pointeurs vers les matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="86a15-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="86a15-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="86a15-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="86a15-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86a15-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a15-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86a15-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86a15-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="86a15-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a15-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86a15-118">Return value</span></span>

<span data-ttu-id="86a15-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86a15-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86a15-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86a15-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86a15-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="86a15-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a15-122">Notes </span><span class="sxs-lookup"><span data-stu-id="86a15-122">Remarks</span></span>

<span data-ttu-id="86a15-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="86a15-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a15-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86a15-124">Requirements</span></span>



| <span data-ttu-id="86a15-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86a15-125">Requirement</span></span> | <span data-ttu-id="86a15-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="86a15-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a15-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="86a15-127">Header</span></span><br/>  | <dl> <span data-ttu-id="86a15-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="86a15-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="86a15-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86a15-129">Library</span></span><br/> | <dl> <span data-ttu-id="86a15-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86a15-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="86a15-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86a15-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a15-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="86a15-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
