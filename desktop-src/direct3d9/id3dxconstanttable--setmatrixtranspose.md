---
description: 'ID3DXConstantTable :: SetMatrixTranspose, méthode-définit une matrice transposée.'
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'ID3DXConstantTable :: SetMatrixTranspose, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06cc989a14da6f2fe84d30f7f5d7d9fc35acd3bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115057"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="0be4c-103">ID3DXConstantTable :: SetMatrixTranspose, méthode</span><span class="sxs-lookup"><span data-stu-id="0be4c-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="0be4c-104">Définit une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="0be4c-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0be4c-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="0be4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0be4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be4c-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0be4c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be4c-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0be4c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0be4c-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="0be4c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0be4c-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0be4c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be4c-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0be4c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0be4c-112">Identificateur unique de la matrice de constantes.</span><span class="sxs-lookup"><span data-stu-id="0be4c-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="0be4c-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0be4c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0be4c-114">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0be4c-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be4c-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be4c-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0be4c-116">Pointeur désignant une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="0be4c-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="0be4c-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0be4c-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be4c-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0be4c-118">Return value</span></span>

<span data-ttu-id="0be4c-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0be4c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0be4c-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0be4c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0be4c-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0be4c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be4c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0be4c-122">Requirements</span></span>



| <span data-ttu-id="0be4c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0be4c-123">Requirement</span></span> | <span data-ttu-id="0be4c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0be4c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be4c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0be4c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0be4c-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be4c-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0be4c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0be4c-127">Library</span></span><br/> | <dl> <span data-ttu-id="0be4c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0be4c-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0be4c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0be4c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be4c-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0be4c-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
