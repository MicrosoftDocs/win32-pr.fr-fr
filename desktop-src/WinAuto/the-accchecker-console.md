---
title: Console AccChecker
description: La console AccChecker (AccCheckConsole.exe) est un outil en ligne de commande permettant de vérifier l’implémentation de l’accessibilité de l’interface utilisateur de votre application.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Console AccChecker
- Outil en ligne de commande AccChecker
- ligne de commande, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839441"
---
# <a name="the-accchecker-console"></a>Console AccChecker

La console AccChecker (AccCheckConsole.exe) est un outil en ligne de commande permettant de vérifier l’implémentation de l’accessibilité de l’interface utilisateur de votre application. La ligne de commande accepte une variété d’entrées (telles que HWND, le titre de la fenêtre et la routine de vérification) et fournit un code de sortie qui correspond au nombre de journaux d’erreurs.

-   [Syntaxe de la ligne de commande](#command-line-syntax)
-   [Codes d’erreur de ligne de commande](#command-line-error-codes)
-   [Exemples de ligne de commande](#command-line-examples)
-   [Rubriques connexes](#related-topics)

![outil en ligne de commande de la console accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Syntaxe de ligne de commande

La console AccChecker a la syntaxe de ligne de commande suivante.

**\[Options AccCheckConsole \] (-HWND <hwnd> \| -process <name> )\[<dlls>\]**

Les options de ligne de commande sont les suivantes.



| Options                                                                                                                                                         | Description                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd><br/>                                                                     | Valide la fenêtre qui a le handle spécifié (HWND). Le descripteur peut être spécifié au format hexadécimal ou décimal.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-fenêtre <title><br/>                                                            | Valide la fenêtre qui a le titre spécifié.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -processus <name><br/>                       | Valide la fenêtre principale du processus qui porte le nom spécifié.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -List<br/>                                       | Répertorie toutes les routines de vérification disponibles.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -activer <name><br/>                          | Exécute la routine de vérification spécifiée. Cette option peut être spécifiée plusieurs fois.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -désactiver <name><br/> | Exécute toutes les tâches sauf la routine de vérification spécifiée. Cette option peut être spécifiée plusieurs fois.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| avertir \| Err)<br/>                          | L’évaluation de l’événement le plus bas qui sera enregistrée.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file><br/>                       | Écrit la sortie dans le fichier journal spécifié. Cette option peut être spécifiée plusieurs fois.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-supprimer <file><br/>                                                         | Utilisez le fichier XML spécifié pour supprimer les erreurs. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-quiet<br/>                                                                                             | N’écrivez pas la sortie de journalisation dans stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-aide <br/>                           | Affiche l’aide rapide. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Codes d’erreur de ligne de commande

Voici les codes d’erreur retournés par AccCheckConsole lors de l’utilisation de « echo% errorlevel% »



| Code d'erreur                       | Description                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Aucune erreur ni aucun avertissement.<br/>       |
| <span id="1"></span>1<br/> | L’instruction usages a été demandée. <br/> |
| <span id="2"></span>2<br/> | Erreurs et aucun avertissement.<br/>          |
| <span id="3"></span>1,3<br/> | Erreurs et avertissements.<br/>             |
| <span id="4"></span>4<br/> | Avertissements, mais aucune erreur.<br/>          |
| <span id="5"></span>5,5<br/> | Ligne de commande non valide. <br/>           |



 

## <a name="command-line-examples"></a>Exemples de ligne de commande

Voici plusieurs exemples de ligne de commande de la console AccChecker.

-   Exécuter toutes les vérifications sur une fenêtre avec un nom spécifié.

    **AccCheckConsole-fenêtre « sans titre-bloc-notes »**

-   Exécuter un sous-ensemble des vérifications sur un HWND, en spécifiant un fichier de suppression.

    **AccCheckConsole-HWND 0x00382f00-Enable CheckTabbing-Enable CheckName-supprimer les suppress.xml**

-   Exécuter toutes les vérifications à partir d’une nouvelle DLL de vérification.

    **AccCheckConsole-fenêtre « sans titre-bloc-notes » VerificationRoutine1.dll**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 





