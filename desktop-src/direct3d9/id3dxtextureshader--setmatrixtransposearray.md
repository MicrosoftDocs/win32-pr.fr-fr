---
description: Définit un tableau de matrices transposées.
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'ID3DXTextureShader :: SetMatrixTransposeArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9efd0c81cef8a72880a9755ca40e4dd8b4950ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953828"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="1f16c-103">ID3DXTextureShader :: SetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="1f16c-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="1f16c-104">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="1f16c-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f16c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f16c-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="1f16c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f16c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f16c-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f16c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f16c-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1f16c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1f16c-109">Identificateur unique du tableau de constantes de matrice.</span><span class="sxs-lookup"><span data-stu-id="1f16c-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="1f16c-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="1f16c-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f16c-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f16c-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f16c-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f16c-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1f16c-113">Tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="1f16c-113">Array of transposed matrices.</span></span> <span data-ttu-id="1f16c-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1f16c-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f16c-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f16c-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f16c-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f16c-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f16c-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1f16c-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f16c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f16c-118">Return value</span></span>

<span data-ttu-id="1f16c-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f16c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f16c-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f16c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1f16c-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1f16c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f16c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1f16c-122">Remarks</span></span>

<span data-ttu-id="1f16c-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="1f16c-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f16c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f16c-124">Requirements</span></span>



| <span data-ttu-id="1f16c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f16c-125">Requirement</span></span> | <span data-ttu-id="1f16c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f16c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f16c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f16c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1f16c-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f16c-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1f16c-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f16c-129">Library</span></span><br/> | <dl> <span data-ttu-id="1f16c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f16c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1f16c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f16c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f16c-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="1f16c-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
