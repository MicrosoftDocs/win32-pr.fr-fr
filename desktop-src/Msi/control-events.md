---
description: Un ControlEvent, spécifie une action à entreprendre par le programme d’installation ou une modification des attributs d’un ou plusieurs contrôles dans une boîte de dialogue. Pour plus d’informations sur ControlEvents, consultez vue d’ensemble de ControlEvent,.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Événements de contrôle (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221e8d9e6a8cea9a02b303040d06da346800912e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543715"
---
# <a name="control-events-windows-installer"></a>Événements de contrôle (Windows Installer)

Un ControlEvent, spécifie une action à entreprendre par le programme d’installation ou une modification des attributs d’un ou plusieurs contrôles dans une boîte de dialogue. Pour plus d’informations sur ControlEvents, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).

Le tableau suivant fournit des liens vers des informations supplémentaires sur les ControlEvents spécifiques.



| Événement de contrôle                                                       | Brève description de ControlEvent,                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Publie des données sur la dernière action.                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | Publie le nom de l’action présente.                                                                                                                                                                     |
| [AddLocal](addlocal-controlevent.md)                               | Indique au programme d’installation d’exécuter des fonctionnalités localement.                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | Indique au programme d’installation d’exécuter des fonctionnalités à partir de leur source.                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | Indique au programme d’installation de vérifier que le chemin d’accès peut être écrit.                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | Notifie le programme d’installation de vérifier que le chemin d’accès est valide.                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | Avertit le contrôle DirectoryList de la création d’un nouveau dossier.                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | Sélectionne le répertoire dans le contrôle DirectoryList.                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | Notifie le contrôle DirectoryList de sélectionner le parent du répertoire actuel.                                                                                                                             |
| [Action](doaction-controlevent.md)                               | La boîte de dialogue notifie le programme d’installation de l’exécution d’une action personnalisée.                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | Utilisé pour désactiver et activer les fonctionnalités de restauration.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Notifie le programme d’installation de la suppression d’une boîte de dialogue modale.                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | Publié par le contrôle DirectoryList lorsqu’un dossier est mis en surbrillance mais pas ouvert.                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | Cet événement de contrôle exécute un fichier spécifié. **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                                                       |
| [MsiPrint](msiprint-controlevent.md)                               | Permet à l’utilisateur d’imprimer le contenu du [contrôle ScrollableText](scrollabletext-control.md). **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/> |
| [NewDialog](newdialog-controlevent.md)                             | Notifie le programme d’installation de modifier une boîte de dialogue modale dans une autre boîte de dialogue.                                                                                                                                  |
| [Réinstallation](reinstall-controlevent.md)                             | Lance une réinstallation des fonctionnalités.                                                                                                                                                                       |
| [ReinstallMode](reinstallmode-controlevent.md)                     | Spécifie le mode de validation lors d’une réinstallation.                                                                                                                                                        |
| [Remove](remove-controlevent.md)                                   | Notifie le programme d’installation lorsque des fonctionnalités sont sélectionnées pour la suppression.                                                                                                                                                |
| [Réinitialiser](reset-controlevent.md)                                     | Rétablit les valeurs par défaut de toutes les valeurs de propriété utilisées lors de la création de la boîte de dialogue.                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | Utilisez le [Gestionnaire de redémarrage](/windows/desktop/RstMgr/restart-manager-portal) pour arrêter toutes les applications qui ont des fichiers en cours d’utilisation et les redémarrer à la fin de l’installation.                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | Affiche une chaîne pendant la compilation du script d’exécution.                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | Publié par SelectionTree pour décrire un élément.                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | Publié par SelectionTree pour générer une boîte de dialogue.                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | Publié par SelectionTree pour fournir une chaîne dans le champ Description de la table de fonctionnalités.                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | Utilisé par SelectionTree pour supprimer du texte ou désactiver des boutons.                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | Publié par SelectionTree pour fournir le chemin d’accès d’un élément.                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | Publié par SelectionTree pour indiquer si un chemin d’accès est associé à une fonctionnalité.                                                                                                                     |
| [Options de sélection](selectionsize-controlevent.md)                     | Publié par le contrôle SelectionTree pour fournir la taille d’un élément.                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | Le programme d’installation modifie le niveau d’installation à une valeur spécifiée.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Publié par le programme d’installation pour assurer la progression de l’installation.                                                                                                                                                  |
| [setProperty](setproperty-controlevent.md)                         | Définit une propriété spécifiée.                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | Notifie le programme d’installation de la vérification et de la définition d’un chemin d’accès.                                                                                                                                                               |
| [SpawnDialog](spawndialog-controlevent.md)                         | Notifie le programme d’installation de créer un enfant d’une zone modale.                                                                                                                                                      |
| [SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | Déclenche une boîte de dialogue spécifiée.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Publié par le programme d’installation pour fournir le temps restant dans la séquence de progression.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Définit ProductID sur l’ID de produit complet.                                                                                                                                                                        |



 

 

