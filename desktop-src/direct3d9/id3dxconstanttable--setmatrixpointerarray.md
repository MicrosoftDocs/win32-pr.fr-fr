---
description: 'ID3DXConstantTable :: SetMatrixPointerArray, méthode-définit un tableau de pointeurs vers des matrices nontransposed.'
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'ID3DXConstantTable :: SetMatrixPointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd9505f82674efc822d4921d7116c8eab17198c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115067"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="fc6b6-103">ID3DXConstantTable :: SetMatrixPointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="fc6b6-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="fc6b6-104">Définit un tableau de pointeurs sur les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc6b6-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="fc6b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc6b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6b6-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc6b6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6b6-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fc6b6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fc6b6-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="fc6b6-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc6b6-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6b6-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fc6b6-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fc6b6-112">Identificateur unique d’un tableau de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="fc6b6-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fc6b6-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc6b6-114">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc6b6-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6b6-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="fc6b6-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="fc6b6-116">Tableau de pointeurs vers les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="fc6b6-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fc6b6-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc6b6-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc6b6-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6b6-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc6b6-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc6b6-120">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc6b6-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc6b6-121">Return value</span></span>

<span data-ttu-id="fc6b6-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc6b6-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc6b6-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc6b6-124">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6b6-125">Notes </span><span class="sxs-lookup"><span data-stu-id="fc6b6-125">Remarks</span></span>

<span data-ttu-id="fc6b6-126">Une matrice nontransposed contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="fc6b6-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6b6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc6b6-127">Requirements</span></span>



| <span data-ttu-id="fc6b6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc6b6-128">Requirement</span></span> | <span data-ttu-id="fc6b6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc6b6-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6b6-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc6b6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fc6b6-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc6b6-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fc6b6-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc6b6-132">Library</span></span><br/> | <dl> <span data-ttu-id="fc6b6-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc6b6-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fc6b6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc6b6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6b6-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fc6b6-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
