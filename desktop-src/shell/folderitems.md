---
description: Représente la collection d’éléments dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.
title: Objet FolderItems (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840650"
---
# <a name="folderitems-object"></a><span data-ttu-id="9531f-104">Objet FolderItems</span><span class="sxs-lookup"><span data-stu-id="9531f-104">FolderItems object</span></span>

<span data-ttu-id="9531f-105">Représente la collection d’éléments dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="9531f-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="9531f-106">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.</span><span class="sxs-lookup"><span data-stu-id="9531f-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="9531f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9531f-107">Members</span></span>

<span data-ttu-id="9531f-108">L’objet **FolderItems** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9531f-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="9531f-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9531f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9531f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9531f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9531f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9531f-111">Methods</span></span>

<span data-ttu-id="9531f-112">L’objet **FolderItems** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9531f-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="9531f-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="9531f-113">Method</span></span>                                    | <span data-ttu-id="9531f-114">Description</span><span class="sxs-lookup"><span data-stu-id="9531f-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9531f-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="9531f-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="9531f-116">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="9531f-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="9531f-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9531f-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="9531f-118">Récupère l’objet [**FolderItem**](folderitem.md) pour un élément spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="9531f-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9531f-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9531f-119">Properties</span></span>

<span data-ttu-id="9531f-120">L’objet **FolderItems** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9531f-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="9531f-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="9531f-121">Property</span></span>                                                  | <span data-ttu-id="9531f-122">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="9531f-122">Access type</span></span>          | <span data-ttu-id="9531f-123">Description</span><span class="sxs-lookup"><span data-stu-id="9531f-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9531f-124">**Application**</span><span class="sxs-lookup"><span data-stu-id="9531f-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="9531f-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9531f-125">Read-only</span></span><br/> | <span data-ttu-id="9531f-126">Contient l’objet [**application**](folderitems-application.md) de la collection d’éléments Folder.</span><span class="sxs-lookup"><span data-stu-id="9531f-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="9531f-127">**Count**</span><span class="sxs-lookup"><span data-stu-id="9531f-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="9531f-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9531f-128">Read-only</span></span><br/> | <span data-ttu-id="9531f-129">Contient le nombre d’éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="9531f-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="9531f-130">**Parent**</span><span class="sxs-lookup"><span data-stu-id="9531f-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="9531f-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9531f-131">Read-only</span></span><br/> | <span data-ttu-id="9531f-132">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="9531f-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="9531f-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9531f-133">Requirements</span></span>



| <span data-ttu-id="9531f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9531f-134">Requirement</span></span> | <span data-ttu-id="9531f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9531f-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9531f-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9531f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9531f-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9531f-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9531f-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9531f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9531f-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9531f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9531f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="9531f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9531f-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9531f-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9531f-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="9531f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9531f-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9531f-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9531f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9531f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9531f-145"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9531f-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




