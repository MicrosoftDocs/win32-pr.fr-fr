---
description: Les applications utilisent les méthodes de l’interface IDirectXFile pour créer des instances des interfaces IDirectXFileEnumObject et IDirectXFileSaveObject, et pour inscrire des modèles. Action déconseillée.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interface IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870177"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="71212-104">Interface IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="71212-104">IDirectXFile interface</span></span>

<span data-ttu-id="71212-105">Les applications utilisent les méthodes de l’interface IDirectXFile pour créer des instances des interfaces [**IDirectXFileEnumObject**](idirectxfileenumobject.md) et [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , et pour inscrire des modèles.</span><span class="sxs-lookup"><span data-stu-id="71212-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="71212-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="71212-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="71212-107">Membres</span><span class="sxs-lookup"><span data-stu-id="71212-107">Members</span></span>

<span data-ttu-id="71212-108">L’interface **IDirectXFile** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71212-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="71212-109">**IDirectXFile** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71212-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="71212-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71212-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="71212-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71212-111">Methods</span></span>

<span data-ttu-id="71212-112">L’interface **IDirectXFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="71212-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="71212-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="71212-113">Method</span></span>                                                       | <span data-ttu-id="71212-114">Description</span><span class="sxs-lookup"><span data-stu-id="71212-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="71212-115">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="71212-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="71212-116">Crée un objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="71212-116">Creates an enumerator object.</span></span> <span data-ttu-id="71212-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="71212-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="71212-118">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="71212-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="71212-119">Crée un objet Save.</span><span class="sxs-lookup"><span data-stu-id="71212-119">Creates a save object.</span></span> <span data-ttu-id="71212-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="71212-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="71212-121">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="71212-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="71212-122">Inscrit des modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="71212-122">Registers custom templates.</span></span> <span data-ttu-id="71212-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="71212-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="71212-124">Notes</span><span class="sxs-lookup"><span data-stu-id="71212-124">Remarks</span></span>

<span data-ttu-id="71212-125">L’identificateur global unique (GUID) de l’interface IDirectXFile est IID \_ IDirectXFile.</span><span class="sxs-lookup"><span data-stu-id="71212-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="71212-126">L’interface IDirectXFile est obtenue en appelant la fonction [**DirectXFileCreate**](directxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="71212-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="71212-127">Le type LPDIRECTXFILE est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="71212-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="71212-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71212-128">Requirements</span></span>



| <span data-ttu-id="71212-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71212-129">Requirement</span></span> | <span data-ttu-id="71212-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="71212-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71212-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="71212-131">Header</span></span><br/>  | <dl> <span data-ttu-id="71212-132"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="71212-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="71212-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71212-133">Library</span></span><br/> | <dl> <span data-ttu-id="71212-134"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71212-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71212-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71212-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71212-136">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="71212-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
