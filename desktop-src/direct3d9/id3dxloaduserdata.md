---
description: Cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interface ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538497"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="01471-103">Interface ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="01471-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="01471-104">Cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x.</span><span class="sxs-lookup"><span data-stu-id="01471-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="01471-105">Une instance de cette interface est passée à [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), et D3DX appelle la méthode appropriée sur cette interface chaque fois que les données appropriées sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="01471-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="01471-106">Par exemple, pour chaque objet frame du fichier. x, [**ID3DXLoadUserData :: LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) est appelé et reçoit les données enfants.</span><span class="sxs-lookup"><span data-stu-id="01471-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="01471-107">Membres</span><span class="sxs-lookup"><span data-stu-id="01471-107">Members</span></span>

<span data-ttu-id="01471-108">L’interface **ID3DXLoadUserData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01471-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01471-109">**ID3DXLoadUserData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="01471-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="01471-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01471-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01471-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01471-111">Methods</span></span>

<span data-ttu-id="01471-112">L’interface **ID3DXLoadUserData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="01471-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="01471-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="01471-113">Method</span></span>                                                              | <span data-ttu-id="01471-114">Description</span><span class="sxs-lookup"><span data-stu-id="01471-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="01471-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="01471-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="01471-116">Charger les données enfants d’un frame à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="01471-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="01471-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="01471-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="01471-118">Charger les données enfants de maillage à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="01471-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="01471-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="01471-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="01471-120">Charger les données de niveau supérieur à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="01471-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="01471-121">Notes</span><span class="sxs-lookup"><span data-stu-id="01471-121">Remarks</span></span>

<span data-ttu-id="01471-122">Le type LPD3DXLOADUSERDATA est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="01471-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="01471-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01471-123">Requirements</span></span>



| <span data-ttu-id="01471-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01471-124">Requirement</span></span> | <span data-ttu-id="01471-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="01471-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01471-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="01471-126">Header</span></span><br/>  | <dl> <span data-ttu-id="01471-127"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="01471-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="01471-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01471-128">Library</span></span><br/> | <dl> <span data-ttu-id="01471-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01471-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01471-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01471-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01471-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="01471-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
