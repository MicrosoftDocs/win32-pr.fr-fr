---
description: Définit un tableau de matrices transposées.
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
ms.openlocfilehash: e646761435f75688fe652683281297ca2b8de99e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543565"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="3c1bb-103">ID3DXBaseEffect :: SetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="3c1bb-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="3c1bb-104">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c1bb-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="3c1bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c1bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c1bb-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c1bb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1bb-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3c1bb-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-109">Unique identifier.</span></span> <span data-ttu-id="3c1bb-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3c1bb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c1bb-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c1bb-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1bb-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c1bb-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3c1bb-113">Tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-113">Array of transposed matrices.</span></span> <span data-ttu-id="3c1bb-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3c1bb-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c1bb-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c1bb-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1bb-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c1bb-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c1bb-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c1bb-118">Return value</span></span>

<span data-ttu-id="3c1bb-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c1bb-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c1bb-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c1bb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3c1bb-122">Remarks</span></span>

<span data-ttu-id="3c1bb-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="3c1bb-124">Si les matrices de destination sont plus petites que les matrices sources, les composants supplémentaires des matrices sources seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c1bb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c1bb-125">Requirements</span></span>



| <span data-ttu-id="3c1bb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c1bb-126">Requirement</span></span> | <span data-ttu-id="3c1bb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c1bb-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1bb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c1bb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3c1bb-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c1bb-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3c1bb-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c1bb-130">Library</span></span><br/> | <dl> <span data-ttu-id="3c1bb-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c1bb-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3c1bb-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c1bb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1bb-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3c1bb-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3c1bb-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
