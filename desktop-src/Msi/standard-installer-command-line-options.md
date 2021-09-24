---
description: Voici les options de ligne de commande standard pour le programme d’installation standard de Microsoft (Msiexec.exe), l’exécutable utilisé pour l’interprétation des packages et l’installation des programmes.
ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e
title: Options du programme d’installation standard de Microsoft Command-Line
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 8e3771975cee51e08c6b4686056f8a594a566f46
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521206"
---
# <a name="microsoft-standard-installer-command-line-options"></a>Options du programme d’installation standard de Microsoft Command-Line

Voici les options de ligne de commande standard pour le programme d’installation standard de Microsoft (Msiexec.exe), l’exécutable utilisé pour interpréter les packages et installer les produits.

Les options de ligne de commande ne respectent pas la casse.

Msiexec définit un niveau d’erreur au retour qui correspond aux [codes d’erreur système](../debug/system-error-codes.md).

> [!NOTE]
> les options de ligne de commande qui sont identifiées dans cette rubrique sont disponibles à partir de Windows Installer 3,0. les [Options de ligne de commande](command-line-options.md) Windows Installer sont disponibles avec Windows Installer 3,0 et versions antérieures.

## <a name="help"></a>/help

Aide et aide-mémoire. Affiche l’utilisation correcte de la commande d’installation, y compris la liste de tous les commutateurs et comportements. La description de l’utilisation peut être affichée dans l’interface utilisateur. Une utilisation incorrecte de toute option appelle cette option d’aide.

l’Option Command-Line Windows Installer équivalente est : `/?` .

### <a name="examples"></a>Exemples

`Msiexec /help`.

## <a name="quiet"></a>/quiet

Option Display quiet. Le programme d’installation exécute une installation sans afficher d’interface utilisateur. Aucune invite, aucun message ou boîte de dialogue n’est affiché à l’utilisateur. L’utilisateur ne peut pas annuler l’installation.

Utilisez les `/norestart` `/forcerestart` options de ligne de commande ou standard pour contrôler les redémarrages. Si aucune option de redémarrage n’est spécifiée, le programme d’installation redémarre l’ordinateur chaque fois que nécessaire sans afficher d’invite ou d’avertissement à l’utilisateur.

l’Option Command-Line Windows Installer équivalente est : `/qn` .

### <a name="examples"></a>Exemples

`Msiexec /package Application.msi /quiet`

`Msiexec /uninstall Application.msi /quiet`

`Msiexec /update msipatch.msp /quiet`

`Msiexec /uninstall msipatch.msp /package  Application.msi / quiet`

## <a name="passive"></a>/passive

Option d’affichage passif. Le programme d’installation affiche une barre de progression à l’utilisateur qui indique qu’une installation est en cours, mais aucune invite ni aucun message d’erreur ne s’affiche pour l’utilisateur. L’utilisateur ne peut pas annuler l’installation.

Utilisez les `/norestart` `/forcerestart` options de ligne de commande ou standard pour contrôler les redémarrages. Si aucune option de redémarrage n’est spécifiée, le programme d’installation redémarre l’ordinateur chaque fois que nécessaire sans afficher d’invite ou d’avertissement à l’utilisateur.

 l’Option Command-Line Windows Installer équivalente est : `/qb!` -with `REBOOTPROMPT=S` set sur la ligne de commande.

### <a name="examples"></a>Exemples
`msiexec /package Application.msi /passive`

## <a name="norestart"></a>/norestart
Option ne jamais redémarrer. Le programme d’installation ne redémarre jamais l’ordinateur après l’installation.

l’équivalent de la ligne de commande Windows Installer a `REBOOT=ReallySuppress` été défini sur la ligne de commande.

### <a name="examples"></a>Exemples
`msiexec /package Application.msi /norestart`.

## <a name="forcerestart"></a>/forcerestart

Option Always restart. Le programme d’installation redémarre toujours l’ordinateur après chaque installation.

l’équivalent de la ligne de commande Windows Installer a `REBOOT=Force` été défini sur la ligne de commande.

### <a name="examples"></a>Exemples

`msiexec /package Application.msi /forcerestart`

## <a name="promptrestart"></a>/promptrestart

Invite avant le redémarrage de l’option. Affiche un message indiquant qu’un redémarrage est nécessaire pour terminer l’installation et demande à l’utilisateur s’il faut redémarrer le système maintenant. Cette option ne peut pas être utilisée avec l'option `/quiet`.

l’équivalent de la ligne de commande Windows Installer a `REBOOTPROMPT = ""` été défini sur la ligne de commande.

## <a name="uninstall-product"></a>/Uninstall (produit)

Option de désinstallation du produit. Désinstalle un produit.

l’Option équivalente Command-Line Windows Installer est`/x.`

### <a name="parameters"></a>Paramètres

*<Package.msi| ProductCode>*


## <a name="uninstall-patch"></a>/Uninstall (patch)

Option de désinstallation de mise à jour. Désinstalle un correctif de mise à jour.

l’Option Command-Line Windows Installer équivalente est : `/I` avec `MSIPATCHREMOVE=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2]` set sur la ligne de commande.

### <a name="parameters"></a>Paramètres

*/package <Package.msi | ProductCode>/uninstall [; Update2. msp | PatchGUID2]*

## <a name="log"></a>/log

Option de journalisation. Écrit les informations de journalisation dans un fichier journal au niveau du chemin d’accès existant spécifié. Le chemin d’accès à l’emplacement du fichier journal doit déjà exister. Le programme d’installation ne crée pas la structure de répertoire pour le fichier journal.

pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez Windows Installer de [journalisation normale](normal-logging.md).  

l’Option Command-Line Windows Installer équivalente est : `/L*` .

Les informations suivantes sont entrées dans le journal :

- Messages d'état
- Avertissements récupérables
- Tous les messages d’erreur
- Démarrer des actions
- Enregistrements spécifiques aux actions
- Demandes de l’utilisateur
- Paramètres initiaux de l’interface utilisateur
- Informations de sortie insuffisantes ou irrécupérables
- Messages d’espace disque insuffisant
- Propriétés du terminal

## <a name="package"></a>/package

Option d’installation du produit. Installe ou configure un produit.

l’Option Command-Line Windows Installer équivalente est : `/I` .

### <a name="parameters"></a>Paramètres

*<Package.msi| ProductCode>*

## <a name="update"></a>/update

Option installer les correctifs. Installe un ou plusieurs correctifs.

l’équivalent de la ligne de commande Windows Installer contient PATCH = [msipatch. msp] < ; PatchGuid2> défini sur la ligne de commande.

### <a name="parameters"></a>Paramètres

*[; Update2. msp]*
