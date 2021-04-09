---
description: Cette interface est implémentée par l’application pour allouer ou libérer des objets conteneurs de frame et de maillage. Les méthodes de ce sont appelées lors du chargement et de la destruction des hiérarchies de frame.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interface ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043174"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="6b583-104">Interface ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="6b583-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="6b583-105">Cette interface est implémentée par l’application pour allouer ou libérer des objets conteneurs de frame et de maillage.</span><span class="sxs-lookup"><span data-stu-id="6b583-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="6b583-106">Les méthodes de ce sont appelées lors du chargement et de la destruction des hiérarchies de frame.</span><span class="sxs-lookup"><span data-stu-id="6b583-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="6b583-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6b583-107">Members</span></span>

<span data-ttu-id="6b583-108">L’interface **ID3DXAllocateHierarchy** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6b583-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6b583-109">**ID3DXAllocateHierarchy** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6b583-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="6b583-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6b583-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6b583-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6b583-111">Methods</span></span>

<span data-ttu-id="6b583-112">L’interface **ID3DXAllocateHierarchy** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6b583-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="6b583-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="6b583-113">Method</span></span>                                                                       | <span data-ttu-id="6b583-114">Description</span><span class="sxs-lookup"><span data-stu-id="6b583-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="6b583-115">**CreateFrame**</span><span class="sxs-lookup"><span data-stu-id="6b583-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="6b583-116">Demande l’allocation d’un objet Frame.</span><span class="sxs-lookup"><span data-stu-id="6b583-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="6b583-117">**CreateMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="6b583-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="6b583-118">Demande l’allocation d’un objet conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="6b583-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="6b583-119">**DestroyFrame**</span><span class="sxs-lookup"><span data-stu-id="6b583-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="6b583-120">Demande la désallocation d’un objet Frame.</span><span class="sxs-lookup"><span data-stu-id="6b583-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="6b583-121">**DestroyMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="6b583-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="6b583-122">Demande la désallocation d’un objet conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="6b583-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b583-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6b583-123">Remarks</span></span>

<span data-ttu-id="6b583-124">Le type LPD3DXALLOCATEHIERARCHY est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="6b583-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="6b583-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b583-125">Requirements</span></span>



| <span data-ttu-id="6b583-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b583-126">Requirement</span></span> | <span data-ttu-id="6b583-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b583-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b583-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b583-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6b583-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b583-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6b583-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b583-130">Library</span></span><br/> | <dl> <span data-ttu-id="6b583-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b583-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b583-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b583-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b583-133">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6b583-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
