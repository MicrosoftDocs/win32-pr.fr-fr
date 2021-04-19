---
description: Définit une matrice transposée.
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'ID3DXBaseEffect :: SetMatrixTranspose, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f62847f7b15899389cbd5f207ce810b0ed0dd119
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531310"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="448ea-103">ID3DXBaseEffect :: SetMatrixTranspose, méthode</span><span class="sxs-lookup"><span data-stu-id="448ea-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="448ea-104">Définit une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="448ea-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="448ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="448ea-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="448ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="448ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="448ea-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="448ea-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448ea-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="448ea-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="448ea-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="448ea-109">Unique identifier.</span></span> <span data-ttu-id="448ea-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="448ea-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="448ea-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="448ea-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448ea-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="448ea-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="448ea-113">Pointeur désignant une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="448ea-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="448ea-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="448ea-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="448ea-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="448ea-115">Return value</span></span>

<span data-ttu-id="448ea-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="448ea-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="448ea-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="448ea-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="448ea-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="448ea-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="448ea-119">Notes</span><span class="sxs-lookup"><span data-stu-id="448ea-119">Remarks</span></span>

<span data-ttu-id="448ea-120">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="448ea-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="448ea-121">Si la matrice de destination est plus petite que la matrice source, les composants supplémentaires de la matrice source seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="448ea-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="448ea-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="448ea-122">Requirements</span></span>



| <span data-ttu-id="448ea-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="448ea-123">Requirement</span></span> | <span data-ttu-id="448ea-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="448ea-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="448ea-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="448ea-125">Header</span></span><br/>  | <dl> <span data-ttu-id="448ea-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="448ea-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="448ea-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="448ea-127">Library</span></span><br/> | <dl> <span data-ttu-id="448ea-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="448ea-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="448ea-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="448ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448ea-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="448ea-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="448ea-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="448ea-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




