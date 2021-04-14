---
description: Représente les objets dans une vue et fournit des propriétés et des méthodes utilisées pour obtenir des informations sur le contenu de la vue.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Objet ShellFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991721"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="d1882-103">Objet ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="d1882-103">ShellFolderView object</span></span>

<span data-ttu-id="d1882-104">Représente les objets dans une vue et fournit des propriétés et des méthodes utilisées pour obtenir des informations sur le contenu de la vue.</span><span class="sxs-lookup"><span data-stu-id="d1882-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="d1882-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d1882-105">Members</span></span>

<span data-ttu-id="d1882-106">L’objet **ShellFolderView** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1882-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="d1882-107">Événements</span><span class="sxs-lookup"><span data-stu-id="d1882-107">Events</span></span>](#events)
-   [<span data-ttu-id="d1882-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1882-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1882-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1882-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="d1882-110">Événements</span><span class="sxs-lookup"><span data-stu-id="d1882-110">Events</span></span>

<span data-ttu-id="d1882-111">L’objet **ShellFolderView** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="d1882-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="d1882-112">Événement</span><span class="sxs-lookup"><span data-stu-id="d1882-112">Event</span></span>                                                        | <span data-ttu-id="d1882-113">Description</span><span class="sxs-lookup"><span data-stu-id="d1882-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1882-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="d1882-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="d1882-115">Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.</span><span class="sxs-lookup"><span data-stu-id="d1882-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d1882-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1882-116">Methods</span></span>

<span data-ttu-id="d1882-117">L’objet **ShellFolderView** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d1882-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="d1882-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="d1882-118">Method</span></span>                                                 | <span data-ttu-id="d1882-119">Description</span><span class="sxs-lookup"><span data-stu-id="d1882-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1882-120">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="d1882-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="d1882-121">Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d1882-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="d1882-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="d1882-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="d1882-123">Obtient un objet [**FolderItems**](folderitems.md) qui représente tous les éléments sélectionnés dans la vue.</span><span class="sxs-lookup"><span data-stu-id="d1882-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="d1882-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="d1882-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="d1882-125">Définit l’état de sélection d’un élément dans la vue.</span><span class="sxs-lookup"><span data-stu-id="d1882-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="d1882-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1882-126">Properties</span></span>

<span data-ttu-id="d1882-127">L’objet **ShellFolderView** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d1882-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="d1882-128">Propriété</span><span class="sxs-lookup"><span data-stu-id="d1882-128">Property</span></span>                                                      | <span data-ttu-id="d1882-129">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d1882-129">Access type</span></span>          | <span data-ttu-id="d1882-130">Description</span><span class="sxs-lookup"><span data-stu-id="d1882-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1882-131">**Application**</span><span class="sxs-lookup"><span data-stu-id="d1882-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="d1882-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1882-132">Read-only</span></span><br/> | <span data-ttu-id="d1882-133">Contient l’objet d’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1882-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="d1882-134">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="d1882-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="d1882-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1882-135">Read-only</span></span><br/> | <span data-ttu-id="d1882-136">Obtient un objet [**FolderItem**](folderitem.md) qui représente l’élément ayant le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d1882-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="d1882-137">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="d1882-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="d1882-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1882-138">Read-only</span></span><br/> | <span data-ttu-id="d1882-139">Obtient un objet [**dossier**](folder.md) qui représente la vue.</span><span class="sxs-lookup"><span data-stu-id="d1882-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="d1882-140">**Parent**</span><span class="sxs-lookup"><span data-stu-id="d1882-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="d1882-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1882-141">Read-only</span></span><br/> | <span data-ttu-id="d1882-142">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d1882-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d1882-143">**Conseils**</span><span class="sxs-lookup"><span data-stu-id="d1882-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="d1882-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1882-144">Read-only</span></span><br/> | <span data-ttu-id="d1882-145">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d1882-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d1882-146">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="d1882-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="d1882-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1882-147">Read-only</span></span><br/> | <span data-ttu-id="d1882-148">Obtient un jeu d’indicateurs qui indiquent les options actuelles de la vue.</span><span class="sxs-lookup"><span data-stu-id="d1882-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="d1882-149">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d1882-149">Requirements</span></span>



| <span data-ttu-id="d1882-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1882-150">Requirement</span></span> | <span data-ttu-id="d1882-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1882-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1882-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1882-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d1882-153">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1882-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d1882-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1882-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d1882-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1882-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1882-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1882-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1882-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1882-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d1882-158">MIDL</span><span class="sxs-lookup"><span data-stu-id="d1882-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1882-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1882-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d1882-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d1882-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1882-161"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d1882-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="d1882-162">IID</span><span class="sxs-lookup"><span data-stu-id="d1882-162">IID</span></span><br/>                      | <span data-ttu-id="d1882-163">CLSID \_ ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="d1882-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="d1882-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1882-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1882-165">**Indicateurs ShellFolderViewOptions**</span><span class="sxs-lookup"><span data-stu-id="d1882-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




