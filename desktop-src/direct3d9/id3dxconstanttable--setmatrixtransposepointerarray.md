---
description: 'ID3DXConstantTable :: SetMatrixTransposePointerArray, méthode-définit un tableau de pointeurs vers des matrices transposées.'
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'ID3DXConstantTable :: SetMatrixTransposePointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fefb5a0b62174499a4631f2fe8020c25a3a8efa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115037"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="17c87-103">ID3DXConstantTable :: SetMatrixTransposePointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="17c87-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="17c87-104">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="17c87-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17c87-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="17c87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17c87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c87-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17c87-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c87-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="17c87-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="17c87-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="17c87-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="17c87-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17c87-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c87-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="17c87-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="17c87-112">Identificateur unique du tableau de constantes de matrice.</span><span class="sxs-lookup"><span data-stu-id="17c87-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="17c87-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="17c87-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="17c87-114">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17c87-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c87-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="17c87-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="17c87-116">Tableau de pointeurs vers les matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="17c87-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="17c87-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="17c87-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="17c87-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17c87-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c87-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17c87-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17c87-120">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="17c87-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c87-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="17c87-121">Return value</span></span>

<span data-ttu-id="17c87-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17c87-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17c87-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17c87-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17c87-124">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17c87-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c87-125">Notes </span><span class="sxs-lookup"><span data-stu-id="17c87-125">Remarks</span></span>

<span data-ttu-id="17c87-126">Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="17c87-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c87-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17c87-127">Requirements</span></span>



| <span data-ttu-id="17c87-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17c87-128">Requirement</span></span> | <span data-ttu-id="17c87-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="17c87-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c87-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="17c87-130">Header</span></span><br/>  | <dl> <span data-ttu-id="17c87-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="17c87-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="17c87-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17c87-132">Library</span></span><br/> | <dl> <span data-ttu-id="17c87-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17c87-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="17c87-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17c87-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c87-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="17c87-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
