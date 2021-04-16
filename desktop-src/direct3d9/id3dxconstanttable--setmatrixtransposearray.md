---
description: Définit un tableau de matrices transposées.
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
ms.openlocfilehash: 69755ed973a8c412373287f128642b78ea2ad346
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530945"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="f4639-103">ID3DXConstantTable :: SetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="f4639-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="f4639-104">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="f4639-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4639-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4639-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="f4639-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4639-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4639-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4639-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4639-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f4639-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f4639-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="f4639-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f4639-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4639-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4639-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f4639-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f4639-112">Identificateur unique du tableau de constantes de matrice.</span><span class="sxs-lookup"><span data-stu-id="f4639-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="f4639-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f4639-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4639-114">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4639-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4639-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4639-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f4639-116">Tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="f4639-116">Array of transposed matrices.</span></span> <span data-ttu-id="f4639-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="f4639-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4639-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4639-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4639-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4639-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4639-120">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f4639-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4639-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4639-121">Return value</span></span>

<span data-ttu-id="f4639-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4639-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4639-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4639-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f4639-124">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f4639-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4639-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4639-125">Requirements</span></span>



| <span data-ttu-id="f4639-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4639-126">Requirement</span></span> | <span data-ttu-id="f4639-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4639-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4639-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4639-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f4639-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4639-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f4639-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4639-130">Library</span></span><br/> | <dl> <span data-ttu-id="f4639-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4639-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f4639-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4639-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4639-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f4639-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
