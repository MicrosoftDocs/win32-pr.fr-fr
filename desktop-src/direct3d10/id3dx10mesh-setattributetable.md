---
description: Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'ID3DX10Mesh :: SetAttributeTable, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211857"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="eb662-103">ID3DX10Mesh :: SetAttributeTable, méthode</span><span class="sxs-lookup"><span data-stu-id="eb662-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="eb662-104">Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.</span><span class="sxs-lookup"><span data-stu-id="eb662-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb662-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb662-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="eb662-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb662-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb662-107">*pAttribTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb662-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb662-108">Type : **const [**d3dx10 \_ attribut \_ Range**](d3dx10-attribute-range.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb662-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="eb662-109">Pointeur vers un tableau de \_ structures de plage d’attributs d3dx10 \_ , représentant les entrées de la table d’attributs de maillage.</span><span class="sxs-lookup"><span data-stu-id="eb662-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="eb662-110">*cAttribTableSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb662-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb662-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb662-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb662-112">Nombre d’attributs dans la table d’attributs du maillage.</span><span class="sxs-lookup"><span data-stu-id="eb662-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb662-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb662-113">Return value</span></span>

<span data-ttu-id="eb662-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb662-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb662-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eb662-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb662-116">Notes</span><span class="sxs-lookup"><span data-stu-id="eb662-116">Remarks</span></span>

<span data-ttu-id="eb662-117">Si une application effectue le suivi des informations dans une table d’attributs et réorganise la table suite à des modifications apportées aux attributs ou aux visages, cette méthode permet à l’application de mettre à jour les tables d’attributs au lieu d’appeler ID3DX10Mesh :: optimize.</span><span class="sxs-lookup"><span data-stu-id="eb662-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb662-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb662-118">Requirements</span></span>



| <span data-ttu-id="eb662-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb662-119">Requirement</span></span> | <span data-ttu-id="eb662-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb662-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb662-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb662-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eb662-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb662-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb662-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb662-123">Library</span></span><br/> | <dl> <span data-ttu-id="eb662-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb662-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb662-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb662-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb662-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="eb662-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="eb662-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="eb662-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
