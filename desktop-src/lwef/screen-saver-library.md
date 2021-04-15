---
title: Gestion des économiseurs d’écran
description: L’API Microsoft Win32 prend en charge des applications spéciales appelées économiseurs d’écran.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- économiseurs d’écran
- Panneau de configuration, économiseurs d’écran
- ScreenSaverConfigureDialog
- fichiers de définition de module
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463095"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="7a25c-107">Gestion des économiseurs d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-107">Handling Screen Savers</span></span>

<span data-ttu-id="7a25c-108">L’API Microsoft Win32 prend en charge des applications spéciales appelées *économiseurs d’écran*.</span><span class="sxs-lookup"><span data-stu-id="7a25c-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="7a25c-109">Les économiseurs d’écran démarrent lorsque la souris et le clavier sont restés inactifs pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7a25c-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="7a25c-110">Ils sont utilisés pour les deux raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a25c-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="7a25c-111">Pour protéger un écran de la gravure de phosphore provoquée par les images statiques.</span><span class="sxs-lookup"><span data-stu-id="7a25c-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="7a25c-112">Pour masquer les informations sensibles laissées sur un écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="7a25c-113">Cette rubrique est composée des sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a25c-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="7a25c-114">À propos des économiseurs d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="7a25c-115">Utilisation des fonctions d’économiseur d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="7a25c-116">Création d’un écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="7a25c-117">Installation des nouveaux économiseurs d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   [<span data-ttu-id="7a25c-118">Ajout de l’aide à la boîte de dialogue Configuration de l’écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-118">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a><span data-ttu-id="7a25c-119">À propos des économiseurs d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-119">About Screen Savers</span></span>

<span data-ttu-id="7a25c-120">L’application de bureau dans le panneau de configuration Windows permet aux utilisateurs de sélectionner dans une liste d’économiseurs d’écran, de spécifier le temps qui doit s’écouler avant le démarrage de l’économiseur d’écran, de configurer des économiseurs d’écran et d’afficher un aperçu des économiseurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="7a25c-121">Les économiseurs d’écran sont chargés automatiquement au démarrage de Windows ou lorsqu’un utilisateur active l’économiseur d’écran par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="7a25c-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="7a25c-122">Une fois qu’un économiseur d’écran est choisi, Windows surveille les séquences de touches et les mouvements de la souris, puis démarre l’écran de veille après une période d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="7a25c-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="7a25c-123">Toutefois, Windows ne démarre pas l’économiseur d’écran si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="7a25c-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="7a25c-124">L’application active n’est pas une application Windows.</span><span class="sxs-lookup"><span data-stu-id="7a25c-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="7a25c-125">Une fenêtre de formation basée sur l’ordinateur (CBT) est présente.</span><span class="sxs-lookup"><span data-stu-id="7a25c-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="7a25c-126">L’application active reçoit le message [WM \_ SYSCOMMAND](../menurc/wm-syscommand.md) avec le paramètre *wParam* défini sur la valeur SC \_ SCREENSAVE, mais il ne transmet pas le message à la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="7a25c-127">**Contexte de sécurité de l’écran de veille**</span><span class="sxs-lookup"><span data-stu-id="7a25c-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="7a25c-128">Le contexte de sécurité de l’écran de veille dépend du fait qu’un utilisateur ait ouvert une session interactive.</span><span class="sxs-lookup"><span data-stu-id="7a25c-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="7a25c-129">Si un utilisateur est connecté de manière interactive lorsque l’économiseur d’écran est appelé, l’économiseur d’écran s’exécute dans le contexte de sécurité de l’utilisateur interactif.</span><span class="sxs-lookup"><span data-stu-id="7a25c-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="7a25c-130">Si aucun utilisateur n’est connecté, le contexte de sécurité de l’écran de veille dépend de la version de Windows utilisée.</span><span class="sxs-lookup"><span data-stu-id="7a25c-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="7a25c-131">Windows XP et Windows 2000-l’économiseur d’écran s’exécute dans le contexte de LocalSystem avec les comptes restreints.</span><span class="sxs-lookup"><span data-stu-id="7a25c-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="7a25c-132">Windows 2003-l’économiseur d’écran s’exécute dans le contexte de LocalService avec tous les privilèges supprimés et le groupe administrateurs désactivé.</span><span class="sxs-lookup"><span data-stu-id="7a25c-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="7a25c-133">Ne s’applique pas à Windows NT4.</span><span class="sxs-lookup"><span data-stu-id="7a25c-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="7a25c-134">Le contexte de sécurité détermine le niveau des opérations privilégiées qui peuvent être effectuées à partir d’un écran de veille.</span><span class="sxs-lookup"><span data-stu-id="7a25c-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="7a25c-135">**Windows Vista et versions ultérieures :** Si la protection par mot de passe est activée par la stratégie, l’économiseur d’écran est démarré indépendamment de ce que fait une application avec la \_ notification SC SCREENSAVE.</span><span class="sxs-lookup"><span data-stu-id="7a25c-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="7a25c-136">Les économiseurs d’écran contiennent des fonctions exportées spécifiques, des définitions de ressource et des déclarations de variables.</span><span class="sxs-lookup"><span data-stu-id="7a25c-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="7a25c-137">La bibliothèque de l’économiseur d’écran contient la fonction **principale** et le code de démarrage requis pour un économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="7a25c-138">Lorsqu’un économiseur d’écran démarre, le code de démarrage de la bibliothèque de l’écran de veille crée une fenêtre plein écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="7a25c-139">La classe de fenêtre pour cette fenêtre est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a25c-139">The window class for this window is declared as follows:</span></span>


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



<span data-ttu-id="7a25c-140">Pour créer un écran de veille, la plupart des développeurs créent un module de code source contenant trois fonctions requises et les lient à la bibliothèque de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="7a25c-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="7a25c-141">Un module d’économiseur d’écran est uniquement responsable de la configuration et de la fourniture d’effets visuels.</span><span class="sxs-lookup"><span data-stu-id="7a25c-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="7a25c-142">L’une des trois fonctions requises dans un module d’économiseur d’écran est [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="7a25c-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="7a25c-143">Cette fonction traite des messages spécifiques et renvoie tous les messages non traités à la bibliothèque de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="7a25c-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="7a25c-144">Voici quelques-uns des messages classiques traités par **ScreenSaverProc**.</span><span class="sxs-lookup"><span data-stu-id="7a25c-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="7a25c-145">Message</span><span class="sxs-lookup"><span data-stu-id="7a25c-145">Message</span></span>        | <span data-ttu-id="7a25c-146">Signification</span><span class="sxs-lookup"><span data-stu-id="7a25c-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a25c-147">création de WM \_</span><span class="sxs-lookup"><span data-stu-id="7a25c-147">WM\_CREATE</span></span>     | <span data-ttu-id="7a25c-148">Récupérez les données d’initialisation à partir du fichier Regedit.ini.</span><span class="sxs-lookup"><span data-stu-id="7a25c-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="7a25c-149">Définissez un minuteur de fenêtre pour la fenêtre de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="7a25c-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="7a25c-150">Effectuez toute autre initialisation requise.</span><span class="sxs-lookup"><span data-stu-id="7a25c-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="7a25c-151">\_ERASEBKGND WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="7a25c-152">Effacez la fenêtre de l’écran de veille et préparez-vous aux opérations de dessin suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a25c-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="7a25c-153">\_minuteur WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-153">WM\_TIMER</span></span>      | <span data-ttu-id="7a25c-154">Effectuer des opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="7a25c-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="7a25c-155">\_destructeur WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-155">WM\_DESTROY</span></span>    | <span data-ttu-id="7a25c-156">Détruisez les minuteurs créés lorsque l’application a traité le message [WM \_ Create](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="7a25c-157">Effectuez tout nettoyage supplémentaire requis.</span><span class="sxs-lookup"><span data-stu-id="7a25c-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="7a25c-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) transmet les messages non traités à la bibliothèque de l’écran de veille en appelant la fonction [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="7a25c-159">Le tableau suivant décrit comment cette fonction traite différents messages.</span><span class="sxs-lookup"><span data-stu-id="7a25c-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="7a25c-160">Message</span><span class="sxs-lookup"><span data-stu-id="7a25c-160">Message</span></span>         | <span data-ttu-id="7a25c-161">Action</span><span class="sxs-lookup"><span data-stu-id="7a25c-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="7a25c-162">\_SETCURSOR WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="7a25c-163">Définissez le curseur sur le curseur null, en le supprimant de l’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="7a25c-164">\_peinture WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-164">WM\_PAINT</span></span>       | <span data-ttu-id="7a25c-165">Peindre l’arrière-plan de l’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="7a25c-166">\_LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="7a25c-167">Mettre fin à l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="7a25c-168">\_MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="7a25c-169">Mettre fin à l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="7a25c-170">\_RBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="7a25c-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="7a25c-171">Mettre fin à l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="7a25c-172">WM- \_ touche</span><span class="sxs-lookup"><span data-stu-id="7a25c-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="7a25c-173">Mettre fin à l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="7a25c-174">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="7a25c-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="7a25c-175">Mettre fin à l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="7a25c-176">activation de WM \_</span><span class="sxs-lookup"><span data-stu-id="7a25c-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="7a25c-177">Met fin à l’économiseur d’écran si le paramètre *wParam* est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="7a25c-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="7a25c-178">La deuxième fonction requise dans un module d’économiseur d’écran est [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span><span class="sxs-lookup"><span data-stu-id="7a25c-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="7a25c-179">Cette fonction affiche une boîte de dialogue qui permet à l’utilisateur de configurer l’économiseur d’écran (une application doit fournir un modèle de boîte de dialogue correspondant).</span><span class="sxs-lookup"><span data-stu-id="7a25c-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="7a25c-180">Windows affiche la boîte de dialogue de configuration lorsque l’utilisateur sélectionne le bouton **configurer** dans la boîte de dialogue économiseur d’écran du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="7a25c-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="7a25c-181">La troisième fonction requise dans un module d’économiseur d’écran est [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span><span class="sxs-lookup"><span data-stu-id="7a25c-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="7a25c-182">Cette fonction doit être appelée par toutes les applications de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="7a25c-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="7a25c-183">Toutefois, les applications qui ne nécessitent pas de contrôles personnalisés ou Windows spéciaux dans la boîte de dialogue de configuration peuvent simplement retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7a25c-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="7a25c-184">Les applications nécessitant des contrôles personnalisés ou des fenêtres spéciales doivent utiliser cette fonction pour inscrire les classes de fenêtre correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7a25c-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="7a25c-185">En plus de créer un module qui prend en charge les trois fonctions qui viennent d’être décrites, un écran de veille doit fournir une icône.</span><span class="sxs-lookup"><span data-stu-id="7a25c-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="7a25c-186">Cette icône est visible uniquement lorsque l’économiseur d’écran est exécuté en tant qu’application autonome.</span><span class="sxs-lookup"><span data-stu-id="7a25c-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="7a25c-187">(Pour qu’il soit exécuté par le panneau de configuration, un économiseur d’écran doit avoir l’extension de nom de fichier. SCR ; pour être exécuté en tant qu’application autonome, il doit avoir l’extension de nom de fichier. exe.) L’icône doit être identifiée dans le fichier de ressources de l’écran de veille par l’application d’ID de constante \_ , qui est définie dans le fichier d’en-tête scrnsave. h.</span><span class="sxs-lookup"><span data-stu-id="7a25c-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="7a25c-188">Une dernière exigence est une chaîne de description de l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="7a25c-189">Le fichier de ressources d’un économiseur d’écran doit contenir une chaîne que le panneau de configuration affiche comme nom de l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="7a25c-190">La chaîne de description doit être la première chaîne dans la table de chaînes du fichier de ressources (identifiée par la valeur ordinale 1).</span><span class="sxs-lookup"><span data-stu-id="7a25c-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="7a25c-191">Toutefois, la chaîne de description est ignorée par le panneau de configuration si l’économiseur d’écran a un nom de fichier long.</span><span class="sxs-lookup"><span data-stu-id="7a25c-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="7a25c-192">Dans ce cas, le nom de fichier sera utilisé comme chaîne de description.</span><span class="sxs-lookup"><span data-stu-id="7a25c-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="7a25c-193">Utilisation des fonctions d’économiseur d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="7a25c-194">Cette section utilise un exemple de code tiré d’une application d’écran de veille pour illustrer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a25c-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="7a25c-195">Création d’un écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="7a25c-196">Installation des nouveaux économiseurs d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   [<span data-ttu-id="7a25c-197">Ajout de l’aide à la boîte de dialogue Configuration de l’écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-197">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a><span data-ttu-id="7a25c-198">Création d’un écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-198">Creating a Screen Saver</span></span>

<span data-ttu-id="7a25c-199">À intervalles allant de 1 à 10 secondes, l’application dans cet exemple repeint l’écran avec l’une des quatre couleurs suivantes : blanc, gris clair, gris foncé et noir.</span><span class="sxs-lookup"><span data-stu-id="7a25c-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="7a25c-200">L’application peint l’écran chaque fois qu’il reçoit un message de [ \_ minuteur WM](../winmsg/wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="7a25c-201">L’utilisateur peut régler l’intervalle auquel ce message est envoyé en sélectionnant la boîte de dialogue de configuration de l’application et en ajustant une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="7a25c-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="7a25c-202">Bibliothèque de l’écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-202">Screen saver library</span></span>

<span data-ttu-id="7a25c-203">Les fonctions d’économiseur d’écran statiques sont contenues dans la bibliothèque de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="7a25c-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="7a25c-204">Deux versions de la bibliothèque sont disponibles : scrnsave. lib et Scrnsavw. lib.</span><span class="sxs-lookup"><span data-stu-id="7a25c-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="7a25c-205">Vous devez lier votre projet avec l’un de ces.</span><span class="sxs-lookup"><span data-stu-id="7a25c-205">You must link your project with one of these.</span></span> <span data-ttu-id="7a25c-206">Scrnsave. lib est utilisé pour les économiseurs d’écran qui utilisent des caractères ANSI et Scrnsavw. lib est utilisé pour les économiseurs d’écran qui utilisent des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a25c-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="7a25c-207">Un économiseur d’écran qui est lié à Scrnsavw. lib s’exécutera uniquement sur les plateformes Windows qui prennent en charge Unicode, tandis qu’un économiseur d’écran lié à scrnsave. lib s’exécutera sur toute plateforme Windows.</span><span class="sxs-lookup"><span data-stu-id="7a25c-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="7a25c-208">Prise en charge de la boîte de dialogue de configuration</span><span class="sxs-lookup"><span data-stu-id="7a25c-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="7a25c-209">La plupart des économiseurs d’écran fournissent une boîte de dialogue de configuration pour permettre à l’utilisateur de spécifier des données de personnalisation, telles que des couleurs uniques, des vitesses de dessin, l’épaisseur de ligne, les polices, etc.</span><span class="sxs-lookup"><span data-stu-id="7a25c-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="7a25c-210">Pour prendre en charge la boîte de dialogue de configuration, l’application doit fournir un modèle de boîte de dialogue et doit également prendre en charge la fonction [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="7a25c-211">Voici le modèle de boîte de dialogue pour l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="7a25c-211">Following is the dialog box template for the sample application.</span></span>


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



<span data-ttu-id="7a25c-212">Vous devez définir la constante utilisée pour identifier le modèle de boîte de dialogue à l’aide de la valeur décimale 2003, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7a25c-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="7a25c-213">L’exemple suivant illustre la fonction [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) trouvée dans l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="7a25c-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



<span data-ttu-id="7a25c-214">En plus de fournir le modèle de boîte de dialogue et de prendre en charge la fonction [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , une application doit également prendre en charge la fonction [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="7a25c-215">Cette fonction inscrit toutes les classes de fenêtre non standard requises par l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="7a25c-216">Étant donné que l’exemple d’application a utilisé uniquement des classes de fenêtre standard dans sa procédure de boîte de dialogue, cette fonction retourne simplement **true**, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7a25c-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="7a25c-217">Prise en charge de la procédure de fenêtre de l’écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="7a25c-218">Chaque écran de veille doit prendre en charge une procédure de fenêtre nommée [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="7a25c-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="7a25c-219">À l’instar de la plupart des procédures de fenêtre, **ScreenSaverProc** traite un ensemble de messages spécifiques et transmet les messages non traités à une procédure par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a25c-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="7a25c-220">Toutefois, au lieu de les transmettre à la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , **ScreenSaverProc** passe des messages non traités à la fonction [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="7a25c-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="7a25c-221">Une autre différence entre **ScreenSaverProc** et une procédure de fenêtre normale est que le handle passé à **ScreenSaverProc** identifie l’intégralité du Bureau plutôt qu’une fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="7a25c-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="7a25c-222">L’exemple suivant illustre la procédure de fenêtre **ScreenSaverProc** pour l’exemple d’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a25c-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="7a25c-223">Création d’un fichier de définition de module</span><span class="sxs-lookup"><span data-stu-id="7a25c-223">Creating a module-definition file</span></span>

<span data-ttu-id="7a25c-224">Les fonctions [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) et [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) doivent être exportées dans le fichier de définition de module de l’application ; Toutefois, [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) ne doit pas être exporté.</span><span class="sxs-lookup"><span data-stu-id="7a25c-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="7a25c-225">L’exemple suivant montre le fichier de définition de module pour l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="7a25c-225">The following example shows the module-definition file for the sample application.</span></span>


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a><span data-ttu-id="7a25c-226">Installation des nouveaux économiseurs d’écran</span><span class="sxs-lookup"><span data-stu-id="7a25c-226">Installing New Screen Savers</span></span>

<span data-ttu-id="7a25c-227">Lors de la compilation de la liste des économiseurs d’écran disponibles, le panneau de configuration recherche dans le répertoire de démarrage Windows les fichiers portant l’extension. scr.</span><span class="sxs-lookup"><span data-stu-id="7a25c-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="7a25c-228">Étant donné que les économiseurs d’écran sont des fichiers exécutables Windows standard avec des extensions. exe, vous devez les renommer pour qu’ils aient des extensions. SCR et les copier dans le répertoire approprié.</span><span class="sxs-lookup"><span data-stu-id="7a25c-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="7a25c-229">Ajout de l’aide à la boîte de dialogue Configuration de l’écran de veille</span><span class="sxs-lookup"><span data-stu-id="7a25c-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="7a25c-230">La boîte de dialogue de configuration d’un écran de veille comprend généralement un bouton **aide** .</span><span class="sxs-lookup"><span data-stu-id="7a25c-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="7a25c-231">Les applications de l’écran de veille peuvent Rechercher l’identificateur du bouton d’aide et appeler la fonction [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) de la même façon que dans d’autres applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7a25c-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 