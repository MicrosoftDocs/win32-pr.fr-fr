---
title: WebViewFolderContents, objet (Shldisp.h)
description: Implémenté par le Shell pour une utilisation à l’intérieur d’une WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Fonctionnalités de l’environnement Windows hérité de l’objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, Description
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511346"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="1da6d-105">Objet WebViewFolderContents</span><span class="sxs-lookup"><span data-stu-id="1da6d-105">WebViewFolderContents object</span></span>

<span data-ttu-id="1da6d-106">Implémenté par le Shell pour une utilisation à l’intérieur d’une *WebView*.</span><span class="sxs-lookup"><span data-stu-id="1da6d-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="1da6d-107">**WebViewFolderContents** s’initialise automatiquement dans le dossier actif de WebView.</span><span class="sxs-lookup"><span data-stu-id="1da6d-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="1da6d-108">Il crée un affichage des dossiers de l’interpréteur de commandes qui affiche le contenu du dossier dans l’un des cinq formats suivants : petite icône, grande icône, liste, détails ou miniature.</span><span class="sxs-lookup"><span data-stu-id="1da6d-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="1da6d-109">Elle n’est pas valide en dehors d’une WebView.</span><span class="sxs-lookup"><span data-stu-id="1da6d-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="1da6d-110">Les méthodes et propriétés exposées par **WebViewFolderContents** sont identiques à celles de l’objet [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .</span><span class="sxs-lookup"><span data-stu-id="1da6d-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="1da6d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1da6d-111">Members</span></span>

<span data-ttu-id="1da6d-112">L’objet **WebViewFolderContents** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1da6d-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="1da6d-113">Événements</span><span class="sxs-lookup"><span data-stu-id="1da6d-113">Events</span></span>](#events)
-   [<span data-ttu-id="1da6d-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1da6d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="1da6d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1da6d-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="1da6d-116">Événements</span><span class="sxs-lookup"><span data-stu-id="1da6d-116">Events</span></span>

<span data-ttu-id="1da6d-117">L’objet **WebViewFolderContents** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="1da6d-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="1da6d-118">Événement</span><span class="sxs-lookup"><span data-stu-id="1da6d-118">Event</span></span>                                                              | <span data-ttu-id="1da6d-119">Description</span><span class="sxs-lookup"><span data-stu-id="1da6d-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1da6d-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="1da6d-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="1da6d-121">Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1da6d-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="1da6d-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1da6d-122">Methods</span></span>

<span data-ttu-id="1da6d-123">L’objet **WebViewFolderContents** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1da6d-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="1da6d-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="1da6d-124">Method</span></span>                                                       | <span data-ttu-id="1da6d-125">Description</span><span class="sxs-lookup"><span data-stu-id="1da6d-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1da6d-126">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="1da6d-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="1da6d-127">Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1da6d-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="1da6d-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="1da6d-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="1da6d-129">Obtient un objet [**FolderItems**](../shell/folderitems.md) qui représente tous les éléments sélectionnés dans la vue.</span><span class="sxs-lookup"><span data-stu-id="1da6d-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="1da6d-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="1da6d-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="1da6d-131">Définit l’état de sélection d’un élément dans la vue.</span><span class="sxs-lookup"><span data-stu-id="1da6d-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="1da6d-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1da6d-132">Properties</span></span>

<span data-ttu-id="1da6d-133">L’objet **WebViewFolderContents** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1da6d-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="1da6d-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="1da6d-134">Property</span></span>                                                            | <span data-ttu-id="1da6d-135">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1da6d-135">Access type</span></span>          | <span data-ttu-id="1da6d-136">Description</span><span class="sxs-lookup"><span data-stu-id="1da6d-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1da6d-137">**Application**</span><span class="sxs-lookup"><span data-stu-id="1da6d-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="1da6d-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1da6d-138">Read-only</span></span><br/> | <span data-ttu-id="1da6d-139">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="1da6d-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1da6d-140">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="1da6d-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="1da6d-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1da6d-141">Read-only</span></span><br/> | <span data-ttu-id="1da6d-142">Obtient un objet [**FolderItem**](../shell/folderitem.md) qui représente l’élément ayant le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1da6d-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="1da6d-143">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="1da6d-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="1da6d-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1da6d-144">Read-only</span></span><br/> | <span data-ttu-id="1da6d-145">Obtient un objet [**dossier**](../shell/folder.md) qui représente la vue.</span><span class="sxs-lookup"><span data-stu-id="1da6d-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="1da6d-146">**Parent**</span><span class="sxs-lookup"><span data-stu-id="1da6d-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="1da6d-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1da6d-147">Read-only</span></span><br/> | <span data-ttu-id="1da6d-148">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="1da6d-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1da6d-149">**Script**</span><span class="sxs-lookup"><span data-stu-id="1da6d-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="1da6d-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1da6d-150">Read-only</span></span><br/> | <span data-ttu-id="1da6d-151">Obtient l’objet de script pour la vue.</span><span class="sxs-lookup"><span data-stu-id="1da6d-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1da6d-152">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="1da6d-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="1da6d-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1da6d-153">Read-only</span></span><br/> | <span data-ttu-id="1da6d-154">Obtient un jeu d’indicateurs [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) qui indiquent les options actuelles de la vue.</span><span class="sxs-lookup"><span data-stu-id="1da6d-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1da6d-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1da6d-155">Requirements</span></span>



| <span data-ttu-id="1da6d-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1da6d-156">Requirement</span></span> | <span data-ttu-id="1da6d-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="1da6d-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1da6d-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da6d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="1da6d-159">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1da6d-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1da6d-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da6d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="1da6d-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1da6d-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1da6d-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="1da6d-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="1da6d-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da6d-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1da6d-164">MIDL</span><span class="sxs-lookup"><span data-stu-id="1da6d-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1da6d-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1da6d-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1da6d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="1da6d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1da6d-167"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1da6d-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

