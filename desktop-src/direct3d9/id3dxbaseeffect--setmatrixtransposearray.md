---
description: 'ID3DXBaseEffect :: SetMatrixTransposeArray, méthode-définit un tableau de matrices transposées.'
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: 'ID3DXBaseEffect :: SetMatrixTransposeArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7f145dc45f053e208f7890c8afdac6422ecde13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097507"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="a3fbb-103">ID3DXBaseEffect :: SetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="a3fbb-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="a3fbb-104">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3fbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3fbb-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="a3fbb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3fbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3fbb-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3fbb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fbb-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a3fbb-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-109">Unique identifier.</span></span> <span data-ttu-id="a3fbb-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a3fbb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3fbb-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3fbb-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fbb-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3fbb-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a3fbb-113">Tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-113">Array of transposed matrices.</span></span> <span data-ttu-id="a3fbb-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a3fbb-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3fbb-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3fbb-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fbb-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3fbb-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3fbb-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3fbb-118">Return value</span></span>

<span data-ttu-id="a3fbb-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3fbb-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3fbb-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3fbb-122">Notes </span><span class="sxs-lookup"><span data-stu-id="a3fbb-122">Remarks</span></span>

<span data-ttu-id="a3fbb-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="a3fbb-124">Si les matrices de destination sont plus petites que les matrices sources, les composants supplémentaires des matrices sources seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3fbb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3fbb-125">Requirements</span></span>



| <span data-ttu-id="a3fbb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3fbb-126">Requirement</span></span> | <span data-ttu-id="a3fbb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3fbb-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fbb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3fbb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a3fbb-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3fbb-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a3fbb-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3fbb-130">Library</span></span><br/> | <dl> <span data-ttu-id="a3fbb-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3fbb-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a3fbb-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3fbb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3fbb-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a3fbb-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a3fbb-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
