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
# <a name="the-accchecker-console"></a><span data-ttu-id="fff81-106">Console AccChecker</span><span class="sxs-lookup"><span data-stu-id="fff81-106">The AccChecker Console</span></span>

<span data-ttu-id="fff81-107">La console AccChecker (AccCheckConsole.exe) est un outil en ligne de commande permettant de vérifier l’implémentation de l’accessibilité de l’interface utilisateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="fff81-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="fff81-108">La ligne de commande accepte une variété d’entrées (telles que HWND, le titre de la fenêtre et la routine de vérification) et fournit un code de sortie qui correspond au nombre de journaux d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="fff81-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="fff81-109">Syntaxe de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fff81-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="fff81-110">Codes d’erreur de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fff81-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="fff81-111">Exemples de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fff81-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="fff81-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fff81-112">Related topics</span></span>](#related-topics)

![outil en ligne de commande de la console accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="fff81-114">Syntaxe de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fff81-114">Command-line Syntax</span></span>

<span data-ttu-id="fff81-115">La console AccChecker a la syntaxe de ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="fff81-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="fff81-116">**\[Options AccCheckConsole \] (-HWND <hwnd> \| -process <name> )\[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="fff81-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="fff81-117">Les options de ligne de commande sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="fff81-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="fff81-118">Options</span><span class="sxs-lookup"><span data-stu-id="fff81-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="fff81-119">Description</span><span class="sxs-lookup"><span data-stu-id="fff81-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fff81-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd></span><span class="sxs-lookup"><span data-stu-id="fff81-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="fff81-121">Valide la fenêtre qui a le handle spécifié (HWND).</span><span class="sxs-lookup"><span data-stu-id="fff81-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="fff81-122">Le descripteur peut être spécifié au format hexadécimal ou décimal.</span><span class="sxs-lookup"><span data-stu-id="fff81-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="fff81-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-fenêtre <title></span><span class="sxs-lookup"><span data-stu-id="fff81-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="fff81-124">Valide la fenêtre qui a le titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="fff81-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="fff81-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -processus <name></span><span class="sxs-lookup"><span data-stu-id="fff81-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="fff81-126">Valide la fenêtre principale du processus qui porte le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="fff81-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="fff81-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -List</span><span class="sxs-lookup"><span data-stu-id="fff81-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="fff81-128">Répertorie toutes les routines de vérification disponibles.</span><span class="sxs-lookup"><span data-stu-id="fff81-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="fff81-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -activer <name></span><span class="sxs-lookup"><span data-stu-id="fff81-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="fff81-130">Exécute la routine de vérification spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fff81-130">Runs the specified verification routine.</span></span> <span data-ttu-id="fff81-131">Cette option peut être spécifiée plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="fff81-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="fff81-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -désactiver <name></span><span class="sxs-lookup"><span data-stu-id="fff81-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="fff81-133">Exécute toutes les tâches sauf la routine de vérification spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fff81-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="fff81-134">Cette option peut être spécifiée plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="fff81-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="fff81-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| avertir \| Err)</span><span class="sxs-lookup"><span data-stu-id="fff81-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="fff81-136">L’évaluation de l’événement le plus bas qui sera enregistrée.</span><span class="sxs-lookup"><span data-stu-id="fff81-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="fff81-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span><span class="sxs-lookup"><span data-stu-id="fff81-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="fff81-138">Écrit la sortie dans le fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="fff81-138">Write the output to the specified log file.</span></span> <span data-ttu-id="fff81-139">Cette option peut être spécifiée plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="fff81-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="fff81-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-supprimer <file></span><span class="sxs-lookup"><span data-stu-id="fff81-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="fff81-141">Utilisez le fichier XML spécifié pour supprimer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="fff81-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="fff81-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span><span class="sxs-lookup"><span data-stu-id="fff81-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="fff81-143">N’écrivez pas la sortie de journalisation dans stdout.</span><span class="sxs-lookup"><span data-stu-id="fff81-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="fff81-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-aide</span><span class="sxs-lookup"><span data-stu-id="fff81-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="fff81-145">Affiche l’aide rapide.</span><span class="sxs-lookup"><span data-stu-id="fff81-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="fff81-146">Codes d’erreur de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fff81-146">Command-line Error Codes</span></span>

<span data-ttu-id="fff81-147">Voici les codes d’erreur retournés par AccCheckConsole lors de l’utilisation de « echo% errorlevel% »</span><span class="sxs-lookup"><span data-stu-id="fff81-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="fff81-148">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="fff81-148">Error code</span></span>                       | <span data-ttu-id="fff81-149">Description</span><span class="sxs-lookup"><span data-stu-id="fff81-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="fff81-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="fff81-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="fff81-151">Aucune erreur ni aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="fff81-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="fff81-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="fff81-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="fff81-153">L’instruction usages a été demandée.</span><span class="sxs-lookup"><span data-stu-id="fff81-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="fff81-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="fff81-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="fff81-155">Erreurs et aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="fff81-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="fff81-156"><span id="3"></span>1,3</span><span class="sxs-lookup"><span data-stu-id="fff81-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="fff81-157">Erreurs et avertissements.</span><span class="sxs-lookup"><span data-stu-id="fff81-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="fff81-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="fff81-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="fff81-159">Avertissements, mais aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="fff81-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="fff81-160"><span id="5"></span>5,5</span><span class="sxs-lookup"><span data-stu-id="fff81-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="fff81-161">Ligne de commande non valide.</span><span class="sxs-lookup"><span data-stu-id="fff81-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="fff81-162">Exemples de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fff81-162">Command-line Examples</span></span>

<span data-ttu-id="fff81-163">Voici plusieurs exemples de ligne de commande de la console AccChecker.</span><span class="sxs-lookup"><span data-stu-id="fff81-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="fff81-164">Exécuter toutes les vérifications sur une fenêtre avec un nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="fff81-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="fff81-165">**AccCheckConsole-fenêtre « sans titre-bloc-notes »**</span><span class="sxs-lookup"><span data-stu-id="fff81-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="fff81-166">Exécuter un sous-ensemble des vérifications sur un HWND, en spécifiant un fichier de suppression.</span><span class="sxs-lookup"><span data-stu-id="fff81-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="fff81-167">**AccCheckConsole-HWND 0x00382f00-Enable CheckTabbing-Enable CheckName-supprimer les suppress.xml**</span><span class="sxs-lookup"><span data-stu-id="fff81-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="fff81-168">Exécuter toutes les vérifications à partir d’une nouvelle DLL de vérification.</span><span class="sxs-lookup"><span data-stu-id="fff81-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="fff81-169">**AccCheckConsole-fenêtre « sans titre-bloc-notes » VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="fff81-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="fff81-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fff81-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fff81-171">Vérificateur d’accessibilité de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="fff81-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





