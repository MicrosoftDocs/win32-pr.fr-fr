---
description: Définit un tableau de matrices non transposées.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'ID3DXTextureShader :: SetMatrixArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106540926"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a><span data-ttu-id="b19c3-103">ID3DXTextureShader :: SetMatrixArray, méthode</span><span class="sxs-lookup"><span data-stu-id="b19c3-103">ID3DXTextureShader::SetMatrixArray method</span></span>

<span data-ttu-id="b19c3-104">Définit un tableau de matrices non transposées.</span><span class="sxs-lookup"><span data-stu-id="b19c3-104">Sets an array of non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b19c3-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b19c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b19c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b19c3-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b19c3-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b19c3-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b19c3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b19c3-109">Identificateur unique du tableau de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="b19c3-109">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="b19c3-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="b19c3-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="b19c3-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b19c3-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b19c3-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b19c3-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b19c3-113">Tableau de matrices non transposées.</span><span class="sxs-lookup"><span data-stu-id="b19c3-113">Array of non-transposed matrices.</span></span> <span data-ttu-id="b19c3-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b19c3-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b19c3-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b19c3-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b19c3-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b19c3-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b19c3-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b19c3-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b19c3-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b19c3-118">Return value</span></span>

<span data-ttu-id="b19c3-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b19c3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b19c3-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b19c3-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b19c3-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b19c3-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b19c3-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b19c3-122">Remarks</span></span>

<span data-ttu-id="b19c3-123">Une matrice non transposée contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="b19c3-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19c3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b19c3-124">Requirements</span></span>



| <span data-ttu-id="b19c3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b19c3-125">Requirement</span></span> | <span data-ttu-id="b19c3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b19c3-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b19c3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b19c3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b19c3-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b19c3-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b19c3-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b19c3-129">Library</span></span><br/> | <dl> <span data-ttu-id="b19c3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b19c3-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b19c3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b19c3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b19c3-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b19c3-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
