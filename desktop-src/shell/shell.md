---
description: Représente les objets dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.
title: Objet Shell (shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: d31adcbf5a12d699750029c15a308ef73f4d8c03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412374"
---
# <a name="shell-object"></a>Objet Shell

Représente les objets dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.

## <a name="members"></a>Membres

L’objet **Shell** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Shell** possède ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a> | Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).<br /> | 
| <a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet <a href="folder.md"><strong>dossier</strong></a> du dossier sélectionné.<br /> | 
| <a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a> | Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.<br /> | 
| <a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a> | Cascade toutes les fenêtres sur le bureau. Cette méthode a le même effet que le fait de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>Cascade Windows</strong>.<br /> | 
| <a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Exécute l’application du panneau de configuration (* .cpl) spécifiée. Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution. <br /><blockquote><p>[!Note]<br />à partir de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction. Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe. Par exemple :</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="shell-ejectpc.md"><strong>EjectPC</strong></a> | Éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>éjecter le PC</strong>, si votre ordinateur prend en charge cette commande.<br /> | 
| <a href="shell-explore.md"><strong>Explorer</strong></a> | ouvre un dossier spécifié dans une fenêtre de l’explorateur de Windows.<br /> | 
| <a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a> | Obtient la valeur d’une stratégie Internet Explorer spécifiée.<br /> | 
| <a href="shell-filerun.md"><strong>FileRun</strong></a> | Affiche la boîte de dialogue <strong>exécuter</strong> à l’utilisateur. Cette méthode a le même effet que lorsque vous cliquez sur le menu <strong>Démarrer</strong> et sélectionnez <strong>exécuter</strong>.<br /> | 
| <a href="shell-findcomputer.md"><strong>FindComputer</strong></a> | Affiche la boîte de dialogue résultats de la <strong>recherche : ordinateurs</strong> . La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.<br /> | 
| <a href="shell-findfiles.md"><strong>FindFiles</strong></a> | Affiche la boîte de dialogue <strong>Rechercher : tous les fichiers</strong> . cela revient à cliquer sur le menu <strong>démarrer</strong> , puis à sélectionner <strong>rechercher</strong> (ou son équivalent sous systèmes antérieurs à Windows XP).<br /> | 
| <a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a> | Affiche la boîte de dialogue <strong>Rechercher l’imprimante</strong> .<br /> | 
| <a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a> | Récupère un paramètre d’interpréteur de commandes global.<br /> | 
| <a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a> | Récupère des informations système.<br /> | 
| <a href="shell-help.md"><strong>Aide</strong></a> | affiche le centre d’aide et de Support Windows. Cette méthode a le même effet que le fait de cliquer sur le menu <strong>Démarrer</strong> et de sélectionner <strong>aide et support</strong>.<br /> | 
| <a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a> | Récupère le paramètre de restriction d’un groupe à partir du Registre.<br /> | 
| <a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a> | Retourne une valeur qui indique si un service particulier est en cours d’exécution.<br /> | 
| <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> | Réduit toutes les fenêtres sur le bureau. cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez <strong>réduire tout Windows</strong> sur les anciens systèmes ou si vous cliquez sur l’icône <strong>afficher le bureau</strong> dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.<br /> | 
| <a href="shell-namespace.md"><strong>Joint</strong></a> | Crée et retourne un objet <a href="folder.md"><strong>Folder</strong></a> pour le dossier spécifié.<br /> | 
| <a href="shell-open.md"><strong>Ouvrir</strong></a> | Ouvre le dossier spécifié.<br /> | 
| <a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a> | Actualise le contenu du menu <strong>Démarrer</strong> . utilisé uniquement avec les systèmes précédents Windows XP.<br /> | 
| <a href="shell-searchcommand.md"><strong>SearchCommand</strong></a> | Affiche le volet de recherche applications.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a> | Démarre un service nommé.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a> | Arrête un service nommé.<br /> | 
| <a href="shell-settime.md"><strong>SetTime</strong></a> | Affiche la boîte de dialogue <strong>Propriétés de date et heure</strong> . Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner <strong>ajuster la date/l’heure</strong>.<br /> | 
| <a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a> | Exécute une opération spécifiée sur un fichier spécifié.<br /> | 
| <a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a> | Affiche une barre de navigateur.<br /> | 
| <a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | affiche la boîte de dialogue <strong>arrêter le Windows</strong> . Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>arrêter</strong>.<br /> | 
| <a href="shell-suspend.md"><strong>Momentané</strong></a> | équipements | 
| <a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Mosaïques horizontalement toutes les fenêtres sur le bureau. cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des <strong>vignettes Windows horizontalement</strong>.<br /> | 
| <a href="shell-tilevertically.md"><strong>TileVertically</strong></a> | Mosaïque verticalement toutes les fenêtres sur le bureau. cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des <strong>vignettes Windows verticalement</strong>.<br /> | 
| <a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a> | Affiche ou masque le bureau.<br /> | 
| <a href="shell-trayproperties.md"><strong>TrayProperties</strong></a> | Affiche la boîte de dialogue <strong>Propriétés de la barre des tâches et du menu Démarrer</strong> . Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez <strong>Propriétés</strong>.<br /> | 
| <a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . cette méthode a le même effet que le fait de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>annuler réduire tout Windows</strong> sur les systèmes plus anciens ou un second clic sur l’icône <strong>afficher le bureau</strong> dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.<br /> | 
| <a href="shell-windows.md"><strong>Windows</strong></a> | Crée et retourne un objet <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.<br /> | 
| <a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a> | affiche la boîte de dialogue <strong>Sécurité Windows</strong> .<br /> | 
| <a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a> | Affiche vos fenêtres ouvertes dans une pile 3D que vous pouvez parcourir.<br /> | 




 

### <a name="properties"></a>Propriétés

L’objet **Shell** possède ces propriétés.



| Propriété                                            | Type d’accès          | Description                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Lecture seule<br/> | Contient l’objet d’application de l’objet.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Lecture seule<br/> | Obtient un objet qui représente le parent de l’objet actuel.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
