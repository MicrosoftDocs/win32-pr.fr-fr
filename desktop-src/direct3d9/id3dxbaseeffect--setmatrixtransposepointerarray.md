---
description: Définit un tableau de pointeurs vers des matrices transposées.
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: 'ID3DXBaseEffect :: SetMatrixTransposePointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1152deccdcadebe9f421fac6d7d5ce53c8d3e5f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535199"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="f79a8-103">ID3DXBaseEffect :: SetMatrixTransposePointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="f79a8-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="f79a8-104">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="f79a8-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f79a8-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="f79a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f79a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f79a8-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f79a8-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a8-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f79a8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f79a8-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="f79a8-109">Unique identifier.</span></span> <span data-ttu-id="f79a8-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f79a8-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f79a8-111">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f79a8-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a8-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="f79a8-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="f79a8-113">Tableau de pointeurs vers les matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="f79a8-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="f79a8-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="f79a8-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="f79a8-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f79a8-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a8-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f79a8-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f79a8-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f79a8-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f79a8-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f79a8-118">Return value</span></span>

<span data-ttu-id="f79a8-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f79a8-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f79a8-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f79a8-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f79a8-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f79a8-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f79a8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f79a8-122">Remarks</span></span>

<span data-ttu-id="f79a8-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="f79a8-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="f79a8-124">Si les matrices de destination sont plus petites que les matrices sources, les composants supplémentaires des matrices sources seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="f79a8-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f79a8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f79a8-125">Requirements</span></span>



| <span data-ttu-id="f79a8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f79a8-126">Requirement</span></span> | <span data-ttu-id="f79a8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f79a8-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79a8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f79a8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f79a8-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f79a8-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f79a8-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f79a8-130">Library</span></span><br/> | <dl> <span data-ttu-id="f79a8-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f79a8-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f79a8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f79a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79a8-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f79a8-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f79a8-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="f79a8-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
