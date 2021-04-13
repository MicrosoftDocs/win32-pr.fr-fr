---
description: Crée un maillage de correctifs avec la déclaration de vertex spécifiée.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh :: CloneMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322706"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="3dc79-103">ID3DXPatchMesh :: CloneMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="3dc79-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="3dc79-104">Crée un maillage de correctifs avec la déclaration de vertex spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3dc79-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc79-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dc79-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="3dc79-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dc79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dc79-107">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dc79-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc79-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3dc79-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3dc79-109">Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) qui spécifient des options de création pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="3dc79-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3dc79-110">*pDecl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dc79-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc79-111">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="3dc79-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="3dc79-112">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) qui spécifient le format de vertex pour les vertex dans le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="3dc79-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3dc79-113">*pMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3dc79-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc79-114">Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3dc79-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="3dc79-115">Adresse d’un pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) qui représente le maillage cloné.</span><span class="sxs-lookup"><span data-stu-id="3dc79-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dc79-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3dc79-116">Return value</span></span>

<span data-ttu-id="3dc79-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3dc79-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3dc79-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3dc79-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3dc79-119">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3dc79-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc79-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3dc79-120">Remarks</span></span>

<span data-ttu-id="3dc79-121">**CloneMesh** convertit la mémoire tampon de vertex en la nouvelle déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="3dc79-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="3dc79-122">Les entrées de la déclaration de vertex qui sont nouvelles dans le maillage d’origine ont la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="3dc79-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="3dc79-123">Si le maillage actuel a une contiguïté, le nouveau maillage aura également une contiguïté.</span><span class="sxs-lookup"><span data-stu-id="3dc79-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc79-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dc79-124">Requirements</span></span>



| <span data-ttu-id="3dc79-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dc79-125">Requirement</span></span> | <span data-ttu-id="3dc79-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dc79-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc79-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3dc79-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3dc79-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dc79-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3dc79-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3dc79-129">Library</span></span><br/> | <dl> <span data-ttu-id="3dc79-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dc79-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3dc79-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dc79-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc79-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="3dc79-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
