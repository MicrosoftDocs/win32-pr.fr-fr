---
description: vous pouvez fournir toutes les informations nécessaires pour configurer ajout/suppression de programmes dans le panneau de configuration en définissant les valeurs de certaines propriétés du programme d’installation dans le package Windows Installer de votre application.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: configuration de l’ajout/suppression de programmes avec Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99e1393eb586cfe1067840e4622fddd777a84512f55f9e82f7c9fad3b1f5688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638748"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>configuration de l’ajout/suppression de programmes avec Windows Installer

vous pouvez fournir toutes les informations nécessaires pour configurer ajout/suppression de programmes dans le panneau de configuration en définissant les valeurs de certaines propriétés du programme d’installation dans le package Windows Installer de votre application. La définition de ces propriétés écrit automatiquement les valeurs correspondantes dans le registre. Si le programme d’installation détecte que le produit est marqué pour une suppression complète, les opérations sont automatiquement ajoutées au script pour supprimer le dossier ajout/suppression de programmes dans les informations du panneau de configuration du produit.

Si une application n’est pas inscrite, elle n’est pas répertoriée dans Ajout/suppression de programmes dans le panneau de configuration. Pour plus d’informations, consultez [Ajout et suppression d’une application et conservation d’aucune trace dans le registre](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Les applications qui ont été installées dans le [contexte d’installation](installation-context.md) par utilisateur s’affichent dans Ajout/suppression de programmes de l’utilisateur actuel. Les applications qui ont été installées dans le contexte d’installation par ordinateur sont affichées dans Ajout/suppression de programmes de tous les utilisateurs. Les applications qui n’ont pas été installées par ordinateur et qui n’ont été installées qu’en tant qu’applications par utilisateur pour les utilisateurs autres que l’utilisateur actuel, n’apparaissent pas dans Ajout/suppression de programmes de l’utilisateur actuel.

Notez que les packages d’installation qui utilisent la propriété [**LIMITUI**](limitui.md) doivent également contenir [**ARPNOMODIFY**](arpnomodify.md). Cela est nécessaire pour qu’un utilisateur obtienne le comportement correct à partir de l’utilitaire ajout/suppression de programmes dans le panneau de configuration lors de la tentative de configuration d’un produit.

Le programme d’installation utilise les [propriétés publiques](public-properties.md) suivantes pour gérer ajout/suppression de programmes dans le panneau de configuration.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom de la propriété</th>
<th>Brève description de la propriété</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></td>
<td>URL du canal de mise à jour pour l’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Fournit des commentaires pour l’ajout/suppression de programmes dans le panneau de configuration. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Fournit le contact pour ajout/suppression de programmes dans le panneau de configuration. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Chemin d’accès complet au dossier principal de l’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Adresse Internet, ou URL, pour le support technique. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Numéros de téléphone du support technique. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Empêche l’affichage d’un bouton modifier pour le produit dans Ajout/suppression de programmes dans le panneau de configuration.
<blockquote>
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Empêche l’affichage d’un bouton Supprimer pour le produit dans Ajout/suppression de programmes dans le panneau de configuration. Le produit peut toujours être supprimé en sélectionnant le bouton modifier si le package d’installation a été créé avec une interface utilisateur qui permet de supprimer le produit en tant qu’option.
<blockquote>
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Désactive le bouton réparer dans Ajout/suppression de programmes dans le panneau de configuration.
<blockquote>
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifie l’icône affichée dans Ajout/suppression de programmes. Si cette propriété n’est pas définie, ajout/suppression de programmes spécifie l’icône d’affichage.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Contient le fichier Lisez-moi pour ajout/suppression de programmes dans le panneau de configuration. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Estimation de la taille de l’application en Ko.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Empêche l’affichage de l’application dans la liste des programmes du panneau de configuration Ajout/suppression de programmes.
<blockquote>
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>URL de la page d’hébergement de l’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>URL pour les informations de mise à jour d’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Pour plus d’informations sur l’outil définir le programme et les valeurs par défaut, reportez-vous à la section [utilisation des paramètres par défaut de l’accès aux programmes et](/previous-versions//bb776877(v=vs.85))de l’ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Désinstaller la clé de Registre](uninstall-registry-key.md)
</dt> </dl>
