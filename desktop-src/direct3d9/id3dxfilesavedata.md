---
description: Les applications utilisent les méthodes de l’interface ID3DXFileSaveData pour ajouter des objets de données comme enfants d’un nœud de données de fichier. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interface ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522589"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="b09b0-103">Interface ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="b09b0-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="b09b0-104">Les applications utilisent les méthodes de l’interface ID3DXFileSaveData pour ajouter des objets de données comme enfants d’un nœud de données de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="b09b0-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="b09b0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b09b0-105">Members</span></span>

<span data-ttu-id="b09b0-106">L’interface **ID3DXFileSaveData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b09b0-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b09b0-107">**ID3DXFileSaveData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b09b0-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="b09b0-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b09b0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b09b0-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b09b0-109">Methods</span></span>

<span data-ttu-id="b09b0-110">L’interface **ID3DXFileSaveData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b09b0-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="b09b0-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="b09b0-111">Method</span></span>                                                          | <span data-ttu-id="b09b0-112">Description</span><span class="sxs-lookup"><span data-stu-id="b09b0-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b09b0-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="b09b0-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="b09b0-114">Ajoute un objet de données en tant qu’enfant du nœud de données du fichier **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="b09b0-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="b09b0-115">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="b09b0-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="b09b0-116">Ajoute une référence de données en tant qu’enfant de ce nœud de données de fichier **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="b09b0-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="b09b0-117">La référence de données pointe vers un objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="b09b0-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="b09b0-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="b09b0-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="b09b0-119">Récupère le GUID de ce nœud de données de fichier **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="b09b0-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="b09b0-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="b09b0-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="b09b0-121">Récupère le nom de ce nœud de données de fichier **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="b09b0-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="b09b0-122">**GetSave**</span><span class="sxs-lookup"><span data-stu-id="b09b0-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="b09b0-123">Récupère un pointeur vers ce nœud de données de fichier [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="b09b0-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="b09b0-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="b09b0-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="b09b0-125">Récupère l’ID de modèle de ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="b09b0-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="b09b0-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b09b0-126">Remarks</span></span>

<span data-ttu-id="b09b0-127">Le GUID de l’interface ID3DXFileSaveObject est IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="b09b0-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="b09b0-128">Le type LPD3DXFileSaveData est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="b09b0-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="b09b0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b09b0-129">Requirements</span></span>



| <span data-ttu-id="b09b0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b09b0-130">Requirement</span></span> | <span data-ttu-id="b09b0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b09b0-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b09b0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b09b0-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b09b0-133"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="b09b0-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b09b0-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b09b0-134">Library</span></span><br/> | <dl> <span data-ttu-id="b09b0-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b09b0-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b09b0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b09b0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09b0-137">Interfaces de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="b09b0-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
