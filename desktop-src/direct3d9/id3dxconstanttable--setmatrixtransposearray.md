---
description: 'ID3DXConstantTable :: SetMatrixTransposeArray, méthode-définit un tableau de matrices transposées.'
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: 'ID3DXConstantTable :: SetMatrixTransposeArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0118c888adc52671a943b7b159bae80deca26a1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115047"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="2b210-103">ID3DXConstantTable :: SetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="2b210-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="2b210-104">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="2b210-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b210-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b210-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="2b210-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b210-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b210-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b210-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2b210-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2b210-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="2b210-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2b210-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b210-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b210-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2b210-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2b210-112">Identificateur unique du tableau de constantes de matrice.</span><span class="sxs-lookup"><span data-stu-id="2b210-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="2b210-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2b210-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b210-114">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b210-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b210-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b210-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2b210-116">Tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="2b210-116">Array of transposed matrices.</span></span> <span data-ttu-id="2b210-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2b210-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b210-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b210-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b210-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b210-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b210-120">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2b210-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b210-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b210-121">Return value</span></span>

<span data-ttu-id="2b210-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b210-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b210-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b210-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b210-124">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2b210-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b210-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b210-125">Requirements</span></span>



| <span data-ttu-id="2b210-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b210-126">Requirement</span></span> | <span data-ttu-id="2b210-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b210-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b210-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b210-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2b210-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b210-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2b210-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b210-130">Library</span></span><br/> | <dl> <span data-ttu-id="2b210-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b210-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2b210-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b210-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b210-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2b210-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
