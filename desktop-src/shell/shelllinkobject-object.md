---
description: Gère les liens de l’interpréteur de commandes. Cet objet permet d’accéder à la plupart des fonctionnalités de l’interface IShellLink pour la script des applications.
title: Objet ShellLinkObject (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973738"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="0dda5-104">Objet ShellLinkObject</span><span class="sxs-lookup"><span data-stu-id="0dda5-104">ShellLinkObject object</span></span>

<span data-ttu-id="0dda5-105">Gère les liens de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="0dda5-105">Manages Shell links.</span></span> <span data-ttu-id="0dda5-106">Cet objet permet d’accéder à la plupart des fonctionnalités de l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) pour la script des applications.</span><span class="sxs-lookup"><span data-stu-id="0dda5-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="0dda5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0dda5-107">Members</span></span>

<span data-ttu-id="0dda5-108">L’objet **ShellLinkObject** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0dda5-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="0dda5-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0dda5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0dda5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0dda5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0dda5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0dda5-111">Methods</span></span>

<span data-ttu-id="0dda5-112">L’objet **ShellLinkObject** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0dda5-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="0dda5-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="0dda5-113">Method</span></span>                                                     | <span data-ttu-id="0dda5-114">Description</span><span class="sxs-lookup"><span data-stu-id="0dda5-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dda5-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="0dda5-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="0dda5-116">Obtient l’emplacement de l’icône assignée au lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="0dda5-117">**Résolution**</span><span class="sxs-lookup"><span data-stu-id="0dda5-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="0dda5-118">Recherche la cible d’un lien de Shell, même si la cible a été déplacée ou renommée.</span><span class="sxs-lookup"><span data-stu-id="0dda5-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="0dda5-119">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="0dda5-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="0dda5-120">Enregistre toutes les modifications apportées au lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="0dda5-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="0dda5-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="0dda5-122">Définit l’emplacement de l’icône assignée au lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="0dda5-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0dda5-123">Properties</span></span>

<span data-ttu-id="0dda5-124">L’objet **ShellLinkObject** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0dda5-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="0dda5-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="0dda5-125">Property</span></span>                                                                | <span data-ttu-id="0dda5-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0dda5-126">Access type</span></span>           | <span data-ttu-id="0dda5-127">Description</span><span class="sxs-lookup"><span data-stu-id="0dda5-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dda5-128">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="0dda5-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="0dda5-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0dda5-129">Read/write</span></span><br/> | <span data-ttu-id="0dda5-130">Contient les arguments d’un lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="0dda5-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="0dda5-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="0dda5-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0dda5-132">Read/write</span></span><br/> | <span data-ttu-id="0dda5-133">Obtient ou définit la description du lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="0dda5-134">**Touche d’accès rapide**</span><span class="sxs-lookup"><span data-stu-id="0dda5-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="0dda5-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0dda5-135">Read/write</span></span><br/> | <span data-ttu-id="0dda5-136">Obtient ou définit le raccourci clavier du lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="0dda5-137">**Path**</span><span class="sxs-lookup"><span data-stu-id="0dda5-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="0dda5-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0dda5-138">Read/write</span></span><br/> | <span data-ttu-id="0dda5-139">Obtient ou définit le chemin d’accès à l’objet de lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="0dda5-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="0dda5-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="0dda5-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0dda5-141">Read/write</span></span><br/> | <span data-ttu-id="0dda5-142">Obtient ou définit l’état d’affichage initial (dimensionné, réduit ou agrandi) de la commande du lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="0dda5-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="0dda5-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="0dda5-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0dda5-144">Read/write</span></span><br/> | <span data-ttu-id="0dda5-145">Obtient ou définit le répertoire de travail spécifié dans le lien.</span><span class="sxs-lookup"><span data-stu-id="0dda5-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="0dda5-146">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0dda5-146">Requirements</span></span>



| <span data-ttu-id="0dda5-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dda5-147">Requirement</span></span> | <span data-ttu-id="0dda5-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dda5-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dda5-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dda5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0dda5-150">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dda5-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0dda5-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dda5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0dda5-152">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dda5-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0dda5-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="0dda5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dda5-154"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dda5-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0dda5-155">MIDL</span><span class="sxs-lookup"><span data-stu-id="0dda5-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0dda5-156"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0dda5-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0dda5-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0dda5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dda5-158"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="0dda5-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dda5-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dda5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dda5-160">Liens de Shell</span><span class="sxs-lookup"><span data-stu-id="0dda5-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
