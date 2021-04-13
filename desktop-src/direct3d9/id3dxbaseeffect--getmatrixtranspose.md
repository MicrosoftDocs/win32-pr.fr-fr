---
description: Obtient une matrice transposée.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'ID3DXBaseEffect :: GetMatrixTranspose, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323333"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a><span data-ttu-id="242fd-103">ID3DXBaseEffect :: GetMatrixTranspose, méthode</span><span class="sxs-lookup"><span data-stu-id="242fd-103">ID3DXBaseEffect::GetMatrixTranspose method</span></span>

<span data-ttu-id="242fd-104">Obtient une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="242fd-104">Gets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="242fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="242fd-105">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="242fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="242fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242fd-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="242fd-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242fd-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="242fd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="242fd-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="242fd-109">Unique identifier.</span></span> <span data-ttu-id="242fd-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="242fd-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="242fd-111">*pMatrix* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="242fd-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="242fd-112">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="242fd-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="242fd-113">Retourne une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="242fd-113">Returns a transposed matrix.</span></span> <span data-ttu-id="242fd-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="242fd-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242fd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="242fd-115">Return value</span></span>

<span data-ttu-id="242fd-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="242fd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="242fd-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="242fd-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="242fd-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="242fd-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="242fd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="242fd-119">Remarks</span></span>

<span data-ttu-id="242fd-120">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="242fd-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="242fd-121">Si la matrice de destination est plus grande que la matrice source, seuls les éléments supérieurs gauches de la matrice de destination sont remplis et les autres composants de la matrice de destination sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="242fd-121">If the destination matrix is larger than the source matrix, only the upper-left elements of the destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="242fd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="242fd-122">Requirements</span></span>



| <span data-ttu-id="242fd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="242fd-123">Requirement</span></span> | <span data-ttu-id="242fd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="242fd-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="242fd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="242fd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="242fd-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="242fd-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="242fd-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="242fd-127">Library</span></span><br/> | <dl> <span data-ttu-id="242fd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="242fd-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="242fd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="242fd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="242fd-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="242fd-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="242fd-131">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="242fd-131">**SetMatrixTranspose**</span></span>](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




