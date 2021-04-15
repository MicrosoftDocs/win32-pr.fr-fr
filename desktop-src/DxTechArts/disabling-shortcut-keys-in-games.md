---
title: Désactivation des touches de raccourci dans les jeux
description: Cet article explique comment désactiver temporairement les raccourcis clavier dans Microsoft Windows pour éviter toute interruption de jeu pour les jeux en mode plein écran.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463350"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="af8ca-103">Désactivation des touches de raccourci dans les jeux</span><span class="sxs-lookup"><span data-stu-id="af8ca-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="af8ca-104">Cet article explique comment désactiver temporairement les raccourcis clavier dans Microsoft Windows pour éviter toute interruption de jeu pour les jeux en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="af8ca-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="af8ca-105">La touche Maj et la touche CTRL sont souvent utilisées comme boutons de déclenchement ou d’exécution dans les jeux.</span><span class="sxs-lookup"><span data-stu-id="af8ca-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="af8ca-106">Si les utilisateurs appuient accidentellement sur la touche Windows (situés près de ces touches), ils peuvent se rendre soudains à l’application, ce qui Ruins l’expérience du jeu.</span><span class="sxs-lookup"><span data-stu-id="af8ca-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="af8ca-107">En utilisant simplement la touche Maj comme bouton de jeu, vous pouvez exécuter par inadvertance le raccourci touches rémanentes qui peut afficher une boîte de dialogue d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="af8ca-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="af8ca-108">Pour éviter ces problèmes, vous devez désactiver ces clés lorsqu’elles s’exécutent en mode plein écran et les réactiver à leurs gestionnaires par défaut en cas d’exécution en mode fenêtre ou quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="af8ca-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="af8ca-109">Cet article explique comment effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="af8ca-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="af8ca-110">Désactiver la touche Windows à l’aide d’un crochet clavier</span><span class="sxs-lookup"><span data-stu-id="af8ca-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="af8ca-111">Désactiver les touches de raccourci d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="af8ca-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="af8ca-112">Désactiver la touche Windows à l’aide d’un crochet clavier</span><span class="sxs-lookup"><span data-stu-id="af8ca-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="af8ca-113">Utilisez un crochet de clavier de bas niveau pour filtrer la clé Windows du traitement.</span><span class="sxs-lookup"><span data-stu-id="af8ca-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="af8ca-114">Le crochet de clavier de bas niveau illustré dans l’exemple 1 reste en vigueur même si un utilisateur réduit la fenêtre ou bascule vers une autre application.</span><span class="sxs-lookup"><span data-stu-id="af8ca-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="af8ca-115">Cela signifie que vous devez veiller à ce que la touche Windows ne soit pas désactivée lorsque l’application est désactivée.</span><span class="sxs-lookup"><span data-stu-id="af8ca-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="af8ca-116">Pour ce faire, le code de l’exemple 1 gère le \_ message WM ACTIVATEAPP.</span><span class="sxs-lookup"><span data-stu-id="af8ca-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="af8ca-117">Cette méthode fonctionne sur Windows 2000 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="af8ca-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="af8ca-118">Cette méthode fonctionne également avec les comptes d’utilisateur dotés de privilèges minimum (également appelés comptes d’utilisateur limité).</span><span class="sxs-lookup"><span data-stu-id="af8ca-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="af8ca-119">Cette méthode est utilisée par DXUT et est illustrée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="af8ca-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="af8ca-120">**Exemple 1 : Utilisation d’un crochet de clavier de bas niveau pour désactiver la touche Windows**</span><span class="sxs-lookup"><span data-stu-id="af8ca-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="af8ca-121">Désactiver les touches de raccourci d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="af8ca-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="af8ca-122">Windows comprend des fonctionnalités d’accessibilité telles que les touches rémanentes, les touches filtres et les touches [d'](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))accès.</span><span class="sxs-lookup"><span data-stu-id="af8ca-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="af8ca-123">Chacun d’eux a un objectif différent ; Par exemple, la touche rémanente est conçue pour les personnes qui éprouvent des difficultés à maintenir simultanément deux clés ou plus.</span><span class="sxs-lookup"><span data-stu-id="af8ca-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="af8ca-124">Chacune de ces fonctionnalités d’accessibilité possède également un raccourci clavier qui permet d’activer ou de désactiver la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="af8ca-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="af8ca-125">Par exemple, le raccourci touches rémanentes est déclenché en appuyant cinq fois sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="af8ca-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="af8ca-126">Si la touche Maj est également utilisée dans le jeu, l’utilisateur peut déclencher accidentellement ce raccourci pendant la lecture du jeu.</span><span class="sxs-lookup"><span data-stu-id="af8ca-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="af8ca-127">Quand le raccourci est déclenché, Windows (par défaut) affiche un avertissement dans une boîte de dialogue, ce qui fait que Windows réduit le jeu s’exécutant en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="af8ca-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="af8ca-128">Cela peut bien sûr avoir un effet considérable sur le jeu.</span><span class="sxs-lookup"><span data-stu-id="af8ca-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="af8ca-129">Les fonctionnalités d’accessibilité sont requises pour certains clients et n’interfèrent pas eux-mêmes avec les jeux en plein écran. par conséquent, vous ne devez pas modifier les paramètres d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="af8ca-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="af8ca-130">Toutefois, étant donné que les raccourcis des fonctionnalités d’accessibilité peuvent perturber la lecture du jeu en cas de déclenchement accidentel, vous devez désactiver un raccourci d’accessibilité uniquement lorsque cette fonctionnalité n’est pas activée en appelant [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="af8ca-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="af8ca-131">Un raccourci d’accessibilité désactivé par [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) reste désactivé même après la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="af8ca-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="af8ca-132">Cela signifie que vous devez restaurer les paramètres avant de quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="af8ca-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="af8ca-133">Étant donné qu’il est possible que l’application ne s’arrête pas correctement, vous devez écrire ces paramètres dans un stockage persistant afin qu’ils puissent être restaurés lorsque l’application est réexécutée.</span><span class="sxs-lookup"><span data-stu-id="af8ca-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="af8ca-134">Vous pouvez également utiliser un gestionnaire d’exceptions pour restaurer ces paramètres si un incident se produit.</span><span class="sxs-lookup"><span data-stu-id="af8ca-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="af8ca-135">**Pour désactiver ces raccourcis**</span><span class="sxs-lookup"><span data-stu-id="af8ca-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="af8ca-136">Capturer les paramètres d’accessibilité actuels avant de les désactiver.</span><span class="sxs-lookup"><span data-stu-id="af8ca-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="af8ca-137">Désactivez le raccourci d’accessibilité lorsque l’application passe en mode plein écran si la fonctionnalité d’accessibilité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="af8ca-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="af8ca-138">Restaurez les paramètres d’accessibilité lorsque l’application passe en mode fenêtre ou se ferme.</span><span class="sxs-lookup"><span data-stu-id="af8ca-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="af8ca-139">Cette méthode est utilisée dans DXUT et est illustrée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="af8ca-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="af8ca-140">Cette méthode fonctionne lors de l’exécution sur un compte d’utilisateur limité.</span><span class="sxs-lookup"><span data-stu-id="af8ca-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="af8ca-141">**Exemple 2 : Désactivation des touches de raccourci d’accessibilité**</span><span class="sxs-lookup"><span data-stu-id="af8ca-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 