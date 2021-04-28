---
description: 'Interface ID3DXSaveUserData : cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x.'
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interface ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbdc71239455772809e44f535634a0d06cc0653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107177"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="e7f09-103">Interface ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="e7f09-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="e7f09-104">Cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x.</span><span class="sxs-lookup"><span data-stu-id="e7f09-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="e7f09-105">Une instance de cette interface est passée à [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), et D3DX appelle la méthode appropriée sur cette interface chaque fois que les données appropriées sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="e7f09-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="e7f09-106">Par exemple, pour chaque objet frame du fichier. x, [**ID3DXSaveUserData :: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) est appelé et reçoit les données enfants.</span><span class="sxs-lookup"><span data-stu-id="e7f09-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="e7f09-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e7f09-107">Members</span></span>

<span data-ttu-id="e7f09-108">L’interface **ID3DXSaveUserData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e7f09-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7f09-109">**ID3DXSaveUserData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e7f09-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="e7f09-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e7f09-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7f09-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e7f09-111">Methods</span></span>

<span data-ttu-id="e7f09-112">L’interface **ID3DXSaveUserData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e7f09-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="e7f09-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="e7f09-113">Method</span></span>                                                                              | <span data-ttu-id="e7f09-114">Description</span><span class="sxs-lookup"><span data-stu-id="e7f09-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="e7f09-115">**AddFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="e7f09-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="e7f09-116">Ajoutez des données enfants au frame.</span><span class="sxs-lookup"><span data-stu-id="e7f09-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="e7f09-117">**AddMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="e7f09-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="e7f09-118">Ajoutez des données enfants à la maille.</span><span class="sxs-lookup"><span data-stu-id="e7f09-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="e7f09-119">**AddTopLevelDataObjectsPost**</span><span class="sxs-lookup"><span data-stu-id="e7f09-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="e7f09-120">Ajoutez un objet de niveau supérieur après la hiérarchie de frames.</span><span class="sxs-lookup"><span data-stu-id="e7f09-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="e7f09-121">**AddTopLevelDataObjectsPre**</span><span class="sxs-lookup"><span data-stu-id="e7f09-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="e7f09-122">Ajoutez un objet de niveau supérieur avant la hiérarchie des frames.</span><span class="sxs-lookup"><span data-stu-id="e7f09-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="e7f09-123">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="e7f09-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="e7f09-124">Rappel permettant à l’utilisateur d’inscrire un modèle de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="e7f09-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="e7f09-125">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="e7f09-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="e7f09-126">Rappel permettant à l’utilisateur d’enregistrer un modèle de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="e7f09-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e7f09-127">Notes </span><span class="sxs-lookup"><span data-stu-id="e7f09-127">Remarks</span></span>

<span data-ttu-id="e7f09-128">Le type LPD3DXSAVEUSERDATA est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="e7f09-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="e7f09-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f09-129">Requirements</span></span>



| <span data-ttu-id="e7f09-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f09-130">Requirement</span></span> | <span data-ttu-id="e7f09-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f09-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f09-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7f09-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e7f09-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f09-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e7f09-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7f09-134">Library</span></span><br/> | <dl> <span data-ttu-id="e7f09-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f09-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7f09-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f09-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f09-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e7f09-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
