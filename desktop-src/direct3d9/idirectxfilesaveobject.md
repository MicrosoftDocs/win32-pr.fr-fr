---
description: Les applications utilisent les méthodes de l’interface IDirectXFileSaveObject pour créer des objets de données et enregistrer des modèles et des objets de données.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interface IDirectXFileSaveObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520317"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="8f1d5-103">Interface IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="8f1d5-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="8f1d5-104">Les applications utilisent les méthodes de l’interface IDirectXFileSaveObject pour créer des objets de données et enregistrer des modèles et des objets de données.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="8f1d5-105">Notez que les modèles ne sont pas requis dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="8f1d5-106">Par exemple, vous pouvez placer tous les modèles dans un seul fichier Microsoft DirectX au lieu de les dupliquer dans chaque fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="8f1d5-107">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="8f1d5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8f1d5-108">Members</span></span>

<span data-ttu-id="8f1d5-109">L’interface **IDirectXFileSaveObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8f1d5-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8f1d5-110">**IDirectXFileSaveObject** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f1d5-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="8f1d5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f1d5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8f1d5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f1d5-112">Methods</span></span>

<span data-ttu-id="8f1d5-113">L’interface **IDirectXFileSaveObject** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="8f1d5-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="8f1d5-114">Method</span></span>                                                               | <span data-ttu-id="8f1d5-115">Description</span><span class="sxs-lookup"><span data-stu-id="8f1d5-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8f1d5-116">**CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="8f1d5-117">Crée un objet de données.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-117">Creates a data object.</span></span> <span data-ttu-id="8f1d5-118">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="8f1d5-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="8f1d5-120">Enregistre un objet de données et ses enfants dans un fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="8f1d5-121">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="8f1d5-122">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="8f1d5-123">Enregistre les modèles dans un fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="8f1d5-124">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="8f1d5-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8f1d5-125">Remarks</span></span>

<span data-ttu-id="8f1d5-126">L’identificateur global unique (GUID) de l’interface IDirectXFileSaveObject est **IID \_ IDirectXFileSaveObject**.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="8f1d5-127">L’interface **IDirectXFileSaveObject** est obtenue en appelant la méthode [**IDirectXFile :: CreateSaveObject**](idirectxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="8f1d5-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="8f1d5-128">Le type **LPDIRECTXFILESAVEOBJECT** est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="8f1d5-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f1d5-129">Requirements</span></span>



| <span data-ttu-id="8f1d5-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f1d5-130">Requirement</span></span> | <span data-ttu-id="8f1d5-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f1d5-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1d5-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f1d5-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8f1d5-133"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d5-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f1d5-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8f1d5-134">Library</span></span><br/> | <dl> <span data-ttu-id="8f1d5-135"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d5-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f1d5-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f1d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f1d5-137">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="8f1d5-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
