---
description: Les applications utilisent les méthodes de l’interface IDirectXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interface IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522976"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="b05bf-103">Interface IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="b05bf-103">IDirectXFileData interface</span></span>

<span data-ttu-id="b05bf-104">Les applications utilisent les méthodes de l’interface IDirectXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="b05bf-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="b05bf-105">Les restrictions de modèle déterminent la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="b05bf-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="b05bf-106">Les types de données autorisés par le modèle sont appelés membres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b05bf-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="b05bf-107">Les membres facultatifs ne sont pas requis, mais un objet peut manquer des informations importantes sans eux.</span><span class="sxs-lookup"><span data-stu-id="b05bf-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="b05bf-108">Ces membres facultatifs sont enregistrés en tant qu’enfants de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="b05bf-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="b05bf-109">Les enfants peuvent être un autre objet de données, une référence à un objet de données antérieur ou un objet binaire.</span><span class="sxs-lookup"><span data-stu-id="b05bf-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="b05bf-110">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="b05bf-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b05bf-111">Members</span></span>

<span data-ttu-id="b05bf-112">L’interface **IDirectXFileData** hérite de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="b05bf-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="b05bf-113">**IDirectXFileData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b05bf-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="b05bf-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b05bf-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b05bf-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b05bf-115">Methods</span></span>

<span data-ttu-id="b05bf-116">L’interface **IDirectXFileData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b05bf-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="b05bf-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="b05bf-117">Method</span></span>                                                         | <span data-ttu-id="b05bf-118">Description</span><span class="sxs-lookup"><span data-stu-id="b05bf-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b05bf-119">**AddBinaryObject**</span><span class="sxs-lookup"><span data-stu-id="b05bf-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="b05bf-120">Crée un objet binaire et l’ajoute en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b05bf-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="b05bf-121">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="b05bf-122">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="b05bf-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="b05bf-123">Ajoute un objet de données en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b05bf-123">Adds a data object as a child object.</span></span> <span data-ttu-id="b05bf-124">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="b05bf-125">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="b05bf-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="b05bf-126">Crée et ajoute un objet de référence de données en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b05bf-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="b05bf-127">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="b05bf-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="b05bf-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="b05bf-129">Récupère les données de l’un des membres de l’objet ou les données de tous les membres.</span><span class="sxs-lookup"><span data-stu-id="b05bf-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="b05bf-130">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="b05bf-131">**GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="b05bf-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="b05bf-132">Récupère l’objet de données enfants, l’objet de référence de données ou l’objet binaire suivant dans le fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="b05bf-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="b05bf-133">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="b05bf-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="b05bf-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="b05bf-135">Récupère le GUID du modèle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b05bf-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="b05bf-136">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b05bf-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b05bf-137">Notes</span><span class="sxs-lookup"><span data-stu-id="b05bf-137">Remarks</span></span>

<span data-ttu-id="b05bf-138">Le GUID de l’interface IDirectXFileData est IID \_ IDirectXFileData.</span><span class="sxs-lookup"><span data-stu-id="b05bf-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="b05bf-139">Le type LPDIRECTXFILEDATA est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="b05bf-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="b05bf-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b05bf-140">Requirements</span></span>



| <span data-ttu-id="b05bf-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b05bf-141">Requirement</span></span> | <span data-ttu-id="b05bf-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="b05bf-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b05bf-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="b05bf-143">Header</span></span><br/>  | <dl> <span data-ttu-id="b05bf-144"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b05bf-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b05bf-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b05bf-145">Library</span></span><br/> | <dl> <span data-ttu-id="b05bf-146"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b05bf-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b05bf-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b05bf-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b05bf-148">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="b05bf-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="b05bf-149">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="b05bf-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




