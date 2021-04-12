---
description: Les applications utilisent les méthodes de l’interface IDirectXFileDataReference pour prendre en charge les objets de référence de données.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interface IDirectXFileDataReference (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116310"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="fd225-103">Interface IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="fd225-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="fd225-104">Les applications utilisent les méthodes de l’interface IDirectXFileDataReference pour prendre en charge les objets de référence de données.</span><span class="sxs-lookup"><span data-stu-id="fd225-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="fd225-105">Un objet de référence de données fait référence à un objet de données défini précédemment dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="fd225-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="fd225-106">Cela vous permet d’utiliser le même objet plusieurs fois sans le répéter dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="fd225-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="fd225-107">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fd225-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="fd225-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fd225-108">Members</span></span>

<span data-ttu-id="fd225-109">L’interface **IDirectXFileDataReference** hérite de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="fd225-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="fd225-110">**IDirectXFileDataReference** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd225-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="fd225-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd225-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fd225-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd225-112">Methods</span></span>

<span data-ttu-id="fd225-113">L’interface **IDirectXFileDataReference** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fd225-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="fd225-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="fd225-114">Method</span></span>                                                | <span data-ttu-id="fd225-115">Description</span><span class="sxs-lookup"><span data-stu-id="fd225-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="fd225-116">**Résolution**</span><span class="sxs-lookup"><span data-stu-id="fd225-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="fd225-117">Résout les références de données.</span><span class="sxs-lookup"><span data-stu-id="fd225-117">Resolves data references.</span></span> <span data-ttu-id="fd225-118">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fd225-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd225-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fd225-119">Remarks</span></span>

<span data-ttu-id="fd225-120">Une fois que vous avez déterminé qu’un objet est un objet de référence de données, utilisez la méthode [**IDirectXFileDataReference :: Resolve**](idirectxfiledatareference--resolve.md) pour récupérer l’objet référencé défini précédemment dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="fd225-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="fd225-121">Pour plus d’informations sur l’identification d’un objet de référence de données, consultez l’interface [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="fd225-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="fd225-122">Le GUID de l’interface IDirectXFileDataReference est IID \_ IDirectXFileDataReference.</span><span class="sxs-lookup"><span data-stu-id="fd225-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="fd225-123">Le type LPDIRECTXFILEDataReference est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="fd225-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="fd225-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd225-124">Requirements</span></span>



| <span data-ttu-id="fd225-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd225-125">Requirement</span></span> | <span data-ttu-id="fd225-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd225-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd225-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd225-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fd225-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd225-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd225-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd225-129">Library</span></span><br/> | <dl> <span data-ttu-id="fd225-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd225-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd225-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd225-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd225-132">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="fd225-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="fd225-133">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="fd225-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




