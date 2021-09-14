---
description: ControlEvents est analogue à Microsoft Windows messages dans les applications Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Présentation de ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091965"
---
# <a name="controlevent-overview"></a>Présentation de ControlEvent,

ControlEvents est analogue à Microsoft Windows messages dans les applications Win32. toutefois, au lieu de créer une fonction de rappel pour recevoir des messages Windows et envoyer des messages Windows avec la fonction [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , le programme d’installation de l’interface utilisateur et les contrôles publient [ControlEvents](control-events.md). D’autres contrôles et le programme d’installation peuvent être spécifiés pour s’abonner à un ControlEvents particulier qui modifie ensuite les attributs du contrôle d’abonnement. Pour ajouter des contrôles de travail aux boîtes de dialogue, l’auteur de l’interface utilisateur spécifie la publication de ControlEvents dans la [table ControlEvent,](controlevent-table.md) et abonne les contrôles à ControlEvents dans la [table EventMapping](eventmapping-table.md).

Le programme d’installation publiera les événements suivants sur les contrôles d’abonnement listés dans le [tableau EventMapping](eventmapping-table.md). Un contrôle [ProgressBar](progressbar-control.md) ou un contrôle de tableau [blanc](billboard-control.md) s’abonne généralement à SetProgress, le reste est abonné aux [contrôles de texte](text-control.md).

[ActionData ControlEvent,](actiondata-controlevent.md)

[ActionText ControlEvent,](actiontext-controlevent.md)

[SetProgress ControlEvent,](setprogress-controlevent.md)

[TimeRemaining ControlEvent,](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md)

Les événements suivants sont publiés par le contrôle lorsque la sélection de l’élément est déplacée dans un contrôle [SelectionTree](selectiontree-control.md) ou un [contrôle DirectoryList](directorylist-control.md). Les contrôles d’abonnement doivent se trouver dans la même boîte de dialogue et être listés dans le tableau EventMapping.

[IgnoreChange ControlEvent,](ignorechange-controlevent.md)

[SelectionDescription ControlEvent,](selectiondescription-controlevent.md)

[Sélection de ControlEvent,](selectionsize-controlevent.md)

[SelectionPath ControlEvent,](selectionpath-controlevent.md)

[SelectionAction ControlEvent,](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md)

Le ControlEvents suivant peut être publié à la discrétion d’un utilisateur en interagissant avec un contrôle de [bouton de commande](pushbutton-control.md) ou un contrôle de [case à cocher](checkbox-control.md) sur une boîte de dialogue. Le contrôle CheckBox peut uniquement publier les événements AddLocal, AddSource, Remove, inaction et SetProperty. avec les versions de Windows Installer fournies avec Windows Server 2003 et versions ultérieures, le [contrôle SelectionTree](selectiontree-control.md) peut publier les actions action, controlevent, et SetProperty ControlEvents. L’auteur de l’interface utilisateur doit répertorier le ControlEvent, dans la [table ControlEvent,](controlevent-table.md). Le gestionnaire d’interface utilisateur du programme d’installation est l’abonné à ces événements.

[AddLocal ControlEvent,](addlocal-controlevent.md)

[AddSource ControlEvent,](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent,](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent,](checktargetpath-controlevent.md)

[Action ControlEvent,](doaction-controlevent.md)

[EnableRollback ControlEvent,](enablerollback-controlevent.md)

[ControlEvent, EndDialog](enddialog-controlevent.md)

[NewDialog ControlEvent,](newdialog-controlevent.md)

[Réinstaller ControlEvent,](reinstall-controlevent.md)

[ReinstallMode ControlEvent,](reinstallmode-controlevent.md)

[Supprimer ControlEvent,](remove-controlevent.md)

[Réinitialiser ControlEvent,](reset-controlevent.md)

[SetInstallLevel ControlEvent,](setinstalllevel-controlevent.md)

[ControlEvent, SetProperty](setproperty-controlevent.md)

[SetTargetPath ControlEvent,](settargetpath-controlevent.md)

[SpawnDialog ControlEvent,](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent,](validateproductid-controlevent.md)

Un [contrôle PUSHBUTTON](pushbutton-control.md) peut publier les événements suivants dans un contrôle [SelectionTree](selectiontree-control.md) d’abonnement ou un [contrôle DirectoryList](directorylist-control.md) situé dans la même boîte de dialogue. Le contrôle PushButton doit être listé dans la table ControlEvent, et les contrôles d’abonnement doivent être listés dans la table EventMapping.

[SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md)

[DirectoryListUp ControlEvent,](directorylistup-controlevent.md)

[DirectoryListNew ControlEvent,](directorylistnew-controlevent.md)

[DirectoryListOpen ControlEvent,](directorylistopen-controlevent.md)

Les événements de contrôle requièrent généralement que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . La plupart des ControlEvents ne fonctionneront pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md) , car ces niveaux affichent uniquement des boîtes de dialogue non modales. Les événements ActionText, AddSource, SetProgress, TimeRemaining et ScriptInProgress sont des exceptions et fonctionnent dans une interface utilisateur réduite ou de base. Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Vous pouvez exécuter des [actions personnalisées](custom-actions.md) en publiant un ControlEvent, à partir d’un contrôle de [bouton de commande](pushbutton-control.md) ou d’un [contrôle CheckBox](checkbox-control.md). Ajoutez un enregistrement à la [table ControlEvent,](controlevent-table.md) avec les noms de la boîte de dialogue et le contrôle qui publie ControlEvent,. Ce contrôle doit publier un [ControlEvent,](doaction-controlevent.md) de script qui notifie le programme d’installation de l’exécution de l’action personnalisée. sur Windows XP ou les systèmes antérieurs, vous ne pouvez pas exécuter une action personnalisée en publiant un controlevent, à partir d’un [contrôle SelectionTree](selectiontree-control.md).

Pour plus d’informations sur le ControlEvents particulier, consultez la liste des données de [référence de l’interface utilisateur](user-interface-reference.md)standard [ControlEvents](control-events.md) .

 

 
