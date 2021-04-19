---
description: Clone un maillage à l’aide d’un code de format de vertex flexible.
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh :: CloneMeshFVF, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542154"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a><span data-ttu-id="74948-103">ID3DXBaseMesh :: CloneMeshFVF, méthode</span><span class="sxs-lookup"><span data-stu-id="74948-103">ID3DXBaseMesh::CloneMeshFVF method</span></span>

<span data-ttu-id="74948-104">Clone un maillage à l’aide d’un code de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="74948-104">Clones a mesh using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="74948-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74948-105">Syntax</span></span>


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="74948-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74948-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74948-107">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74948-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74948-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74948-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74948-109">Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) spécifiant les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="74948-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="74948-110">*Commission* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74948-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74948-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74948-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74948-112">Combinaison de codes de la Commission, qui spécifie le format de vertex pour les vertex dans le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="74948-112">Combination of FVF codes, which specifies the vertex format for the vertices in the output mesh.</span></span> <span data-ttu-id="74948-113">Pour obtenir les valeurs des codes, consultez [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="74948-113">For the values of the codes, see [D3DFVF](d3dfvf.md).</span></span>

</dd> <dt>

<span data-ttu-id="74948-114">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74948-114">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74948-115">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="74948-115">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="74948-116">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) représentant l’objet périphérique associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="74948-116">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="74948-117">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="74948-117">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="74948-118">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="74948-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="74948-119">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage cloné.</span><span class="sxs-lookup"><span data-stu-id="74948-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74948-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74948-120">Return value</span></span>

<span data-ttu-id="74948-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74948-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74948-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74948-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74948-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="74948-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="74948-124">Notes</span><span class="sxs-lookup"><span data-stu-id="74948-124">Remarks</span></span>

<span data-ttu-id="74948-125">**ID3DXBaseMesh :: CloneMeshFVF** est utilisé pour reformater et modifier la disposition des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="74948-125">**ID3DXBaseMesh::CloneMeshFVF** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="74948-126">Pour ce faire, créez un nouvel objet de maillage.</span><span class="sxs-lookup"><span data-stu-id="74948-126">This is done by creating a new mesh object.</span></span> <span data-ttu-id="74948-127">Par exemple, utilisez-le pour ajouter de l’espace pour les normales, les coordonnées de texture, les couleurs, les pondérations, etc. qui n’étaient pas déjà présentes.</span><span class="sxs-lookup"><span data-stu-id="74948-127">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="74948-128">[**ID3DXBaseMesh :: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) met à jour la déclaration de vertex avec des informations sémantiques différentes sans modifier la disposition de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="74948-128">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="74948-129">Cette méthode ne modifie pas le contenu de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="74948-129">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="74948-130">Par exemple, utilisez-le pour réétiqueter une coordonnée de texture 3D en tant que biperpendiculaire ou tangente, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="74948-130">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="74948-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74948-131">Requirements</span></span>



| <span data-ttu-id="74948-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74948-132">Requirement</span></span> | <span data-ttu-id="74948-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="74948-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74948-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="74948-134">Header</span></span><br/>  | <dl> <span data-ttu-id="74948-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="74948-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74948-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="74948-136">Library</span></span><br/> | <dl> <span data-ttu-id="74948-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74948-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74948-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74948-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74948-139">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="74948-139">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="74948-140">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="74948-140">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
