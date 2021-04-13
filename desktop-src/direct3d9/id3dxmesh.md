---
description: Les applications utilisent les méthodes de l’interface ID3DXMesh pour manipuler les objets de maillage.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interface ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323262"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="ddd1f-103">Interface ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="ddd1f-103">ID3DXMesh interface</span></span>

<span data-ttu-id="ddd1f-104">Les applications utilisent les méthodes de l’interface ID3DXMesh pour manipuler les objets de maillage.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="ddd1f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ddd1f-105">Members</span></span>

<span data-ttu-id="ddd1f-106">L’interface **ID3DXMesh** hérite de [**ID3DXBaseMesh**](id3dxbasemesh.md).</span><span class="sxs-lookup"><span data-stu-id="ddd1f-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="ddd1f-107">**ID3DXMesh** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ddd1f-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="ddd1f-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ddd1f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ddd1f-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ddd1f-109">Methods</span></span>

<span data-ttu-id="ddd1f-110">L’interface **ID3DXMesh** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="ddd1f-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ddd1f-111">Method</span></span>                                                            | <span data-ttu-id="ddd1f-112">Description</span><span class="sxs-lookup"><span data-stu-id="ddd1f-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddd1f-113">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="ddd1f-114">Verrouille la mémoire tampon de maillage qui contient les données d’attribut de maillage et retourne un pointeur vers celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="ddd1f-115">**Optimiser**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="ddd1f-116">Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="ddd1f-117">**OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="ddd1f-118">Génère un maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="ddd1f-119">Cette méthode réorganise la maille existante.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="ddd1f-120">**SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="ddd1f-121">Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="ddd1f-122">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="ddd1f-123">Déverrouille une mémoire tampon d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="ddd1f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ddd1f-124">Remarks</span></span>

<span data-ttu-id="ddd1f-125">Pour obtenir l’interface **ID3DXMesh** , appelez la fonction [**D3DXCreateMesh**](d3dxcreatemesh.md) ou [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="ddd1f-126">Cette interface hérite des fonctionnalités supplémentaires de l’interface [**ID3DXBaseMesh**](id3dxbasemesh.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="ddd1f-127">Le type LPD3DXMESH est défini comme un pointeur vers l’interface **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="ddd1f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddd1f-128">Requirements</span></span>



| <span data-ttu-id="ddd1f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddd1f-129">Requirement</span></span> | <span data-ttu-id="ddd1f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddd1f-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd1f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddd1f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ddd1f-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd1f-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ddd1f-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ddd1f-133">Library</span></span><br/> | <dl> <span data-ttu-id="ddd1f-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddd1f-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ddd1f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddd1f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd1f-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="ddd1f-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ddd1f-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ddd1f-138">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="ddd1f-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




