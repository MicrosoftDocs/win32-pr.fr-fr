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
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867745"
---
# <a name="shell-object"></a>Objet Shell

Représente les objets dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.

## <a name="members"></a>Membres

L’objet **Shell** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Shell** possède ces méthodes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Méthode</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></td>
<td style="text-align: left;">Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet <a href="folder.md"><strong>dossier</strong></a> du dossier sélectionné.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Cascade toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des <strong>fenêtres en cascade</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Exécute l’application spécifiée du panneau de configuration (*. cpl). Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution. <br/>
<blockquote>
<p>[!Note]<br />
À compter de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction. Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe. Par exemple :</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>éjecter le PC</strong>, si votre ordinateur prend en charge cette commande.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Explorer</strong></a></td>
<td style="text-align: left;">Ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Obtient la valeur d’une stratégie Internet Explorer spécifiée.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>exécuter</strong> à l’utilisateur. Cette méthode a le même effet que lorsque vous cliquez sur le menu <strong>Démarrer</strong> et sélectionnez <strong>exécuter</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue résultats de la <strong>recherche : ordinateurs</strong> . La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>Rechercher : tous les fichiers</strong> . Cela revient à cliquer sur le menu <strong>Démarrer</strong> , puis à sélectionner <strong>Rechercher</strong> (ou son équivalent sous systèmes ANTÉRIEURs à Windows XP).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>Rechercher l’imprimante</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">Récupère un paramètre d’interpréteur de commandes global.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Récupère des informations système.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Aide</strong></a></td>
<td style="text-align: left;">Affiche le centre d’aide et de support Windows. Cette méthode a le même effet que le fait de cliquer sur le menu <strong>Démarrer</strong> et de sélectionner <strong>aide et support</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Récupère le paramètre de restriction d’un groupe à partir du Registre.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Retourne une valeur qui indique si un service particulier est en cours d’exécution.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Réduit toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>réduire toutes les fenêtres</strong> sur les systèmes plus anciens ou de cliquer sur l’icône <strong>afficher le bureau</strong> dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Joint</strong></a></td>
<td style="text-align: left;">Crée et retourne un objet <a href="folder.md"><strong>Folder</strong></a> pour le dossier spécifié.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Ouvrir</strong></a></td>
<td style="text-align: left;">Ouvre le dossier spécifié.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Actualise le contenu du menu <strong>Démarrer</strong> . Utilisé uniquement avec les systèmes antérieurs à Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Affiche le volet de recherche applications.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></td>
<td style="text-align: left;">Démarre un service nommé.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">Arrête un service nommé.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>Propriétés de date et heure</strong> . Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner <strong>ajuster la date/l’heure</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Exécute une opération spécifiée sur un fichier spécifié.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">Affiche une barre de navigateur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>arrêter Windows</strong> . Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>arrêter</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Interrompre</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Mosaïques horizontalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection <strong>horizontale des fenêtres de mosaïque</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Mosaïque verticalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner les <strong>fenêtres de mosaïque verticalement</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Affiche ou masque le bureau.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>Propriétés de la barre des tâches et du menu Démarrer</strong> . Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez <strong>Propriétés</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez <strong>Annuler réduire toutes les fenêtres</strong> sur les systèmes plus anciens ou un second clic sur l’icône <strong>afficher le bureau</strong> dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crée et retourne un objet <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Affiche la boîte de dialogue <strong>sécurité Windows</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">Affiche vos fenêtres ouvertes dans une pile 3D que vous pouvez parcourir.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriétés

L’objet **Shell** possède ces propriétés.



| Propriété                                            | Type d’accès          | Description                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Lecture seule<br/> | Contient l’objet d’application de l’objet.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Lecture seule<br/> | Obtient un objet qui représente le parent de l’objet actuel.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
