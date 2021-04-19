---
description: Clone un maillage à l’aide d’un déclarateur.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'ID3DXBaseMesh :: CloneMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545275"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="824cb-103">ID3DXBaseMesh :: CloneMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="824cb-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="824cb-104">Clone un maillage à l’aide d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="824cb-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="824cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="824cb-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="824cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="824cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="824cb-107">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="824cb-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824cb-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="824cb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="824cb-109">Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) spécifiant les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="824cb-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="824cb-110">*pDeclaration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="824cb-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824cb-111">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="824cb-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="824cb-112">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , qui spécifie le format de vertex pour les vertex dans le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="824cb-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="824cb-113">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="824cb-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824cb-114">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="824cb-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="824cb-115">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet périphérique associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="824cb-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="824cb-116">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="824cb-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="824cb-117">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="824cb-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="824cb-118">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage cloné.</span><span class="sxs-lookup"><span data-stu-id="824cb-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="824cb-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="824cb-119">Return value</span></span>

<span data-ttu-id="824cb-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="824cb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="824cb-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="824cb-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="824cb-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="824cb-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="824cb-123">Notes</span><span class="sxs-lookup"><span data-stu-id="824cb-123">Remarks</span></span>

<span data-ttu-id="824cb-124">**ID3DXBaseMesh :: CloneMesh** est utilisé pour reformater et modifier la disposition des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="824cb-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="824cb-125">Pour ce faire, créez un nouvel objet de maillage.</span><span class="sxs-lookup"><span data-stu-id="824cb-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="824cb-126">Par exemple, utilisez-le pour ajouter de l’espace pour les normales, les coordonnées de texture, les couleurs, les poids, etc. qui n’étaient pas présents avant.</span><span class="sxs-lookup"><span data-stu-id="824cb-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="824cb-127">[**ID3DXBaseMesh :: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) met à jour la déclaration de vertex avec des informations sémantiques différentes sans modifier la disposition de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="824cb-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="824cb-128">Cette méthode ne modifie pas le contenu de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="824cb-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="824cb-129">Par exemple, utilisez-le pour réétiqueter une coordonnée de texture 3D en tant que biperpendiculaire ou tangente, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="824cb-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="824cb-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="824cb-130">Requirements</span></span>



| <span data-ttu-id="824cb-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="824cb-131">Requirement</span></span> | <span data-ttu-id="824cb-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="824cb-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="824cb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="824cb-133">Header</span></span><br/>  | <dl> <span data-ttu-id="824cb-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="824cb-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="824cb-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="824cb-135">Library</span></span><br/> | <dl> <span data-ttu-id="824cb-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="824cb-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="824cb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="824cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824cb-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="824cb-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="824cb-139">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="824cb-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="824cb-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="824cb-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
