---
description: Obtient une constante d’un tableau de constantes. Un tableau est constitué d’éléments.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable :: GetConstantElement, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531545"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="b3c78-104">ID3DXConstantTable :: GetConstantElement, méthode</span><span class="sxs-lookup"><span data-stu-id="b3c78-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="b3c78-105">Obtient une constante d’un tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="b3c78-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="b3c78-106">Un tableau est constitué d’éléments.</span><span class="sxs-lookup"><span data-stu-id="b3c78-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c78-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3c78-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="b3c78-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c78-109">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c78-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c78-110">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c78-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b3c78-111">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="b3c78-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="b3c78-112">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="b3c78-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3c78-113">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c78-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c78-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c78-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3c78-115">Index de base zéro de l’élément dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b3c78-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c78-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3c78-116">Return value</span></span>

<span data-ttu-id="b3c78-117">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c78-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b3c78-118">Retourne un identificateur unique à la constante d’élément.</span><span class="sxs-lookup"><span data-stu-id="b3c78-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c78-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b3c78-119">Remarks</span></span>

<span data-ttu-id="b3c78-120">Pour obtenir une constante qui ne fait pas partie d’un tableau, utilisez [**ID3DXConstantTable :: GetConstant**](id3dxconstanttable--getconstant.md) ou [**ID3DXConstantTable :: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="b3c78-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c78-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c78-121">Requirements</span></span>



| <span data-ttu-id="b3c78-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3c78-122">Requirement</span></span> | <span data-ttu-id="b3c78-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c78-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c78-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3c78-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b3c78-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c78-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b3c78-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3c78-126">Library</span></span><br/> | <dl> <span data-ttu-id="b3c78-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c78-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b3c78-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c78-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c78-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b3c78-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
