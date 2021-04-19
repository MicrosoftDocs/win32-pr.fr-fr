---
description: Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'ID3DXBaseMesh :: GetAttributeTable, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70c93c8f477655200418793f53706731b42a47ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523200"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="21768-103">ID3DXBaseMesh :: GetAttributeTable, méthode</span><span class="sxs-lookup"><span data-stu-id="21768-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="21768-104">Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.</span><span class="sxs-lookup"><span data-stu-id="21768-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="21768-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21768-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="21768-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21768-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21768-107">*pAttribTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="21768-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21768-108">Type : **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="21768-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="21768-109">Pointeur vers un tableau de structures [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) représentant les entrées dans la table d’attributs du maillage.</span><span class="sxs-lookup"><span data-stu-id="21768-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="21768-110">Spécifiez **null** pour récupérer la valeur de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="21768-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="21768-111">*pAttribTableSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="21768-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21768-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21768-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21768-113">Pointeur vers le nombre d’entrées stockées dans pAttribTable ou une valeur à remplir avec le nombre d’entrées stockées dans la table d’attributs pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="21768-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21768-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21768-114">Return value</span></span>

<span data-ttu-id="21768-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21768-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21768-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21768-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21768-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="21768-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21768-118">Notes</span><span class="sxs-lookup"><span data-stu-id="21768-118">Remarks</span></span>

<span data-ttu-id="21768-119">Une table d’attributs est créée par [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) et en passant D3DXMESHOPT \_ ATTRSORT pour le paramètre flags.</span><span class="sxs-lookup"><span data-stu-id="21768-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="21768-120">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="21768-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="21768-121">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas d’identificateur d’attribut donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="21768-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="21768-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21768-122">Requirements</span></span>



| <span data-ttu-id="21768-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21768-123">Requirement</span></span> | <span data-ttu-id="21768-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="21768-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21768-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="21768-125">Header</span></span><br/>  | <dl> <span data-ttu-id="21768-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="21768-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="21768-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21768-127">Library</span></span><br/> | <dl> <span data-ttu-id="21768-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21768-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21768-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21768-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21768-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="21768-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
