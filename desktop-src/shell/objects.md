---
description: Cette section décrit les objets Windows implémentés par l’interpréteur de commandes.
title: Objets Shell pour l’écriture de scripts et Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529422"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="48bd0-103">Objets Shell pour l’écriture de scripts et Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="48bd0-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="48bd0-104">Cette section décrit les objets Windows implémentés par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="48bd0-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="48bd0-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48bd0-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="48bd0-106">Topic</span></span></th>
<th><span data-ttu-id="48bd0-107">Description</span><span class="sxs-lookup"><span data-stu-id="48bd0-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48bd0-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-109">Permet à un client de gérer les paramètres de quota de disque global d’un volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="48bd0-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="48bd0-110">Cet objet rend les fonctionnalités essentielles de l’interface <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="48bd0-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-112">Permet à un administrateur de gérer les propriétés de quota de disque d’un volume.</span><span class="sxs-lookup"><span data-stu-id="48bd0-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="48bd0-113">Le système de fichiers NTFS permet à un administrateur de gérer l’utilisation du disque sur un volume partagé en allouant une quantité d’espace disque spécifiée ou une <em>limite de quota</em>à chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48bd0-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="48bd0-114">Vous pouvez utiliser cet objet pour définir la limite de quota par défaut qui sera automatiquement affectée à tous les nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="48bd0-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-116">Reçoit les événements d’inscription de la fenêtre <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-117"><a href="folder.md"><strong>Dossier</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-118">Représente un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-118">Represents a Shell folder.</span></span> <span data-ttu-id="48bd0-119">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="48bd0-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-120"><a href="folder2-object.md"><strong>Dossier2</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-121">Étend l’objet <a href="folder.md"><strong>Folder</strong></a> pour prendre en charge les dossiers hors connexion.</span><span class="sxs-lookup"><span data-stu-id="48bd0-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-123">Représente un élément dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="48bd0-124">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="48bd0-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-126">Représente la collection d’éléments dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="48bd0-127">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.</span><span class="sxs-lookup"><span data-stu-id="48bd0-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-129">Étend l’objet <a href="folderitems.md"><strong>FolderItems</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="48bd0-130">Il prend en charge une méthode supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="48bd0-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-132">Étend l’objet <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="48bd0-133">Cet objet prend en charge une méthode et une propriété supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="48bd0-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-135">Représente un verbe unique disponible pour un élément.</span><span class="sxs-lookup"><span data-stu-id="48bd0-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="48bd0-136">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le verbe.</span><span class="sxs-lookup"><span data-stu-id="48bd0-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-138">Représente la collection de verbes pour un élément dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="48bd0-139">Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.</span><span class="sxs-lookup"><span data-stu-id="48bd0-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-141">Représente un objet dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-141">Represents an object in the Shell.</span></span> <span data-ttu-id="48bd0-142">Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="48bd0-143">Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="48bd0-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-146">Étend l’objet <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> avec diverses nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="48bd0-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="48bd0-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-149">Étend l’objet <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="48bd0-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> prend en charge une nouvelle méthode en plus des propriétés et des méthodes prises en charge par <strong>IShellDispatch2</strong>.</span><span class="sxs-lookup"><span data-stu-id="48bd0-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="48bd0-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-153">Étend l’objet <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="48bd0-154">Outre les propriétés et les méthodes prises en charge par <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> prend en charge quatre méthodes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="48bd0-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="48bd0-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-157">Étend l’objet <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="48bd0-158">En plus des propriétés et des méthodes prises en charge par <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> ajoute une méthode qui affiche les fenêtres ouvertes dans une pile 3D.</span><span class="sxs-lookup"><span data-stu-id="48bd0-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="48bd0-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-161">Étend l’objet <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="48bd0-162">En plus des propriétés et des méthodes prises en charge par <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> ajoute une méthode qui affiche le volet de recherche applications.</span><span class="sxs-lookup"><span data-stu-id="48bd0-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="48bd0-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-165">Étend l’objet <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> et prend en charge une propriété supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="48bd0-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-167">Étend l’objet <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> en activant les pages côté serveur hébergées dans un Assistant pour vérifier que l’utilisateur a été authentifié par le biais d’un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48bd0-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-168"><a href="shell.md"><strong>Shell</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-169">Représente les objets dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="48bd0-170">Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="48bd0-171">Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-173">Étend l’objet <a href="folderitem.md"><strong>FolderItem</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48bd0-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="48bd0-174">En plus des propriétés et des méthodes prises en charge par <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> a deux méthodes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="48bd0-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-176">Représente les objets dans une vue et fournit des propriétés et des méthodes utilisées pour obtenir des informations sur le contenu de la vue.</span><span class="sxs-lookup"><span data-stu-id="48bd0-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-178">Transfère les événements déclenchés par un objet <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> spécifié aux gestionnaires d’événements <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondants.</span><span class="sxs-lookup"><span data-stu-id="48bd0-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-180">Gère les liens de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-180">Manages Shell links.</span></span> <span data-ttu-id="48bd0-181">Cet objet permet d’accéder à la plupart des fonctionnalités de l’interface <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> pour la script des applications.</span><span class="sxs-lookup"><span data-stu-id="48bd0-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-183">Implémenté par le Shell pour aider les développeurs à écrire des scripts et Visual Basic utiliser certaines des fonctionnalités disponibles dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="48bd0-184">L’objet <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> n’a pas de propriétés ou d’événements.</span><span class="sxs-lookup"><span data-stu-id="48bd0-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="48bd0-185">Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48bd0-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-187">Représente une collection des fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="48bd0-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="48bd0-188">Les méthodes associées à ces objets peuvent contrôler et exécuter des commandes dans l’interpréteur de commandes, et obtenir d’autres objets liés à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bd0-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48bd0-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="48bd0-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="48bd0-190">Expose des méthodes qui activent des pages HTML hébergées dans une extension d’Assistant pour communiquer avec l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="48bd0-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




