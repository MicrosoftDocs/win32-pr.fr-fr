---
description: Cette interface encapsule la fonctionnalité de maillage des correctifs.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interface ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323061"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="ff3c0-103">Interface ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ff3c0-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="ff3c0-104">Cette interface encapsule la fonctionnalité de maillage des correctifs.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="ff3c0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ff3c0-105">Members</span></span>

<span data-ttu-id="ff3c0-106">L’interface **ID3DXPatchMesh** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ff3c0-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ff3c0-107">**ID3DXPatchMesh** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ff3c0-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="ff3c0-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ff3c0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ff3c0-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ff3c0-109">Methods</span></span>

<span data-ttu-id="ff3c0-110">L’interface **ID3DXPatchMesh** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="ff3c0-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ff3c0-111">Method</span></span>                                                                           | <span data-ttu-id="ff3c0-112">Description</span><span class="sxs-lookup"><span data-stu-id="ff3c0-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff3c0-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="ff3c0-114">Crée un maillage de correctifs avec la déclaration de vertex spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="ff3c0-115">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="ff3c0-116">Générez une liste de bords de maillage et les correctifs qui partagent chaque périphérie.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="ff3c0-117">**GetControlVerticesPerPatch**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="ff3c0-118">Obtient le nombre de vertex de contrôle par correctif.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="ff3c0-119">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="ff3c0-120">Obtient la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="ff3c0-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="ff3c0-122">Obtient l’appareil qui a créé le maillage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="ff3c0-123">**GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="ff3c0-124">Obtient les paramètres de déplacement de la géométrie de maillage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="ff3c0-125">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="ff3c0-126">Obtient la mémoire tampon d’index de maillage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="ff3c0-127">**GetNumPatches**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="ff3c0-128">Obtient le nombre de correctifs dans la maille.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="ff3c0-129">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="ff3c0-130">Obtient le nombre de vertex dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="ff3c0-131">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="ff3c0-132">Obtient le type de correctif.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="ff3c0-133">**GetPatchInfo**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="ff3c0-134">Obtient les attributs du correctif.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="ff3c0-135">**GetTessSize**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="ff3c0-136">Obtient la taille du maillage fractionné, en fonction d’un niveau de pavage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="ff3c0-137">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="ff3c0-138">Obtient la mémoire tampon de vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="ff3c0-139">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="ff3c0-140">Verrouille la mémoire tampon d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="ff3c0-141">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="ff3c0-142">Verrouillez le tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="ff3c0-143">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="ff3c0-144">Verrouille la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="ff3c0-145">**Optimiser**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="ff3c0-146">Optimise le maillage des correctifs pour une polygonalisation efficace.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="ff3c0-147">**SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="ff3c0-148">Définit les paramètres de déplacement de la géométrie du maillage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="ff3c0-149">**Paver**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="ff3c0-150">Effectue un pavage uniforme basé sur le niveau de pavage.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="ff3c0-151">**TessellateAdaptive**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="ff3c0-152">Effectue un pavage adaptatif basé sur le critère de pavage adaptative basé sur z.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="ff3c0-153">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="ff3c0-154">Déverrouillez la mémoire tampon d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="ff3c0-155">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="ff3c0-156">Déverrouillez la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="ff3c0-157">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff3c0-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="ff3c0-158">Déverrouillez la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ff3c0-159">Notes</span><span class="sxs-lookup"><span data-stu-id="ff3c0-159">Remarks</span></span>

<span data-ttu-id="ff3c0-160">Une maille de correctif est une maille qui se compose d’une série de correctifs.</span><span class="sxs-lookup"><span data-stu-id="ff3c0-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="ff3c0-161">Pour obtenir l’interface **ID3DXPatchMesh** , appelez la fonction [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="ff3c0-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="ff3c0-162">Le type LPD3DXPATCHMESH est défini comme un pointeur vers l’interface **ID3DXPatchMesh** , comme suit :</span><span class="sxs-lookup"><span data-stu-id="ff3c0-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="ff3c0-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff3c0-163">Requirements</span></span>



| <span data-ttu-id="ff3c0-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff3c0-164">Requirement</span></span> | <span data-ttu-id="ff3c0-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff3c0-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3c0-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff3c0-166">Header</span></span><br/>  | <dl> <span data-ttu-id="ff3c0-167"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff3c0-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ff3c0-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff3c0-168">Library</span></span><br/> | <dl> <span data-ttu-id="ff3c0-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff3c0-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff3c0-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff3c0-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3c0-171">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ff3c0-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ff3c0-172">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="ff3c0-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
