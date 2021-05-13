---
description: Transfère les événements déclenchés par un objet ShellFolderView spécifié aux gestionnaires d’événements ShellFolderViewOC correspondants.
title: Objet ShellFolderViewOC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840870"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="dcc34-103">Objet ShellFolderViewOC</span><span class="sxs-lookup"><span data-stu-id="dcc34-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="dcc34-104">Transfère les événements déclenchés par un objet [**ShellFolderView**](shellfolderview.md) spécifié aux gestionnaires d’événements **ShellFolderViewOC** correspondants.</span><span class="sxs-lookup"><span data-stu-id="dcc34-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="dcc34-105">Membres</span><span class="sxs-lookup"><span data-stu-id="dcc34-105">Members</span></span>

<span data-ttu-id="dcc34-106">L’objet **ShellFolderViewOC** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dcc34-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="dcc34-107">Événements</span><span class="sxs-lookup"><span data-stu-id="dcc34-107">Events</span></span>](#events)
-   [<span data-ttu-id="dcc34-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dcc34-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="dcc34-109">Événements</span><span class="sxs-lookup"><span data-stu-id="dcc34-109">Events</span></span>

<span data-ttu-id="dcc34-110">L’objet **ShellFolderViewOC** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="dcc34-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="dcc34-111">Événement</span><span class="sxs-lookup"><span data-stu-id="dcc34-111">Event</span></span>                                                          | <span data-ttu-id="dcc34-112">Description</span><span class="sxs-lookup"><span data-stu-id="dcc34-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcc34-113">**EnumDone**</span><span class="sxs-lookup"><span data-stu-id="dcc34-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="dcc34-114">Indique que l’objet [**ShellFolderView**](shellfolderview.md) a terminé l’énumération du contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="dcc34-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="dcc34-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="dcc34-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="dcc34-116">Indique que l’état de sélection d’un ou plusieurs éléments de la vue a changé.</span><span class="sxs-lookup"><span data-stu-id="dcc34-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="dcc34-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dcc34-117">Methods</span></span>

<span data-ttu-id="dcc34-118">L’objet **ShellFolderViewOC** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dcc34-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="dcc34-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="dcc34-119">Method</span></span>                                                   | <span data-ttu-id="dcc34-120">Description</span><span class="sxs-lookup"><span data-stu-id="dcc34-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcc34-121">**SetFolderView**</span><span class="sxs-lookup"><span data-stu-id="dcc34-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="dcc34-122">Transfère les événements de l’objet [**ShellFolderView**](shellfolderview.md) spécifié au gestionnaire d’événements **ShellFolderViewOC** correspondant.</span><span class="sxs-lookup"><span data-stu-id="dcc34-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcc34-123">Notes</span><span class="sxs-lookup"><span data-stu-id="dcc34-123">Remarks</span></span>

<span data-ttu-id="dcc34-124">L’objet [**ShellFolderView**](shellfolderview.md) déclenche deux événements, [**EnumDone**](shellfolderviewoc-enumdone.md) et [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), qui sont généralement gérés par des applications.</span><span class="sxs-lookup"><span data-stu-id="dcc34-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="dcc34-125">Toutefois, certaines applications doivent gérer les événements d’une série d’objets **ShellFolderView** .</span><span class="sxs-lookup"><span data-stu-id="dcc34-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="dcc34-126">Par exemple, une application peut héberger un contrôle WebBrowser qui permet aux utilisateurs de naviguer dans une série de dossiers.</span><span class="sxs-lookup"><span data-stu-id="dcc34-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="dcc34-127">Chaque dossier a son propre objet **ShellFolderView** avec ses événements associés.</span><span class="sxs-lookup"><span data-stu-id="dcc34-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="dcc34-128">La gestion de ces événements peut être difficile.</span><span class="sxs-lookup"><span data-stu-id="dcc34-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="dcc34-129">L’objet **ShellFolderViewOC** simplifie la gestion des événements pour de tels scénarios.</span><span class="sxs-lookup"><span data-stu-id="dcc34-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="dcc34-130">Elle permet aux applications de gérer des événements pour tous les objets [**ShellFolderView**](shellfolderview.md) avec une seule paire de gestionnaires d’événements **ShellFolderViewOC** .</span><span class="sxs-lookup"><span data-stu-id="dcc34-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="dcc34-131">Chaque fois que l’utilisateur accède à un nouveau dossier, l’application transmet l’objet **ShellFolderView** associé à l’objet **ShellFolderViewOC** en appelant [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span><span class="sxs-lookup"><span data-stu-id="dcc34-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="dcc34-132">Ensuite, lorsqu’un événement [**EnumDone**](shellfolderviewoc-enumdone.md) ou [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) est déclenché, l’objet **ShellFolderViewOC** transfère l’événement à son propre gestionnaire de traitement.</span><span class="sxs-lookup"><span data-stu-id="dcc34-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc34-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dcc34-133">Requirements</span></span>



| <span data-ttu-id="dcc34-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcc34-134">Requirement</span></span> | <span data-ttu-id="dcc34-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcc34-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc34-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc34-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc34-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcc34-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcc34-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc34-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc34-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcc34-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dcc34-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcc34-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc34-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc34-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dcc34-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="dcc34-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcc34-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcc34-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dcc34-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc34-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc34-145"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc34-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcc34-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcc34-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc34-147">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="dcc34-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




