---
description: 'ID3DXBaseEffect :: SetMatrixTransposePointerArray, méthode-définit un tableau de pointeurs vers des matrices transposées.'
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
ms.openlocfilehash: 3f35afad1120a26a60f670d12410584b2f9db7f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107387"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="5ca0e-103">ID3DXBaseEffect :: SetMatrixTransposePointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="5ca0e-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="5ca0e-104">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ca0e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="5ca0e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ca0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca0e-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ca0e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0e-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5ca0e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5ca0e-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-109">Unique identifier.</span></span> <span data-ttu-id="5ca0e-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5ca0e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca0e-111">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ca0e-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0e-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="5ca0e-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="5ca0e-113">Tableau de pointeurs vers les matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="5ca0e-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5ca0e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca0e-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ca0e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0e-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ca0e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ca0e-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca0e-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ca0e-118">Return value</span></span>

<span data-ttu-id="5ca0e-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ca0e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ca0e-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ca0e-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca0e-122">Notes </span><span class="sxs-lookup"><span data-stu-id="5ca0e-122">Remarks</span></span>

<span data-ttu-id="5ca0e-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="5ca0e-124">Si les matrices de destination sont plus petites que les matrices sources, les composants supplémentaires des matrices sources seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="5ca0e-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca0e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ca0e-125">Requirements</span></span>



| <span data-ttu-id="5ca0e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ca0e-126">Requirement</span></span> | <span data-ttu-id="5ca0e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ca0e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca0e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ca0e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5ca0e-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca0e-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5ca0e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ca0e-130">Library</span></span><br/> | <dl> <span data-ttu-id="5ca0e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ca0e-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5ca0e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ca0e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca0e-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5ca0e-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5ca0e-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="5ca0e-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
