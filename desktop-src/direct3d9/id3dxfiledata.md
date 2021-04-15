---
description: Les applications utilisent les méthodes de l’interface ID3DXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données. Les restrictions de modèle déterminent la hiérarchie.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interface ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211844"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="828e4-104">Interface ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="828e4-104">ID3DXFileData interface</span></span>

<span data-ttu-id="828e4-105">Les applications utilisent les méthodes de l’interface ID3DXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="828e4-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="828e4-106">Les restrictions de modèle déterminent la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="828e4-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="828e4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="828e4-107">Members</span></span>

<span data-ttu-id="828e4-108">L’interface **ID3DXFileData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="828e4-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="828e4-109">**ID3DXFileData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="828e4-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="828e4-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="828e4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="828e4-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="828e4-111">Methods</span></span>

<span data-ttu-id="828e4-112">L’interface **ID3DXFileData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="828e4-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="828e4-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="828e4-113">Method</span></span>                                            | <span data-ttu-id="828e4-114">Description</span><span class="sxs-lookup"><span data-stu-id="828e4-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="828e4-115">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="828e4-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="828e4-116">Récupère un objet enfant dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="828e4-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="828e4-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="828e4-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="828e4-118">Récupère le nombre d’enfants dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="828e4-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="828e4-119">**GetEnum**</span><span class="sxs-lookup"><span data-stu-id="828e4-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="828e4-120">Récupère l’objet d’énumération dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="828e4-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="828e4-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="828e4-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="828e4-122">Récupère le GUID de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="828e4-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="828e4-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="828e4-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="828e4-124">Récupère le nom de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="828e4-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="828e4-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="828e4-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="828e4-126">Récupère l’ID de modèle dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="828e4-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="828e4-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="828e4-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="828e4-128">Indique si cet objet de données de fichier est un objet de référence qui pointe vers un autre objet de données enfant.</span><span class="sxs-lookup"><span data-stu-id="828e4-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="828e4-129">**Lock**</span><span class="sxs-lookup"><span data-stu-id="828e4-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="828e4-130">Accède aux données du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="828e4-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="828e4-131">**Bloquer**</span><span class="sxs-lookup"><span data-stu-id="828e4-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="828e4-132">Termine la durée de vie du pointeur *ppData* retourné par [**ID3DXFileData :: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="828e4-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="828e4-133">Notes</span><span class="sxs-lookup"><span data-stu-id="828e4-133">Remarks</span></span>

<span data-ttu-id="828e4-134">Les types de données autorisés par le modèle sont appelés membres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="828e4-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="828e4-135">Les membres facultatifs ne sont pas requis, mais un objet peut manquer des informations importantes sans eux.</span><span class="sxs-lookup"><span data-stu-id="828e4-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="828e4-136">Ces membres facultatifs sont enregistrés en tant qu’enfants de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="828e4-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="828e4-137">Un enfant peut être un autre objet de données ou une référence à un objet de données antérieur.</span><span class="sxs-lookup"><span data-stu-id="828e4-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="828e4-138">Le GUID de l’interface ID3DXFileData est IID \_ ID3DXFileData.</span><span class="sxs-lookup"><span data-stu-id="828e4-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="828e4-139">Le type LPD3DXFILEDATA est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="828e4-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="828e4-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="828e4-140">Requirements</span></span>



| <span data-ttu-id="828e4-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="828e4-141">Requirement</span></span> | <span data-ttu-id="828e4-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="828e4-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="828e4-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="828e4-143">Header</span></span><br/>  | <dl> <span data-ttu-id="828e4-144"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="828e4-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="828e4-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="828e4-145">Library</span></span><br/> | <dl> <span data-ttu-id="828e4-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="828e4-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="828e4-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="828e4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828e4-148">Interfaces de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="828e4-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
