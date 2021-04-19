---
description: Les applications utilisent les méthodes de l’interface ID3DXFileSaveObject pour écrire un fichier. x sur le disque, ainsi que pour ajouter et enregistrer des objets et des modèles de données.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interface ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532439"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="fcdd5-103">Interface ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="fcdd5-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="fcdd5-104">Les applications utilisent les méthodes de l’interface ID3DXFileSaveObject pour écrire un fichier. x sur le disque, ainsi que pour ajouter et enregistrer des objets et des modèles de données.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="fcdd5-105">Membres</span><span class="sxs-lookup"><span data-stu-id="fcdd5-105">Members</span></span>

<span data-ttu-id="fcdd5-106">L’interface **ID3DXFileSaveObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fcdd5-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fcdd5-107">**ID3DXFileSaveObject** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fcdd5-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="fcdd5-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fcdd5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fcdd5-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fcdd5-109">Methods</span></span>

<span data-ttu-id="fcdd5-110">L’interface **ID3DXFileSaveObject** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="fcdd5-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="fcdd5-111">Method</span></span>                                                      | <span data-ttu-id="fcdd5-112">Description</span><span class="sxs-lookup"><span data-stu-id="fcdd5-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcdd5-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="fcdd5-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="fcdd5-114">Ajoute un objet de données en tant qu’enfant de l’objet [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="fcdd5-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="fcdd5-115">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="fcdd5-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="fcdd5-116">Obtient l’interface [**ID3DXFile**](id3dxfile.md) de l’objet qui a créé cet objet **ID3DXFileSaveObject** .</span><span class="sxs-lookup"><span data-stu-id="fcdd5-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="fcdd5-117">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="fcdd5-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="fcdd5-118">Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="fcdd5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fcdd5-119">Remarks</span></span>

<span data-ttu-id="fcdd5-120">Les modèles ne sont pas requis dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-120">Templates are not required in every file.</span></span> <span data-ttu-id="fcdd5-121">Par exemple, vous pouvez placer tous les modèles dans un seul fichier. x plutôt que de les dupliquer dans chaque fichier. x.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="fcdd5-122">L’interface ID3DXFileSaveObject est obtenue en appelant la méthode [**ID3DXFile :: CreateSaveObject**](id3dxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="fcdd5-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="fcdd5-123">L’identificateur global unique (GUID) de l’interface ID3DXFileSaveObject est IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="fcdd5-124">Le type LPD3DXFILESAVEOBJECT est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="fcdd5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcdd5-125">Requirements</span></span>



| <span data-ttu-id="fcdd5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcdd5-126">Requirement</span></span> | <span data-ttu-id="fcdd5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcdd5-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcdd5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcdd5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fcdd5-129"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcdd5-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="fcdd5-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcdd5-130">Library</span></span><br/> | <dl> <span data-ttu-id="fcdd5-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcdd5-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fcdd5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcdd5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcdd5-133">Interfaces de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="fcdd5-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
