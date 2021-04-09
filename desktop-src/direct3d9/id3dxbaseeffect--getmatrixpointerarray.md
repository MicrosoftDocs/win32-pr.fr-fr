---
description: Obtient un tableau de pointeurs vers des matrices nontransposed.
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'ID3DXBaseEffect :: GetMatrixPointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954003"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="3bcda-103">ID3DXBaseEffect :: GetMatrixPointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="3bcda-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="3bcda-104">Obtient un tableau de pointeurs vers des matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="3bcda-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bcda-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="3bcda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bcda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bcda-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3bcda-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bcda-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3bcda-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3bcda-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="3bcda-109">Unique identifier.</span></span> <span data-ttu-id="3bcda-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3bcda-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcda-111">*ppMatrix* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3bcda-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bcda-112">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3bcda-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="3bcda-113">Tableau de pointeurs vers les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="3bcda-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="3bcda-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3bcda-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcda-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3bcda-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bcda-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bcda-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bcda-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3bcda-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bcda-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bcda-118">Return value</span></span>

<span data-ttu-id="3bcda-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bcda-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bcda-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3bcda-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3bcda-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3bcda-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bcda-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3bcda-122">Remarks</span></span>

<span data-ttu-id="3bcda-123">Une matrice nontransposed contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="3bcda-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="3bcda-124">Si les matrices de destination sont plus volumineuses que les matrices sources, seuls les composants situés en haut à gauche de chaque matrice de destination sont remplis et les autres composants de la matrice de destination sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="3bcda-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bcda-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bcda-125">Requirements</span></span>



| <span data-ttu-id="3bcda-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bcda-126">Requirement</span></span> | <span data-ttu-id="3bcda-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bcda-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bcda-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bcda-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3bcda-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bcda-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3bcda-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3bcda-130">Library</span></span><br/> | <dl> <span data-ttu-id="3bcda-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bcda-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3bcda-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bcda-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bcda-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3bcda-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3bcda-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="3bcda-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
