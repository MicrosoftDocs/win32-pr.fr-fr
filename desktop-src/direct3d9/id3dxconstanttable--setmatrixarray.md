---
description: 'ID3DXConstantTable :: SetMatrixArray, méthode-définit un tableau de matrices nontransposed.'
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: 'ID3DXConstantTable :: SetMatrixArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02e115cf4526ab065d2613636427059826f450f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115097"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="99c31-103">ID3DXConstantTable :: SetMatrixArray, méthode</span><span class="sxs-lookup"><span data-stu-id="99c31-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="99c31-104">Définit un tableau de matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="99c31-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99c31-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="99c31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99c31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c31-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99c31-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c31-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="99c31-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="99c31-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="99c31-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="99c31-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99c31-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c31-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="99c31-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="99c31-112">Identificateur unique du tableau de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="99c31-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="99c31-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="99c31-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="99c31-114">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99c31-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c31-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="99c31-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99c31-116">Tableau de matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="99c31-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="99c31-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="99c31-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="99c31-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99c31-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c31-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99c31-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99c31-120">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="99c31-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c31-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="99c31-121">Return value</span></span>

<span data-ttu-id="99c31-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99c31-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99c31-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99c31-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99c31-124">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="99c31-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c31-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99c31-125">Requirements</span></span>



| <span data-ttu-id="99c31-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99c31-126">Requirement</span></span> | <span data-ttu-id="99c31-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="99c31-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c31-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="99c31-128">Header</span></span><br/>  | <dl> <span data-ttu-id="99c31-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c31-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="99c31-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99c31-130">Library</span></span><br/> | <dl> <span data-ttu-id="99c31-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99c31-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="99c31-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99c31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c31-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="99c31-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
