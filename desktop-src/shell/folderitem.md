---
description: Représente un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur l’élément.
title: Objet FolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484025"
---
# <a name="folderitem-object"></a><span data-ttu-id="132ed-104">Objet FolderItem</span><span class="sxs-lookup"><span data-stu-id="132ed-104">FolderItem object</span></span>

<span data-ttu-id="132ed-105">Représente un élément dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="132ed-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="132ed-106">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="132ed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="132ed-107">Members</span></span>

<span data-ttu-id="132ed-108">L’objet **FolderItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="132ed-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="132ed-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="132ed-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="132ed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="132ed-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="132ed-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="132ed-111">Methods</span></span>

<span data-ttu-id="132ed-112">L’objet **FolderItem** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="132ed-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="132ed-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="132ed-113">Method</span></span>                                      | <span data-ttu-id="132ed-114">Description</span><span class="sxs-lookup"><span data-stu-id="132ed-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="132ed-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="132ed-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="132ed-116">Exécute un verbe sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="132ed-117">**Verbes et adverbes**</span><span class="sxs-lookup"><span data-stu-id="132ed-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="132ed-118">Récupère l’objet [**FolderItemVerbs**](folderitemverbs.md) de l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="132ed-119">Cet objet est la collection de verbes qui peuvent être exécutés sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="132ed-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="132ed-120">Properties</span></span>

<span data-ttu-id="132ed-121">L’objet **FolderItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="132ed-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="132ed-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="132ed-122">Property</span></span>                                                   | <span data-ttu-id="132ed-123">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="132ed-123">Access type</span></span>           | <span data-ttu-id="132ed-124">Description</span><span class="sxs-lookup"><span data-stu-id="132ed-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="132ed-125">**Application**</span><span class="sxs-lookup"><span data-stu-id="132ed-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="132ed-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-126">Read-only</span></span><br/>  | <span data-ttu-id="132ed-127">Contient l’objet d' [**application**](folderitem-application.md) de l’élément de dossier.</span><span class="sxs-lookup"><span data-stu-id="132ed-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="132ed-128">**GetFolder ITaskService**</span><span class="sxs-lookup"><span data-stu-id="132ed-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="132ed-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-129">Read-only</span></span><br/>  | <span data-ttu-id="132ed-130">Contient l’objet [**dossier**](folder.md) de l’élément, si l’élément est un dossier.</span><span class="sxs-lookup"><span data-stu-id="132ed-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="132ed-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="132ed-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="132ed-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-132">Read-only</span></span><br/>  | <span data-ttu-id="132ed-133">Contient l’objet [**ShellLinkObject**](shelllinkobject-object.md) de l’élément, si l’élément est un raccourci.</span><span class="sxs-lookup"><span data-stu-id="132ed-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="132ed-134">**IsBrowsable**</span><span class="sxs-lookup"><span data-stu-id="132ed-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="132ed-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-135">Read-only</span></span><br/>  | <span data-ttu-id="132ed-136">Indique si l’élément peut être hébergé à l’intérieur d’un navigateur ou d’un frame de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="132ed-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="132ed-137">**IsFileSystem**</span><span class="sxs-lookup"><span data-stu-id="132ed-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="132ed-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-138">Read-only</span></span><br/>  | <span data-ttu-id="132ed-139">Indique si l’élément fait partie du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="132ed-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="132ed-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="132ed-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="132ed-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-141">Read-only</span></span><br/>  | <span data-ttu-id="132ed-142">Indique si l’élément est un dossier.</span><span class="sxs-lookup"><span data-stu-id="132ed-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="132ed-143">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="132ed-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="132ed-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-144">Read-only</span></span><br/>  | <span data-ttu-id="132ed-145">Indique si l’élément est un raccourci.</span><span class="sxs-lookup"><span data-stu-id="132ed-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="132ed-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="132ed-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="132ed-147">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="132ed-147">Read/write</span></span><br/> | <span data-ttu-id="132ed-148">Définit ou obtient la date et l’heure de la dernière modification d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="132ed-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="132ed-149">[**ModifyDate**](folderitem-modifydate.md) peut être utilisé pour récupérer la date et l’heure de la dernière modification d’un dossier, mais ne peut pas le définir.</span><span class="sxs-lookup"><span data-stu-id="132ed-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="132ed-150">**Nom**</span><span class="sxs-lookup"><span data-stu-id="132ed-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="132ed-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="132ed-151">Read/write</span></span><br/> | <span data-ttu-id="132ed-152">Définit ou obtient le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="132ed-153">**Parent**</span><span class="sxs-lookup"><span data-stu-id="132ed-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="132ed-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-154">Read-only</span></span><br/>  | <span data-ttu-id="132ed-155">Obtient un objet qui représente le parent de l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="132ed-156">**Path**</span><span class="sxs-lookup"><span data-stu-id="132ed-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="132ed-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-157">Read-only</span></span><br/>  | <span data-ttu-id="132ed-158">Contient le chemin d’accès complet et le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="132ed-159">**Corps**</span><span class="sxs-lookup"><span data-stu-id="132ed-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="132ed-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-160">Read-only</span></span><br/>  | <span data-ttu-id="132ed-161">Contient la taille de l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="132ed-162">**Type**</span><span class="sxs-lookup"><span data-stu-id="132ed-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="132ed-163">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="132ed-163">Read-only</span></span><br/>  | <span data-ttu-id="132ed-164">Contient une représentation sous forme de chaîne du type de l’élément.</span><span class="sxs-lookup"><span data-stu-id="132ed-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="132ed-165">Spécifications</span><span class="sxs-lookup"><span data-stu-id="132ed-165">Requirements</span></span>



| <span data-ttu-id="132ed-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="132ed-166">Requirement</span></span> | <span data-ttu-id="132ed-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="132ed-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="132ed-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="132ed-168">Minimum supported client</span></span><br/> | <span data-ttu-id="132ed-169">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="132ed-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="132ed-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="132ed-170">Minimum supported server</span></span><br/> | <span data-ttu-id="132ed-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="132ed-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="132ed-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="132ed-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="132ed-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="132ed-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="132ed-174">MIDL</span><span class="sxs-lookup"><span data-stu-id="132ed-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="132ed-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="132ed-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="132ed-176">DLL</span><span class="sxs-lookup"><span data-stu-id="132ed-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="132ed-177"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="132ed-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




