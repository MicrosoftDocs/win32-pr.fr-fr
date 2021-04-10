---
description: Les applications utilisent les méthodes de l’interface ID3DXFileEnumObject pour parcourir les objets de données de fichier enfant dans le fichier et pour récupérer un objet enfant par son identificateur global unique (GUID) ou par son nom.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interface ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953905"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="60a06-103">Interface ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="60a06-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="60a06-104">Les applications utilisent les méthodes de l’interface ID3DXFileEnumObject pour parcourir les objets de données de fichier enfant dans le fichier et pour récupérer un objet enfant par son identificateur global unique (GUID) ou par son nom.</span><span class="sxs-lookup"><span data-stu-id="60a06-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="60a06-105">Membres</span><span class="sxs-lookup"><span data-stu-id="60a06-105">Members</span></span>

<span data-ttu-id="60a06-106">L’interface **ID3DXFileEnumObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="60a06-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="60a06-107">**ID3DXFileEnumObject** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="60a06-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="60a06-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="60a06-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60a06-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="60a06-109">Methods</span></span>

<span data-ttu-id="60a06-110">L’interface **ID3DXFileEnumObject** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="60a06-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="60a06-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="60a06-111">Method</span></span>                                                                  | <span data-ttu-id="60a06-112">Description</span><span class="sxs-lookup"><span data-stu-id="60a06-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="60a06-113">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="60a06-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="60a06-114">Récupère un objet enfant dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="60a06-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="60a06-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="60a06-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="60a06-116">Récupère le nombre d’objets enfants dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="60a06-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="60a06-117">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="60a06-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="60a06-118">Récupère l’objet de données qui a le GUID spécifié.</span><span class="sxs-lookup"><span data-stu-id="60a06-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="60a06-119">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="60a06-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="60a06-120">Récupère l’objet de données qui porte le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="60a06-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="60a06-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="60a06-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="60a06-122">Récupère l’objet [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="60a06-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="60a06-123">Notes</span><span class="sxs-lookup"><span data-stu-id="60a06-123">Remarks</span></span>

<span data-ttu-id="60a06-124">Le GUID de l’interface ID3DXFileEnumObject est IID \_ ID3DXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="60a06-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="60a06-125">Le type LPD3DXFILEENUMOBJECT est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="60a06-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="60a06-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60a06-126">Requirements</span></span>



| <span data-ttu-id="60a06-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60a06-127">Requirement</span></span> | <span data-ttu-id="60a06-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="60a06-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60a06-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="60a06-129">Header</span></span><br/>  | <dl> <span data-ttu-id="60a06-130"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="60a06-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="60a06-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60a06-131">Library</span></span><br/> | <dl> <span data-ttu-id="60a06-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60a06-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="60a06-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60a06-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a06-134">Interfaces de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="60a06-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
