---
description: Représente un objet dans l’interpréteur de commandes.
title: Objet IShellDispatch (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196476"
---
# <a name="ishelldispatch-object"></a>Objet IShellDispatch

Représente un objet dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.

> [!Note]  
> **IShellDispatch** est implémenté et accessible via l’objet [**Shell**](shell.md) .

 

## <a name="members"></a>Membres

L’objet **IShellDispatch** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **IShellDispatch** a ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet <a href="folder.md"><strong>dossier</strong></a> du dossier sélectionné.<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a> | Cascade toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des <strong>fenêtres en cascade</strong>.<br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Exécute l’application du panneau de configuration spécifiée. Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution. <br /><blockquote><p>[!Note]<br />à partir de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction. Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe. Par exemple :</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a> | Éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>éjecter le PC</strong>, si votre ordinateur prend en charge cette commande.<br /> | 
| <a href="ishelldispatch-explore.md"><strong>Explorer</strong></a> | ouvre un dossier spécifié dans une fenêtre de l’explorateur de Windows.<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a> | Affiche la boîte de dialogue <strong>exécuter</strong> à l’utilisateur.<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a> | Affiche la boîte de dialogue résultats de la <strong>recherche : ordinateurs</strong> . La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a> | Affiche la boîte de dialogue <strong>Rechercher : tous les fichiers</strong> . Cela revient à cliquer sur le menu <strong>Démarrer</strong> , puis à sélectionner <strong>Rechercher</strong>.<br /> | 
| <a href="ishelldispatch-help.md"><strong>Aide</strong></a> | affiche la fenêtre d’aide et de Support Windows. Cette méthode a le même effet que le fait de cliquer sur le menu <strong>Démarrer</strong> et de sélectionner <strong>aide et support</strong>.<br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a> | Réduit toutes les fenêtres sur le bureau. cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez <strong>réduire tout Windows</strong> sur les anciens systèmes ou si vous cliquez sur l’icône <strong>afficher le bureau</strong> dans la barre des tâches.<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>Joint</strong></a> | Crée et retourne un objet <a href="folder.md"><strong>Folder</strong></a> pour le dossier spécifié.<br /> | 
| <a href="ishelldispatch-open.md"><strong>Ouvrir</strong></a> | Ouvre le dossier spécifié.<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a> | Actualise le contenu du menu <strong>Démarrer</strong> . utilisé uniquement avec les systèmes précédents Windows XP.<br /> | 
| <a href="ishelldispatch-settime.md"><strong>SetTime</strong></a> | Affiche la boîte de dialogue <strong>date et heure</strong> . Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner <strong>ajuster la date/l’heure</strong>.<br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | affiche la boîte de dialogue <strong>arrêter le Windows</strong> . Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>arrêter</strong>.<br /> | 
| <a href="ishelldispatch-suspend.md"><strong>Momentané</strong></a> | équipements | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Mosaïques horizontalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option <strong>afficher les fenêtres empilées</strong>.<br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a> | Mosaïque verticalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option <strong>afficher les fenêtres côte à côte</strong>.<br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a> | Affiche la boîte de dialogue <strong>Propriétés de la barre des tâches et du menu Démarrer</strong> . Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez <strong>Propriétés</strong>.<br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Restaure toutes les fenêtres de bureau à l’État où elles se trouvaient avant la dernière commande <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>annuler réduire tout Windows</strong> (sur les systèmes plus anciens) ou un second clic sur l’icône <strong>afficher le bureau</strong> dans la barre des tâches.<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | Crée et retourne un objet <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.<br /> | 




 

### <a name="properties"></a>Propriétés

L’objet **IShellDispatch** a ces propriétés.



| Propriété                                                     | Type d’accès          | Description                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | Lecture seule<br/> | Contient un objet qui représente une application.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Lecture seule<br/> | Récupère un objet qui représente le parent de l’objet actuel.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objet Shell**](shell.md)
</dt> </dl>

 

 
