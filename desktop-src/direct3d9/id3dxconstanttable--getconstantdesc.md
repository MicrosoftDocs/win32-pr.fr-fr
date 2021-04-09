---
description: Obtient un pointeur vers un tableau de descriptions constantes dans la table constante.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable :: GetConstantDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953872"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="b8368-103">ID3DXConstantTable :: GetConstantDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="b8368-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="b8368-104">Obtient un pointeur vers un tableau de descriptions constantes dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="b8368-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8368-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8368-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="b8368-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8368-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8368-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8368-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b8368-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b8368-109">Identificateur unique d’une constante.</span><span class="sxs-lookup"><span data-stu-id="b8368-109">Unique identifier to a constant.</span></span> <span data-ttu-id="b8368-110">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8368-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8368-111">*pDesc* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b8368-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8368-112">Type : **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8368-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="b8368-113">Retourne un pointeur vers un tableau de descriptions.</span><span class="sxs-lookup"><span data-stu-id="b8368-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="b8368-114">Consultez [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b8368-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8368-115">*pCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b8368-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8368-116">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8368-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b8368-117">L’entrée fournie doit correspondre à la taille maximale du tableau.</span><span class="sxs-lookup"><span data-stu-id="b8368-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="b8368-118">La sortie est le nombre d’éléments qui sont remplis dans le tableau lorsque la fonction retourne.</span><span class="sxs-lookup"><span data-stu-id="b8368-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8368-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8368-119">Return value</span></span>

<span data-ttu-id="b8368-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8368-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8368-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8368-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8368-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="b8368-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8368-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b8368-123">Remarks</span></span>

<span data-ttu-id="b8368-124">**ID3DXConstantTable :: GetConstantDesc** retourne parfois une [**\_ desc D3DXCONSTANT**](d3dxconstant-desc.md) avec un \_ nombre de registres égal à 0.</span><span class="sxs-lookup"><span data-stu-id="b8368-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="b8368-125">Cela se produit si une constante apparaît dans plusieurs registres, \_ mais n’a pas d’espace dans ce jeu de registres alloué.</span><span class="sxs-lookup"><span data-stu-id="b8368-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="b8368-126">Comme un échantillonneur peut apparaître plusieurs fois dans une table constante, cette méthode peut retourner un tableau de descriptions, chacune avec un index de Registre différent.</span><span class="sxs-lookup"><span data-stu-id="b8368-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8368-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8368-127">Requirements</span></span>



| <span data-ttu-id="b8368-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8368-128">Requirement</span></span> | <span data-ttu-id="b8368-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8368-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8368-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8368-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b8368-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8368-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b8368-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8368-132">Library</span></span><br/> | <dl> <span data-ttu-id="b8368-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8368-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8368-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8368-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8368-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b8368-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="b8368-136">**ID3DXConstantTable::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="b8368-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
