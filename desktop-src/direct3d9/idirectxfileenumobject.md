---
description: Les applications utilisent les méthodes de l’interface IDirectXFileEnumObject pour parcourir les objets de données dans le fichier et pour récupérer un objet de données par son identificateur global unique (GUID) ou par son nom. Action déconseillée.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interface IDirectXFileEnumObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538509"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="6bbfc-104">Interface IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="6bbfc-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="6bbfc-105">Les applications utilisent les méthodes de l’interface IDirectXFileEnumObject pour parcourir les objets de données dans le fichier et pour récupérer un objet de données par son identificateur global unique (GUID) ou par son nom.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="6bbfc-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="6bbfc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6bbfc-107">Members</span></span>

<span data-ttu-id="6bbfc-108">L’interface **IDirectXFileEnumObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6bbfc-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6bbfc-109">**IDirectXFileEnumObject** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6bbfc-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="6bbfc-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6bbfc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6bbfc-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6bbfc-111">Methods</span></span>

<span data-ttu-id="6bbfc-112">L’interface **IDirectXFileEnumObject** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="6bbfc-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="6bbfc-113">Method</span></span>                                                                     | <span data-ttu-id="6bbfc-114">Description</span><span class="sxs-lookup"><span data-stu-id="6bbfc-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="6bbfc-115">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="6bbfc-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="6bbfc-116">Récupère l’objet de données qui a le GUID spécifié.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="6bbfc-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="6bbfc-118">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="6bbfc-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="6bbfc-119">Récupère l’objet de données qui porte le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="6bbfc-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="6bbfc-121">**GetNextDataObject**</span><span class="sxs-lookup"><span data-stu-id="6bbfc-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="6bbfc-122">Récupère l’objet de niveau supérieur suivant dans le fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="6bbfc-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6bbfc-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6bbfc-124">Remarks</span></span>

<span data-ttu-id="6bbfc-125">Le GUID de l’interface IDirectXFileEnumObject est IID \_ IDirectXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="6bbfc-126">Le type LPDIRECTXFILEENUMOBJECT est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="6bbfc-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="6bbfc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bbfc-127">Requirements</span></span>



| <span data-ttu-id="6bbfc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bbfc-128">Requirement</span></span> | <span data-ttu-id="6bbfc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bbfc-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbfc-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bbfc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6bbfc-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bbfc-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="6bbfc-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6bbfc-132">Library</span></span><br/> | <dl> <span data-ttu-id="6bbfc-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bbfc-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bbfc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bbfc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbfc-135">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="6bbfc-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
