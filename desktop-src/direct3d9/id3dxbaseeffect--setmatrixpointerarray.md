---
description: Définit un tableau de pointeurs sur les matrices nontransposed.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'ID3DXBaseEffect :: SetMatrixPointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953794"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="276fb-103">ID3DXBaseEffect :: SetMatrixPointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="276fb-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="276fb-104">Définit un tableau de pointeurs sur les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="276fb-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="276fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="276fb-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="276fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="276fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276fb-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="276fb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276fb-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="276fb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="276fb-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="276fb-109">Unique identifier.</span></span> <span data-ttu-id="276fb-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="276fb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="276fb-111">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="276fb-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276fb-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="276fb-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="276fb-113">Tableau de pointeurs vers les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="276fb-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="276fb-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="276fb-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="276fb-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="276fb-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276fb-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="276fb-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="276fb-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="276fb-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276fb-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="276fb-118">Return value</span></span>

<span data-ttu-id="276fb-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="276fb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="276fb-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="276fb-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="276fb-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="276fb-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="276fb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="276fb-122">Remarks</span></span>

<span data-ttu-id="276fb-123">Une matrice nontransposed contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="276fb-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="276fb-124">Si les matrices de destination sont plus petites que les matrices sources, les composants supplémentaires des matrices sources seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="276fb-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="276fb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="276fb-125">Requirements</span></span>



| <span data-ttu-id="276fb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="276fb-126">Requirement</span></span> | <span data-ttu-id="276fb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="276fb-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="276fb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="276fb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="276fb-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="276fb-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="276fb-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="276fb-130">Library</span></span><br/> | <dl> <span data-ttu-id="276fb-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="276fb-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="276fb-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="276fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276fb-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="276fb-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="276fb-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="276fb-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
