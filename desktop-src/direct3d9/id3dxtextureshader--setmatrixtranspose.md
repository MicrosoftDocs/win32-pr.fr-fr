---
description: 'ID3DXTextureShader :: SetMatrixTranspose, méthode-définit une matrice transposée.'
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: 'ID3DXTextureShader :: SetMatrixTranspose, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91216b49dba7fabb25c128f3801d11bfa2fd95c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114297"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="9db63-103">ID3DXTextureShader :: SetMatrixTranspose, méthode</span><span class="sxs-lookup"><span data-stu-id="9db63-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="9db63-104">Définit une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="9db63-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9db63-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="9db63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9db63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db63-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9db63-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db63-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9db63-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9db63-109">Identificateur unique de la matrice de constantes.</span><span class="sxs-lookup"><span data-stu-id="9db63-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="9db63-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="9db63-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="9db63-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9db63-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db63-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9db63-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9db63-113">Pointeur désignant une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="9db63-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="9db63-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9db63-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db63-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9db63-115">Return value</span></span>

<span data-ttu-id="9db63-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9db63-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9db63-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9db63-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9db63-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9db63-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db63-119">Notes </span><span class="sxs-lookup"><span data-stu-id="9db63-119">Remarks</span></span>

<span data-ttu-id="9db63-120">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="9db63-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db63-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9db63-121">Requirements</span></span>



| <span data-ttu-id="9db63-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9db63-122">Requirement</span></span> | <span data-ttu-id="9db63-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9db63-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db63-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9db63-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9db63-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db63-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9db63-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9db63-126">Library</span></span><br/> | <dl> <span data-ttu-id="9db63-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9db63-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9db63-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9db63-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db63-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9db63-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




