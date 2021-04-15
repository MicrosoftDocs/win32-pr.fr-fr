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
# <a name="disabling-shortcut-keys-in-games"></a>Désactivation des touches de raccourci dans les jeux

Cet article explique comment désactiver temporairement les raccourcis clavier dans Microsoft Windows pour éviter toute interruption de jeu pour les jeux en mode plein écran. La touche Maj et la touche CTRL sont souvent utilisées comme boutons de déclenchement ou d’exécution dans les jeux. Si les utilisateurs appuient accidentellement sur la touche Windows (situés près de ces touches), ils peuvent se rendre soudains à l’application, ce qui Ruins l’expérience du jeu. En utilisant simplement la touche Maj comme bouton de jeu, vous pouvez exécuter par inadvertance le raccourci touches rémanentes qui peut afficher une boîte de dialogue d’avertissement. Pour éviter ces problèmes, vous devez désactiver ces clés lorsqu’elles s’exécutent en mode plein écran et les réactiver à leurs gestionnaires par défaut en cas d’exécution en mode fenêtre ou quitter l’application.

Cet article explique comment effectuer les opérations suivantes :

-   [Désactiver la touche Windows à l’aide d’un crochet clavier](#disable-the-windows-key-with-a-keyboard-hook)
-   [Désactiver les touches de raccourci d’accessibilité](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>Désactiver la touche Windows à l’aide d’un crochet clavier

Utilisez un crochet de clavier de bas niveau pour filtrer la clé Windows du traitement. Le crochet de clavier de bas niveau illustré dans l’exemple 1 reste en vigueur même si un utilisateur réduit la fenêtre ou bascule vers une autre application. Cela signifie que vous devez veiller à ce que la touche Windows ne soit pas désactivée lorsque l’application est désactivée. Pour ce faire, le code de l’exemple 1 gère le \_ message WM ACTIVATEAPP.

> [!Note]  
> Cette méthode fonctionne sur Windows 2000 et les versions ultérieures de Windows. Cette méthode fonctionne également avec les comptes d’utilisateur dotés de privilèges minimum (également appelés comptes d’utilisateur limité).

 

Cette méthode est utilisée par DXUT et est illustrée dans l’exemple de code suivant.

**Exemple 1 : Utilisation d’un crochet de clavier de bas niveau pour désactiver la touche Windows**


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



## <a name="disable-the-accessibility-shortcut-keys"></a>Désactiver les touches de raccourci d’accessibilité

Windows comprend des fonctionnalités d’accessibilité telles que les touches rémanentes, les touches filtres et les touches [d'](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))accès. Chacun d’eux a un objectif différent ; Par exemple, la touche rémanente est conçue pour les personnes qui éprouvent des difficultés à maintenir simultanément deux clés ou plus. Chacune de ces fonctionnalités d’accessibilité possède également un raccourci clavier qui permet d’activer ou de désactiver la fonctionnalité. Par exemple, le raccourci touches rémanentes est déclenché en appuyant cinq fois sur la touche Maj. Si la touche Maj est également utilisée dans le jeu, l’utilisateur peut déclencher accidentellement ce raccourci pendant la lecture du jeu. Quand le raccourci est déclenché, Windows (par défaut) affiche un avertissement dans une boîte de dialogue, ce qui fait que Windows réduit le jeu s’exécutant en mode plein écran. Cela peut bien sûr avoir un effet considérable sur le jeu.

Les fonctionnalités d’accessibilité sont requises pour certains clients et n’interfèrent pas eux-mêmes avec les jeux en plein écran. par conséquent, vous ne devez pas modifier les paramètres d’accessibilité. Toutefois, étant donné que les raccourcis des fonctionnalités d’accessibilité peuvent perturber la lecture du jeu en cas de déclenchement accidentel, vous devez désactiver un raccourci d’accessibilité uniquement lorsque cette fonctionnalité n’est pas activée en appelant [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).

Un raccourci d’accessibilité désactivé par [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) reste désactivé même après la fermeture de l’application. Cela signifie que vous devez restaurer les paramètres avant de quitter l’application. Étant donné qu’il est possible que l’application ne s’arrête pas correctement, vous devez écrire ces paramètres dans un stockage persistant afin qu’ils puissent être restaurés lorsque l’application est réexécutée. Vous pouvez également utiliser un gestionnaire d’exceptions pour restaurer ces paramètres si un incident se produit.

**Pour désactiver ces raccourcis**

1.  Capturer les paramètres d’accessibilité actuels avant de les désactiver.
2.  Désactivez le raccourci d’accessibilité lorsque l’application passe en mode plein écran si la fonctionnalité d’accessibilité est désactivée.
3.  Restaurez les paramètres d’accessibilité lorsque l’application passe en mode fenêtre ou se ferme.

Cette méthode est utilisée dans DXUT et est illustrée dans l’exemple de code suivant.

> [!Note]  
> Cette méthode fonctionne lors de l’exécution sur un compte d’utilisateur limité.

 

**Exemple 2 : Désactivation des touches de raccourci d’accessibilité**


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



 

 