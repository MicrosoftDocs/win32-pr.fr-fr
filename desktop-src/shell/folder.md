---
description: Représente un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le dossier.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objet Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524492"
---
# <a name="folder-object"></a><span data-ttu-id="77fd9-104">Objet Folder</span><span class="sxs-lookup"><span data-stu-id="77fd9-104">Folder object</span></span>

<span data-ttu-id="77fd9-105">Représente un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="77fd9-105">Represents a Shell folder.</span></span> <span data-ttu-id="77fd9-106">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="77fd9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="77fd9-107">Members</span></span>

<span data-ttu-id="77fd9-108">L’objet **Folder** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="77fd9-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="77fd9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="77fd9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="77fd9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77fd9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="77fd9-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="77fd9-111">Methods</span></span>

<span data-ttu-id="77fd9-112">L’objet **Folder** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="77fd9-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="77fd9-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="77fd9-113">Method</span></span>                                      | <span data-ttu-id="77fd9-114">Description</span><span class="sxs-lookup"><span data-stu-id="77fd9-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77fd9-115">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="77fd9-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="77fd9-116">Copie un ou des éléments dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="77fd9-117">**GetDetailsOf**</span><span class="sxs-lookup"><span data-stu-id="77fd9-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="77fd9-118">Récupère des détails sur un élément dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="77fd9-119">Par exemple, sa taille, son type ou l’heure de sa dernière modification.</span><span class="sxs-lookup"><span data-stu-id="77fd9-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="77fd9-120">**Éléments**</span><span class="sxs-lookup"><span data-stu-id="77fd9-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="77fd9-121">Récupère un objet [**FolderItems**](folderitems.md) qui représente la collection d’éléments dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="77fd9-122">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="77fd9-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="77fd9-123">Déplace un élément ou des éléments vers ce dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="77fd9-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="77fd9-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="77fd9-125">Crée un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="77fd9-126">**ParseName**</span><span class="sxs-lookup"><span data-stu-id="77fd9-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="77fd9-127">Crée et retourne un objet [**FolderItem**](folderitem.md) qui représente un élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="77fd9-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="77fd9-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77fd9-128">Properties</span></span>

<span data-ttu-id="77fd9-129">L’objet **Folder** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="77fd9-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="77fd9-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="77fd9-130">Property</span></span>                                               | <span data-ttu-id="77fd9-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="77fd9-131">Access type</span></span>          | <span data-ttu-id="77fd9-132">Description</span><span class="sxs-lookup"><span data-stu-id="77fd9-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="77fd9-133">**Application**</span><span class="sxs-lookup"><span data-stu-id="77fd9-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="77fd9-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77fd9-134">Read-only</span></span><br/> | <span data-ttu-id="77fd9-135">Contient l’objet d’application du dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="77fd9-136">**Parent**</span><span class="sxs-lookup"><span data-stu-id="77fd9-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="77fd9-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77fd9-137">Read-only</span></span><br/> | <span data-ttu-id="77fd9-138">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="77fd9-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="77fd9-139">**ParentFolder**</span><span class="sxs-lookup"><span data-stu-id="77fd9-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="77fd9-140">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77fd9-140">Read-only</span></span><br/> | <span data-ttu-id="77fd9-141">Contient l’objet **dossier** parent.</span><span class="sxs-lookup"><span data-stu-id="77fd9-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="77fd9-142">**Bonhomme**</span><span class="sxs-lookup"><span data-stu-id="77fd9-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="77fd9-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77fd9-143">Read-only</span></span><br/> | <span data-ttu-id="77fd9-144">Contient le titre du dossier.</span><span class="sxs-lookup"><span data-stu-id="77fd9-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="77fd9-145">Notes</span><span class="sxs-lookup"><span data-stu-id="77fd9-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="77fd9-146">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="77fd9-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="77fd9-147">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="77fd9-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="77fd9-148">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="77fd9-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77fd9-149">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77fd9-149">Requirements</span></span>



| <span data-ttu-id="77fd9-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77fd9-150">Requirement</span></span> | <span data-ttu-id="77fd9-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="77fd9-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77fd9-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77fd9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="77fd9-153">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77fd9-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="77fd9-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77fd9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="77fd9-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77fd9-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="77fd9-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="77fd9-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="77fd9-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77fd9-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="77fd9-158">MIDL</span><span class="sxs-lookup"><span data-stu-id="77fd9-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77fd9-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77fd9-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




