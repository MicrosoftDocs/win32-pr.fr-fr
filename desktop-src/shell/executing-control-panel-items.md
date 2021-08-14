---
description: décrit les méthodes d’ouverture d’un élément du panneau de configuration pour les systèmes Windows Vista et versions ultérieures, ainsi que la couverture des commandes du panneau de configuration héritées.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Exécution des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e2bc84ce5225176585f2da221fab6110ce79f9ff68dfc83b3c66125d623d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224275"
---
# <a name="executing-control-panel-items"></a>Exécution des éléments du panneau de configuration

> [!Note]  
> Si vous recherchez la liste des noms canoniques et des noms de module pour les éléments du panneau de configuration, consultez [noms canoniques des éléments du panneau de configuration](controlpanel-canonical-names.md).

 

Il existe deux façons d’ouvrir un élément du panneau de configuration :

-   L’utilisateur peut ouvrir le panneau de configuration, puis ouvrir un élément en cliquant ou en double-cliquant sur l’icône de l’élément.
-   L’utilisateur ou une application peut démarrer un élément du panneau de configuration en l’exécutant directement à partir de l’invite de ligne de commande.

Une application peut ouvrir le panneau de configuration par programmation à l’aide de la fonction [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



L’exemple suivant montre comment une application peut démarrer l’élément du panneau de configuration nommé **MyCpl.cpl** à l’aide de la fonction [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Lorsqu’un élément du panneau de configuration est ouvert par le biais d’une ligne de commande, vous pouvez l’indiquer pour qu’il s’ouvre à un onglet particulier dans l’élément. en raison de l’ajout et de la suppression de certains onglets dans certains éléments du panneau de configuration Windows Vista, la numérotation des onglets peut avoir changé par rapport à celui de Windows XP. par exemple, l’exemple suivant lance le quatrième onglet de l’élément système sur Windows XP et le troisième onglet sur Windows Vista.


```
control.exe sysdm.cpl,,3
```



Cette rubrique traite des sujets suivants :

-   [Windows Noms canoniques Vista](#windows-vista-canonical-names)
-   [nouvelles commandes pour Windows Vista](#new-commands-for-windows-vista)
-   [Commandes du panneau de configuration héritées](#legacy-control-panel-commands)
-   [Rubriques connexes](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Noms canoniques Vista

dans Windows Vista et versions ultérieures, la méthode recommandée pour lancer un élément du panneau de configuration à partir d’une ligne de commande consiste à utiliser le nom canonique de l’élément du panneau de configuration. Un nom canonique est une chaîne non localisée que l’élément du panneau de configuration déclare dans le registre. La valeur de l’utilisation d’un nom canonique est qu’elle résume le nom de module de l’élément du panneau de configuration. Un élément peut être implémenté dans un .dll et ultérieurement être implémenté en tant que .exe ou modifier son nom de module. Tant que le nom canonique reste le même, tout programme qui l’ouvre à l’aide de ce nom canonique n’a pas besoin d’être mis à jour.

Par Convention, le nom canonique est formé en tant que « CorporationName. ControlPanelItemName ».

l’exemple suivant montre comment une application peut démarrer l’élément du panneau de configuration **Windows Update** avec [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Pour démarrer un élément du panneau de configuration avec son nom canonique, utilisez : "% systemroot% \\ system32 \\control.exe/name *canonicalName*"

Pour ouvrir une sous-page spécifique dans un élément ou pour l’ouvrir avec des paramètres supplémentaires, utilisez : « % systemroot% \\ system32 \\control.exe/name **canonicalName** des pages **pagename**»

Une application peut également implémenter la méthode [**IOpenControlPanel :: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) pour lancer des éléments du panneau de configuration, y compris la possibilité d’ouvrir une sous-page spécifique.

Pour obtenir la liste complète des noms canoniques des éléments du panneau de configuration, consultez [noms canoniques des éléments du panneau de configuration](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>nouvelles commandes pour Windows Vista

sur Windows Vista, certaines options qui étaient accessibles par un module .cpl sur Windows XP sont désormais implémentées en tant que fichiers .exe. Cela permet de renforcer la sécurité en permettant aux utilisateurs standard d’être invités à fournir des informations d’identification d’administrateur lors de la tentative de lancement des fichiers. les Options qui ne nécessitent pas de sécurité supplémentaire sont accessibles par les lignes de commande qui ont été utilisées dans Windows XP. la liste suivante répertorie les commandes utilisées dans Windows Vista pour accéder à des onglets spécifiques des éléments du panneau de configuration :

### <a name="personalization"></a>Personalization

-   Taille de police et PPP :% windir% \\ system32 \\DpiScaling.exe
-   résolution d’écran :% windir% \\ system32 \\control.exe desk.cpl, Paramètres,@Settings
-   paramètres d’affichage :% windir% \\ system32 \\control.exe desk.cpl, Paramètres,@Settings
-   Thèmes :% windir% \\ system32 \\control.exe desk.cpl, thèmes,@Themes
-   Économiseur d’écran :% windir% \\ system32 \\control.exe desk.cpl, écran de veille,@screensaver
-   Multi-Monitor :% windir% \\ system32 \\control.exe desk.cpl, surveiller@Monitor
-   Modèle de couleurs :% windir% \\ system32 \\control.exe/name Microsoft. Personalization des pages pageColorization
-   Arrière-plan du Bureau :% windir% \\ system32 \\control.exe/name Microsoft. Personalization des pages pageWallpaper

> [!Note]  
> Les éditions Starter et Basic ne prennent pas en charge la commande control.exe/name Microsoft. Personalization.

 

### <a name="system"></a>Système

-   Performances :% windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Accès à distance :% windir% \\ system32 \\SystemPropertiesRemote.exe
-   Nom de l’ordinateur :% windir% \\ system32 \\SystemPropertiesComputerName.exe
-   Protection du système :% windir% \\ system32 \\SystemPropertiesProtection.exe
-   Propriétés système avancées :% windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programmes et fonctionnalités

-   Ajout/suppression de programmes :% windir% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures
-   fonctionnalités de Windows :% windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Options régionales et linguistiques

-   Clavier :% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions des pages/p : "Keyboard"
-   Emplacement :% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions des pages/p : "location"
-   Administration :% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions des pages/p : "administrative"

### <a name="folder-options"></a>Options des dossiers

-   Recherche de dossier :% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundll 2
-   Associations de fichiers :% windir% \\ system32 \\control.exe/name Microsoft. DefaultPrograms des pages pageFileAssoc
-   Affichage :% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundll 7
-   Général :% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundll 0

### <a name="power-options"></a>Options d’alimentation

-   Modifier les paramètres actuels du plan :% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions des pages pagePlanSettings
-   Paramètres système :% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions des pages pageGlobalSettings
-   Créer un mode de gestion de l’alimentation :% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions des pages pageCreateNewPlan
-   il n’existe aucune commande canonique pour la page de Paramètres avancée, elle est accessible de la manière précédente :% windir% \\ system32 \\control.exe powercfg.cpl,, 3

## <a name="legacy-control-panel-commands"></a>Commandes du panneau de configuration héritées

Lorsque vous utilisez la fonction [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , le système peut reconnaître des commandes spéciales du panneau de configuration. ces commandes préWindows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe Desktop</td>
<td>Lance la fenêtre <strong>propriétés d’affichage</strong> .
<blockquote>
[!Note]<br />
Les éditions Starter et Basic ne prennent pas en charge cette commande.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Couleur de control.exe</td>
<td>Ouvre la fenêtre <strong>propriétés d’affichage</strong> avec l’onglet <strong>apparence</strong> présélectionné.</td>
</tr>
<tr class="odd">
<td>Date/heure de control.exe</td>
<td>Lance la fenêtre des <strong>Propriétés de date et d’heure</strong> .</td>
</tr>
<tr class="even">
<td>control.exe international</td>
<td>Lance la fenêtre <strong>Options régionales et linguistiques</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe souris</td>
<td>Lance la fenêtre Propriétés de la <strong>souris</strong> .</td>
</tr>
<tr class="even">
<td>Clavier control.exe</td>
<td>Lance la fenêtre <strong>Propriétés du clavier</strong> .</td>
</tr>
<tr class="odd">
<td>Imprimantes control.exe</td>
<td>Affiche le dossier <strong>imprimantes et télécopieurs</strong> .</td>
</tr>
<tr class="even">
<td>Polices de control.exe</td>
<td>Affiche le dossier <strong>polices</strong> .</td>
</tr>
</tbody>
</table>



 

pour les systèmes Windows 2000 et versions ultérieures :



| Commande                    | Description                                              |
|----------------------------|----------------------------------------------------------|
| Dossiers de control.exe        | Lance la fenêtre **Options des dossiers** .                  |
| control.exe NetWare        | Lance la fenêtre **Novell NetWare** (si installée).   |
| Téléphonie control.exe      | lance la fenêtre **Options de Téléphone et de Modem** .         |
| control.exe AdminTools     | Affiche le dossier **Outils d’administration** .            |
| control.exe schedtasks     | Affiche le dossier **tâches planifiées** .                 |
| control.exe netconnections | Affiche le dossier **connexions réseau** .             |
| control.exe infrarouge       | Lance la fenêtre **Moniteur infrarouge** (si installée). |
| control.exe userpasswords  | Lance la fenêtre **comptes d’utilisateur** .                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Affectation des catégories du panneau de configuration](assigning-control-panel-categories.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> <dt>

[accès au panneau de configuration en Mode Coffre sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
