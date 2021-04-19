---
description: Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh :: GetAttributeTable, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527739"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="82a8e-103">ID3DX10Mesh :: GetAttributeTable, méthode</span><span class="sxs-lookup"><span data-stu-id="82a8e-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="82a8e-104">Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.</span><span class="sxs-lookup"><span data-stu-id="82a8e-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82a8e-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="82a8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82a8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a8e-107">*pAttribTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82a8e-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a8e-108">Type : **[ **\_ \_ plage d’attributs d3dx10**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="82a8e-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="82a8e-109">Pointeur vers un tableau de \_ structures de plage d’attributs d3dx10 \_ , représentant les entrées dans la table d’attributs du maillage.</span><span class="sxs-lookup"><span data-stu-id="82a8e-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="82a8e-110">Spécifiez **null** pour récupérer la valeur de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="82a8e-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="82a8e-111">*pAttribTableSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82a8e-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a8e-112">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="82a8e-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="82a8e-113">Pointeur vers le nombre d’entrées stockées dans pAttribTable ou une valeur à remplir avec le nombre d’entrées stockées dans la table d’attributs pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="82a8e-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a8e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82a8e-114">Return value</span></span>

<span data-ttu-id="82a8e-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82a8e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82a8e-116">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="82a8e-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82a8e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="82a8e-117">Remarks</span></span>

<span data-ttu-id="82a8e-118">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="82a8e-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="82a8e-119">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas d’identificateur d’attribut donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="82a8e-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a8e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82a8e-120">Requirements</span></span>



| <span data-ttu-id="82a8e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82a8e-121">Requirement</span></span> | <span data-ttu-id="82a8e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="82a8e-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82a8e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="82a8e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="82a8e-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="82a8e-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="82a8e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82a8e-125">Library</span></span><br/> | <dl> <span data-ttu-id="82a8e-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82a8e-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82a8e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82a8e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a8e-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="82a8e-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="82a8e-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="82a8e-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
