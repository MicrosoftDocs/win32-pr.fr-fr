---
description: Les applications utilisent les méthodes de l’interface ID3DXBaseMesh pour manipuler et interroger les objets de maillage et de maillage progressif.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interface ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322989"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="cb8fa-103">Interface ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="cb8fa-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="cb8fa-104">Les applications utilisent les méthodes de l’interface **ID3DXBaseMesh** pour manipuler et interroger les objets de maillage et de maillage progressif.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="cb8fa-105">Membres</span><span class="sxs-lookup"><span data-stu-id="cb8fa-105">Members</span></span>

<span data-ttu-id="cb8fa-106">L’interface **ID3DXBaseMesh** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cb8fa-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cb8fa-107">**ID3DXBaseMesh** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb8fa-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="cb8fa-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb8fa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cb8fa-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb8fa-109">Methods</span></span>

<span data-ttu-id="cb8fa-110">L’interface **ID3DXBaseMesh** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="cb8fa-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb8fa-111">Method</span></span>                                                                            | <span data-ttu-id="cb8fa-112">Description</span><span class="sxs-lookup"><span data-stu-id="cb8fa-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb8fa-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="cb8fa-114">Clone un maillage à l’aide d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="cb8fa-115">**CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="cb8fa-116">Clone un maillage à l’aide d’un code de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="cb8fa-117">**ConvertAdjacencyToPointReps**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="cb8fa-118">Convertit les informations d’adjacence de maillage en un tableau de représentants de point.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="cb8fa-119">**ConvertPointRepsToAdjacency**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="cb8fa-120">Convertit les données représentatives de point en informations d’adjacence de maillage.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="cb8fa-121">**DrawSubset**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="cb8fa-122">Dessine un sous-ensemble d’une maille.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="cb8fa-123">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="cb8fa-124">Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="cb8fa-125">**GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="cb8fa-126">Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cb8fa-127">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="cb8fa-128">Récupère une déclaration décrivant les vertex de la maille.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="cb8fa-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="cb8fa-130">Récupère l’appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="cb8fa-131">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="cb8fa-132">Obtient la valeur de vertex de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="cb8fa-133">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="cb8fa-134">Récupère les données dans une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="cb8fa-135">**GetNumBytesPerVertex**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="cb8fa-136">Obtient le nombre d’octets par vertex.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="cb8fa-137">**GetNumFaces**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="cb8fa-138">Récupère le nombre de faces dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="cb8fa-139">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="cb8fa-140">Récupère le nombre de vertex dans la maille.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="cb8fa-141">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="cb8fa-142">Récupère les options de maillage activées pour ce maillage au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="cb8fa-143">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="cb8fa-144">Récupère la mémoire tampon de vertex associée à la maille.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="cb8fa-145">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="cb8fa-146">Verrouille un tampon d’index et obtient un pointeur vers la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="cb8fa-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="cb8fa-148">Verrouille une mémoire tampon de vertex et obtient un pointeur vers la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="cb8fa-149">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="cb8fa-150">Déverrouille un tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="cb8fa-151">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="cb8fa-152">Déverrouille une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="cb8fa-153">**UpdateSemantics**</span><span class="sxs-lookup"><span data-stu-id="cb8fa-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="cb8fa-154">Cette méthode permet à l’utilisateur de modifier la déclaration de maillage sans modifier la disposition des données de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="cb8fa-155">L’appel est valide uniquement si l’ancien et le nouveau format de déclaration ont la même taille de vertex.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb8fa-156">Notes</span><span class="sxs-lookup"><span data-stu-id="cb8fa-156">Remarks</span></span>

<span data-ttu-id="cb8fa-157">Un maillage est un objet constitué d’un ensemble de visages polygones.</span><span class="sxs-lookup"><span data-stu-id="cb8fa-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="cb8fa-158">Une maille définit un ensemble de vertex et un ensemble de faces (les faces sont définies en termes de vertex et de normales de la maille).</span><span class="sxs-lookup"><span data-stu-id="cb8fa-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="cb8fa-159">Le type LPD3DXBASEMESH est défini comme un pointeur vers l’interface **ID3DXBaseMesh** .</span><span class="sxs-lookup"><span data-stu-id="cb8fa-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="cb8fa-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb8fa-160">Requirements</span></span>



| <span data-ttu-id="cb8fa-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb8fa-161">Requirement</span></span> | <span data-ttu-id="cb8fa-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb8fa-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8fa-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb8fa-163">Header</span></span><br/>  | <dl> <span data-ttu-id="cb8fa-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb8fa-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cb8fa-165">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb8fa-165">Library</span></span><br/> | <dl> <span data-ttu-id="cb8fa-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb8fa-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb8fa-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb8fa-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb8fa-168">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cb8fa-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
