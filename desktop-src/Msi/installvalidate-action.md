---
description: L’action InstallValidate vérifie que tous les volumes auxquels le coût a été attribué disposent d’un espace suffisant pour l’installation. L’action InstallValidate met fin à l’installation en cas d’erreur irrécupérable si un volume manque d’espace disque.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Action InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210050"
---
# <a name="installvalidate-action"></a>Action InstallValidate

L’action InstallValidate vérifie que tous les [*volumes*](v-gly.md) auxquels le [*coût*](c-gly.md) a été attribué disposent d’un espace suffisant pour l’installation. L’action InstallValidate met fin à l’installation en cas d’erreur irrécupérable si un volume manque d’espace disque.

L’action InstallValidate avertit également l’utilisateur si un ou plusieurs fichiers à remplacer ou à supprimer sont en cours d’utilisation par un processus actif. Pour plus d’informations, consultez [redémarrages du système](system-reboots.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [CostFinalize](costfinalize-action.md) et les séquences de la boîte de dialogue d’interface utilisateur qui permettent à l’utilisateur de modifier les États et/ou les répertoires de sélection doivent être séquencées avant l’action InstallValidate.

Les [actions personnalisées](custom-actions.md) qui modifient l’état d’installation des fonctionnalités ou des composants doivent être séquencées avant l’action InstallValidate.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

En règle générale, une séquence antérieure de la boîte de dialogue d’interface utilisateur doit effectuer la même vérification que l’action InstallValidate quand l’utilisateur tente d’initier la copie des fichiers. La boîte de dialogue de l’interface utilisateur doit présenter un **espace disque** insuffisant si les volumes sélectionnés ne disposent pas de suffisamment d’espace pour l’installation. Les boîtes de dialogue de l’interface utilisateur doivent être créées de manière à empêcher l’utilisateur de poursuivre l’installation si l’espace disque est insuffisant. Dans le cas d’une installation silencieuse, il n’y a pas d’interface utilisateur et l’action InstallValidate met fin à l’installation si l’espace disque est insuffisant. La cause de l’arrêt prématuré est enregistrée dans le fichier journal si la journalisation est activée.

Une entrée est ajoutée à une table FilesInUse interne si un fichier est remplacé ou supprimé pendant qu’elle est ouverte pour l’exécution ou la modification par n’importe quel processus pendant le [*coût*](c-gly.md)du fichier. La table FilesInUse contient des colonnes pour le nom et le chemin d’accès complet du fichier. Lorsque l’action InstallValidate s’exécute, le programme d’installation interroge la table FilesInUse pour les entrées et détermine le nom du processus à l’aide du fichier. L’action InstallValidate ajoute un enregistrement à la table de l’interface utilisateur [ListBox](listbox-table.md) pour chaque processus unique identifié par cette requête. L’enregistrement contient les valeurs suivantes dans chaque colonne :

**Propriété**: FileInUseProcess

 

**Valeur**: *nom du processus*

 

**Text**: *texte contenu dans la légende de la fenêtre principale du processus* .

L’action InstallValidate affiche ensuite la boîte **de dialogue fichiers en cours d’utilisation** . Cette boîte de dialogue affiche les processus qui doivent être arrêtés pour éviter de devoir redémarrer le système pour remplacer les fichiers en cours d’utilisation.

L’action InstallValidate interroge la table de [boîte de dialogue](dialog-table.md) pour obtenir une boîte de dialogue créée avec la boîte de dialogue nom réservé [FilesInUse](filesinuse-dialog.md) et l’affiche. Cette boîte de dialogue doit contenir un contrôle [ListBox](listbox-control.md) lié à une propriété nommée FileInUseProcess. Par Convention, cette boîte de dialogue comporte un bouton **quitter**, **Réessayer** ou **Ignorer** , mais il s’agit de l’auteur de l’interface utilisateur. Chaque bouton doit être lié à un ControlEvent, [EndDialog](enddialog-controlevent.md) dans la table [ControlEvent,](controlevent-table.md) . L’action InstallValidate répond comme suit à la valeur retournée par l' [action](doaction-controlevent.md) ControlEvent,, comme indiqué par l’un de ces arguments [EndDialog](enddialog-controlevent.md) associé au bouton envoyé par l’utilisateur :

**Nouvelle tentative**: toutes les valeurs ajoutées à la table [ListBox](listbox-table.md) sont effacées, et la procédure de [*coût*](c-gly.md) de fichier tout entière est répétée, en revérifiant les fichiers qui sont toujours en cours d’utilisation. Si un ou plusieurs processus sont toujours identifiés comme utilisant des fichiers à remplacer ou à supprimer, le processus se répète. Sinon, InstallValidate retourne le contrôle au programme d’installation avec l’État msiDoActionStatusSuccess.

**Exit**: l’action InstallValidate retourne immédiatement le contrôle au programme d’installation avec l’État msiDoActionStatusUserExit. Cela met fin à l’installation.

**Toute autre valeur de retour**: l’action InstallValidate retourne immédiatement le contrôle au programme d’installation avec l’État msiDoActionStatusSuccess. Dans ce cas, étant donné qu’un ou plusieurs fichiers sont toujours en cours d’utilisation, les actions [InstallFiles](installfiles-action.md) et/ou [InstallAdminPackage](installadminpackage-action.md) suivantes doivent planifier le remplacement ou la suppression des fichiers en cours d’utilisation lors du redémarrage du système.

S’il n’existe aucune table de [zone de liste](listbox-table.md) dans la base de données, InstallValidate s’arrête en mode silencieux sans erreur.

Le point-virgule est le délimiteur de liste des transformations, des sources et des correctifs, et ne doit pas être utilisé dans ces noms de fichiers ou chemins d’accès.

Les fichiers marqués en lecture seule dans un emplacement en lecture seule ne sont jamais considérés comme en cours d’utilisation par le programme d’installation.

La boîte **de dialogue espace de l’espace disque** par défaut contenant les boutons **abandonner** et **Réessayer** est présentée à l’utilisateur si le niveau d’interface utilisateur est de base.

 

 



