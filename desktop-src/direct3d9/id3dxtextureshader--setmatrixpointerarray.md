---
description: Définit un tableau de pointeurs vers des matrices non transposées.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: 'ID3DXTextureShader :: SetMatrixPointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bde5250ae8ceeab7522b9df15c99070e9471608
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322774"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a><span data-ttu-id="d56ac-103">ID3DXTextureShader :: SetMatrixPointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="d56ac-103">ID3DXTextureShader::SetMatrixPointerArray method</span></span>

<span data-ttu-id="d56ac-104">Définit un tableau de pointeurs vers des matrices non transposées.</span><span class="sxs-lookup"><span data-stu-id="d56ac-104">Sets an array of pointers to non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d56ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d56ac-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d56ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d56ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d56ac-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d56ac-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ac-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ac-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d56ac-109">Identificateur unique d’un tableau de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="d56ac-109">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="d56ac-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d56ac-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d56ac-111">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d56ac-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ac-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="d56ac-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="d56ac-113">Tableau de pointeurs vers des matrices non transposées.</span><span class="sxs-lookup"><span data-stu-id="d56ac-113">Array of pointers to non-transposed matrices.</span></span> <span data-ttu-id="d56ac-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="d56ac-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d56ac-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d56ac-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ac-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ac-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d56ac-117">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d56ac-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d56ac-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d56ac-118">Return value</span></span>

<span data-ttu-id="d56ac-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d56ac-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d56ac-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d56ac-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d56ac-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d56ac-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d56ac-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d56ac-122">Remarks</span></span>

<span data-ttu-id="d56ac-123">Une matrice non transposée contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="d56ac-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56ac-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d56ac-124">Requirements</span></span>



| <span data-ttu-id="d56ac-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d56ac-125">Requirement</span></span> | <span data-ttu-id="d56ac-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d56ac-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d56ac-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d56ac-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d56ac-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d56ac-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d56ac-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d56ac-129">Library</span></span><br/> | <dl> <span data-ttu-id="d56ac-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d56ac-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d56ac-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d56ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d56ac-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d56ac-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
