---
description: Définit un tableau de pointeurs sur les matrices nontransposed.
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
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538517"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="7e43b-103">ID3DXConstantTable :: SetMatrixPointerArray, méthode</span><span class="sxs-lookup"><span data-stu-id="7e43b-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="7e43b-104">Définit un tableau de pointeurs sur les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7e43b-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e43b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e43b-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="7e43b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e43b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e43b-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e43b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e43b-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7e43b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7e43b-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="7e43b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7e43b-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e43b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e43b-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7e43b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7e43b-112">Identificateur unique d’un tableau de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="7e43b-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="7e43b-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7e43b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e43b-114">*ppMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e43b-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e43b-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="7e43b-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="7e43b-116">Tableau de pointeurs vers les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7e43b-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="7e43b-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7e43b-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e43b-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e43b-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e43b-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e43b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e43b-120">Nombre de matrices dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7e43b-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e43b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e43b-121">Return value</span></span>

<span data-ttu-id="7e43b-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e43b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e43b-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e43b-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e43b-124">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7e43b-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e43b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7e43b-125">Remarks</span></span>

<span data-ttu-id="7e43b-126">Une matrice nontransposed contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="7e43b-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e43b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e43b-127">Requirements</span></span>



| <span data-ttu-id="7e43b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e43b-128">Requirement</span></span> | <span data-ttu-id="7e43b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e43b-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e43b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e43b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7e43b-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e43b-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7e43b-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e43b-132">Library</span></span><br/> | <dl> <span data-ttu-id="7e43b-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e43b-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7e43b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e43b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e43b-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7e43b-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
