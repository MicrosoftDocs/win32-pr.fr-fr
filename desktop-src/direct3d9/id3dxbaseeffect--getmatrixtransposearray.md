---
description: Obtient un tableau de matrices transposées.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'ID3DXBaseEffect :: GetMatrixTransposeArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762356"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a><span data-ttu-id="17f1e-103">ID3DXBaseEffect :: GetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="17f1e-103">ID3DXBaseEffect::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="17f1e-104">Obtient un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="17f1e-104">Gets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f1e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17f1e-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="17f1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f1e-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17f1e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f1e-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="17f1e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="17f1e-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="17f1e-109">Unique identifier.</span></span> <span data-ttu-id="17f1e-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="17f1e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="17f1e-111">*pMatrix* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f1e-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f1e-112">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="17f1e-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="17f1e-113">Retourne un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="17f1e-113">Returns an array of transposed matrices.</span></span> <span data-ttu-id="17f1e-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="17f1e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="17f1e-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17f1e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f1e-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17f1e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17f1e-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="17f1e-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f1e-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17f1e-118">Return value</span></span>

<span data-ttu-id="17f1e-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17f1e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17f1e-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17f1e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17f1e-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17f1e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="17f1e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="17f1e-122">Remarks</span></span>

<span data-ttu-id="17f1e-123">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="17f1e-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="17f1e-124">Si les matrices de destination sont plus volumineuses que les matrices sources, seuls les composants situés en haut à gauche de chaque matrice de destination sont remplis et les autres composants de la matrice de destination sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="17f1e-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f1e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f1e-125">Requirements</span></span>



| <span data-ttu-id="17f1e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17f1e-126">Requirement</span></span> | <span data-ttu-id="17f1e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="17f1e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f1e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f1e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="17f1e-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f1e-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="17f1e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17f1e-130">Library</span></span><br/> | <dl> <span data-ttu-id="17f1e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17f1e-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="17f1e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f1e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f1e-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="17f1e-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="17f1e-134">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="17f1e-134">**SetMatrixTransposeArray**</span></span>](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
