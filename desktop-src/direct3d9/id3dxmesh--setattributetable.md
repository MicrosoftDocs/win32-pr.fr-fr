---
description: Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'ID3DXMesh :: SetAttributeTable, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543022"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="ac7e6-103">ID3DXMesh :: SetAttributeTable, méthode</span><span class="sxs-lookup"><span data-stu-id="ac7e6-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="ac7e6-104">Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.</span><span class="sxs-lookup"><span data-stu-id="ac7e6-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac7e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac7e6-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="ac7e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac7e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac7e6-107">*pAttribTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac7e6-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e6-108">Type : **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac7e6-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="ac7e6-109">Pointeur vers un tableau de structures [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) représentant les entrées de la table d’attributs de maillage.</span><span class="sxs-lookup"><span data-stu-id="ac7e6-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e6-110">*cAttribTableSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac7e6-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e6-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac7e6-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac7e6-112">Nombre d’attributs dans la table d’attributs du maillage.</span><span class="sxs-lookup"><span data-stu-id="ac7e6-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac7e6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac7e6-113">Return value</span></span>

<span data-ttu-id="ac7e6-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac7e6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac7e6-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac7e6-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac7e6-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ac7e6-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac7e6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ac7e6-117">Remarks</span></span>

<span data-ttu-id="ac7e6-118">Si une application effectue le suivi des informations dans une table d’attributs et réorganise la table suite à des modifications apportées aux attributs ou aux visages, cette méthode permet à l’application de mettre à jour les tables d’attributs au lieu d’appeler [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="ac7e6-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7e6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac7e6-119">Requirements</span></span>



| <span data-ttu-id="ac7e6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac7e6-120">Requirement</span></span> | <span data-ttu-id="ac7e6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac7e6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7e6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac7e6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ac7e6-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7e6-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ac7e6-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac7e6-124">Library</span></span><br/> | <dl> <span data-ttu-id="ac7e6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac7e6-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac7e6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac7e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7e6-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="ac7e6-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="ac7e6-128">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ac7e6-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="ac7e6-129">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ac7e6-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
