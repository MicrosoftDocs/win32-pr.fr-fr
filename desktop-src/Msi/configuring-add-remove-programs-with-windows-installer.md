---
description: vous pouvez fournir toutes les informations nécessaires pour configurer ajout/suppression de programmes dans le panneau de configuration en définissant les valeurs de certaines propriétés du programme d’installation dans le package Windows Installer de votre application.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: configuration de l’ajout/suppression de programmes avec Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48ad8499d395ffc4a5aad5491883f9c3161b78a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465486"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>configuration de l’ajout/suppression de programmes avec Windows Installer

vous pouvez fournir toutes les informations nécessaires pour configurer ajout/suppression de programmes dans le panneau de configuration en définissant les valeurs de certaines propriétés du programme d’installation dans le package Windows Installer de votre application. La définition de ces propriétés écrit automatiquement les valeurs correspondantes dans le registre. Si le programme d’installation détecte que le produit est marqué pour une suppression complète, les opérations sont automatiquement ajoutées au script pour supprimer le dossier ajout/suppression de programmes dans les informations du panneau de configuration du produit.

Si une application n’est pas inscrite, elle n’est pas répertoriée dans Ajout/suppression de programmes dans le panneau de configuration. Pour plus d’informations, consultez [Ajout et suppression d’une application et conservation d’aucune trace dans le registre](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Les applications qui ont été installées dans le [contexte d’installation](installation-context.md) par utilisateur s’affichent dans Ajout/suppression de programmes de l’utilisateur actuel. Les applications qui ont été installées dans le contexte d’installation par ordinateur sont affichées dans Ajout/suppression de programmes de tous les utilisateurs. Les applications qui n’ont pas été installées par ordinateur et qui n’ont été installées qu’en tant qu’applications par utilisateur pour les utilisateurs autres que l’utilisateur actuel, n’apparaissent pas dans Ajout/suppression de programmes de l’utilisateur actuel.

Notez que les packages d’installation qui utilisent la propriété [**LIMITUI**](limitui.md) doivent également contenir [**ARPNOMODIFY**](arpnomodify.md). Cela est nécessaire pour qu’un utilisateur obtienne le comportement correct à partir de l’utilitaire ajout/suppression de programmes dans le panneau de configuration lors de la tentative de configuration d’un produit.

Le programme d’installation utilise les [propriétés publiques](public-properties.md) suivantes pour gérer ajout/suppression de programmes dans le panneau de configuration.


| Nom de la propriété | Brève description de la propriété | 
|---------------|-------------------------------|
| <a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a> | URL du canal de mise à jour pour l’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a> | Fournit des commentaires pour l’ajout/suppression de programmes dans le panneau de configuration. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arpcontact.md"><strong>ARPCONTACT</strong></a> | Fournit le contact pour ajout/suppression de programmes dans le panneau de configuration. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a> | Chemin d’accès complet au dossier principal de l’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arphelplink.md"><strong>ARPHELPLINK</strong></a> | Adresse Internet, ou URL, pour le support technique. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a> | Numéros de téléphone du support technique. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a> | Empêche l’affichage d’un bouton modifier pour le produit dans Ajout/suppression de programmes dans le panneau de configuration.<blockquote><b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</blockquote><br /> | 
| <a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a> | Empêche l’affichage d’un bouton Supprimer pour le produit dans Ajout/suppression de programmes dans le panneau de configuration. Le produit peut toujours être supprimé en sélectionnant le bouton modifier si le package d’installation a été créé avec une interface utilisateur qui permet de supprimer le produit en tant qu’option.<blockquote><b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</blockquote><br /> | 
| <a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a> | Désactive le bouton réparer dans Ajout/suppression de programmes dans le panneau de configuration.<blockquote><b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</blockquote><br /> | 
| <a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a> | Identifie l’icône affichée dans Ajout/suppression de programmes. Si cette propriété n’est pas définie, ajout/suppression de programmes spécifie l’icône d’affichage. | 
| <a href="arpreadme.md"><strong>ARPREADME</strong></a> | Contient le fichier Lisez-moi pour ajout/suppression de programmes dans le panneau de configuration. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arpsize.md"><strong>ARPSIZE</strong></a> | Estimation de la taille de l’application en Ko. | 
| <a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a> | Empêche l’affichage de l’application dans la liste des programmes du panneau de configuration Ajout/suppression de programmes.<blockquote><b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP. la Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</blockquote><br /> | 
| <a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a> | URL de la page d’hébergement de l’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 
| <a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a> | URL pour les informations de mise à jour d’application. Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>. | 


> [!Note]  
> Pour plus d’informations sur l’outil définir le programme et les valeurs par défaut, reportez-vous à la section [utilisation des paramètres par défaut de l’accès aux programmes et](/previous-versions//bb776877(v=vs.85))de l’ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Désinstaller la clé de Registre](uninstall-registry-key.md)
</dt> </dl>
