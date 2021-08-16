---
description: cette section décrit les objets Windows implémentés par l’interpréteur de commandes.
title: Objets Shell pour l’écriture de scripts et Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bd2c924d9b66194c8f016fc8b1c16bed8a7e3c62f82e3673837e0e31c8563fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858798"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Objets Shell pour l’écriture de scripts et Microsoft Visual Basic

cette section décrit les objets Windows implémentés par l’interpréteur de commandes.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br/></td>
<td>Permet à un client de gérer les paramètres de quota de disque global d’un volume NTFS. cet objet rend les fonctionnalités essentielles de l’interface <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Permet à un administrateur de gérer les propriétés de quota de disque d’un volume. Le système de fichiers NTFS permet à un administrateur de gérer l’utilisation du disque sur un volume partagé en allouant une quantité d’espace disque spécifiée ou une <em>limite de quota</em>à chaque utilisateur. Vous pouvez utiliser cet objet pour définir la limite de quota par défaut qui sera automatiquement affectée à tous les nouveaux utilisateurs.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Reçoit les événements d’inscription de la fenêtre <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Dossier</strong></a><br/></td>
<td>Représente un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le dossier.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Dossier2</strong></a><br/></td>
<td>Étend l’objet <a href="folder.md"><strong>Folder</strong></a> pour prendre en charge les dossiers hors connexion.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Représente un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur l’élément.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Représente la collection d’éléments dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Étend l’objet <a href="folderitems.md"><strong>FolderItems</strong></a> . Il prend en charge une méthode supplémentaire.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Étend l’objet <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> . Cet objet prend en charge une méthode et une propriété supplémentaires.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Représente un verbe unique disponible pour un élément. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le verbe.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Représente la collection de verbes pour un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Représente un objet dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Étend l’objet <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> avec diverses nouvelles fonctionnalités. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Étend l’objet <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> . <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> prend en charge une nouvelle méthode en plus des propriétés et des méthodes prises en charge par <strong>IShellDispatch2</strong>. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Étend l’objet <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> . Outre les propriétés et les méthodes prises en charge par <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> prend en charge quatre méthodes supplémentaires. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Étend l’objet <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> . En plus des propriétés et des méthodes prises en charge par <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> ajoute une méthode qui affiche les fenêtres ouvertes dans une pile 3D. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Étend l’objet <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> . En plus des propriétés et des méthodes prises en charge par <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> ajoute une méthode qui affiche le volet de recherche applications. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> est implémenté et accessible via l’objet <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Étend l’objet <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> et prend en charge une propriété supplémentaire.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Étend l’objet <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> en activant les pages côté serveur hébergées dans un Assistant pour vérifier que l’utilisateur a été authentifié par le biais d’un compte Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Représente les objets dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Étend l’objet <a href="folderitem.md"><strong>FolderItem</strong></a> . En plus des propriétés et des méthodes prises en charge par <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> a deux méthodes supplémentaires.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Représente les objets dans une vue et fournit des propriétés et des méthodes utilisées pour obtenir des informations sur le contenu de la vue.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Transfère les événements déclenchés par un objet <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> spécifié aux gestionnaires d’événements <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondants.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Gère les liens de l’interpréteur de commandes. Cet objet permet d’accéder à la plupart des fonctionnalités de l’interface <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> pour la script des applications. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>implémenté par le shell pour aider les développeurs à écrire des scripts et Visual Basic utiliser certaines des fonctionnalités disponibles dans l’interpréteur de commandes. L’objet <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> n’a pas de propriétés ou d’événements. Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Représente une collection des fenêtres ouvertes qui appartiennent au shell. Les méthodes associées à ces objets peuvent contrôler et exécuter des commandes dans l’interpréteur de commandes, et obtenir d’autres objets liés à l’interpréteur de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Expose des méthodes qui activent des pages HTML hébergées dans une extension d’Assistant pour communiquer avec l’Assistant.<br/></td>
</tr>
</tbody>
</table>



 

 

 




