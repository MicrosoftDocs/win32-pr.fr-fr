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
# <a name="handling-screen-savers"></a>Gestion des économiseurs d’écran

L’API Microsoft Win32 prend en charge des applications spéciales appelées *économiseurs d’écran*. Les économiseurs d’écran démarrent lorsque la souris et le clavier sont restés inactifs pendant une période spécifiée. Ils sont utilisés pour les deux raisons suivantes :

-   Pour protéger un écran de la gravure de phosphore provoquée par les images statiques.
-   Pour masquer les informations sensibles laissées sur un écran.

Cette rubrique est composée des sections suivantes.

-   [À propos des économiseurs d’écran](#about-screen-savers)
-   [Utilisation des fonctions d’économiseur d’écran](#using-the-screen-saver-functions)
    -   [Création d’un écran de veille](#creating-a-screen-saver)
    -   [Installation des nouveaux économiseurs d’écran](#installing-new-screen-savers)
    -   [Ajout de l’aide à la boîte de dialogue Configuration de l’écran de veille](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>À propos des économiseurs d’écran

L’application de bureau dans le panneau de configuration Windows permet aux utilisateurs de sélectionner dans une liste d’économiseurs d’écran, de spécifier le temps qui doit s’écouler avant le démarrage de l’économiseur d’écran, de configurer des économiseurs d’écran et d’afficher un aperçu des économiseurs d’écran. Les économiseurs d’écran sont chargés automatiquement au démarrage de Windows ou lorsqu’un utilisateur active l’économiseur d’écran par le biais du panneau de configuration.

Une fois qu’un économiseur d’écran est choisi, Windows surveille les séquences de touches et les mouvements de la souris, puis démarre l’écran de veille après une période d’inactivité. Toutefois, Windows ne démarre pas l’économiseur d’écran si l’une des conditions suivantes est remplie :

-   L’application active n’est pas une application Windows.
-   Une fenêtre de formation basée sur l’ordinateur (CBT) est présente.
-   L’application active reçoit le message [WM \_ SYSCOMMAND](../menurc/wm-syscommand.md) avec le paramètre *wParam* défini sur la valeur SC \_ SCREENSAVE, mais il ne transmet pas le message à la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

**Contexte de sécurité de l’écran de veille**

Le contexte de sécurité de l’écran de veille dépend du fait qu’un utilisateur ait ouvert une session interactive. Si un utilisateur est connecté de manière interactive lorsque l’économiseur d’écran est appelé, l’économiseur d’écran s’exécute dans le contexte de sécurité de l’utilisateur interactif. Si aucun utilisateur n’est connecté, le contexte de sécurité de l’écran de veille dépend de la version de Windows utilisée.

-   Windows XP et Windows 2000-l’économiseur d’écran s’exécute dans le contexte de LocalSystem avec les comptes restreints.
-   Windows 2003-l’économiseur d’écran s’exécute dans le contexte de LocalService avec tous les privilèges supprimés et le groupe administrateurs désactivé.
-   Ne s’applique pas à Windows NT4.

Le contexte de sécurité détermine le niveau des opérations privilégiées qui peuvent être effectuées à partir d’un écran de veille.

**Windows Vista et versions ultérieures :** Si la protection par mot de passe est activée par la stratégie, l’économiseur d’écran est démarré indépendamment de ce que fait une application avec la \_ notification SC SCREENSAVE.

Les économiseurs d’écran contiennent des fonctions exportées spécifiques, des définitions de ressource et des déclarations de variables. La bibliothèque de l’économiseur d’écran contient la fonction **principale** et le code de démarrage requis pour un économiseur d’écran. Lorsqu’un économiseur d’écran démarre, le code de démarrage de la bibliothèque de l’écran de veille crée une fenêtre plein écran. La classe de fenêtre pour cette fenêtre est déclarée comme suit :


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



Pour créer un écran de veille, la plupart des développeurs créent un module de code source contenant trois fonctions requises et les lient à la bibliothèque de l’écran de veille. Un module d’économiseur d’écran est uniquement responsable de la configuration et de la fourniture d’effets visuels.

L’une des trois fonctions requises dans un module d’économiseur d’écran est [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Cette fonction traite des messages spécifiques et renvoie tous les messages non traités à la bibliothèque de l’écran de veille. Voici quelques-uns des messages classiques traités par **ScreenSaverProc**.



| Message        | Signification                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| création de WM \_     | Récupérez les données d’initialisation à partir du fichier Regedit.ini. Définissez un minuteur de fenêtre pour la fenêtre de l’écran de veille. Effectuez toute autre initialisation requise.                                     |
| \_ERASEBKGND WM | Effacez la fenêtre de l’écran de veille et préparez-vous aux opérations de dessin suivantes.                                                                                                               |
| \_minuteur WM      | Effectuer des opérations de dessin.                                                                                                                                                                |
| \_destructeur WM    | Détruisez les minuteurs créés lorsque l’application a traité le message [WM \_ Create](../winmsg/wm-create.md) . Effectuez tout nettoyage supplémentaire requis. |



 

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) transmet les messages non traités à la bibliothèque de l’écran de veille en appelant la fonction [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Le tableau suivant décrit comment cette fonction traite différents messages.



| Message         | Action                                                                    |
|-----------------|---------------------------------------------------------------------------|
| \_SETCURSOR WM   | Définissez le curseur sur le curseur null, en le supprimant de l’écran.           |
| \_peinture WM       | Peindre l’arrière-plan de l’écran.                                              |
| \_LBUTTONDOWN WM | Mettre fin à l’économiseur d’écran.                                               |
| \_MBUTTONDOWN WM | Mettre fin à l’économiseur d’écran.                                               |
| \_RBUTTONDOWN WM | Mettre fin à l’économiseur d’écran.                                               |
| WM- \_ touche     | Mettre fin à l’économiseur d’écran.                                               |
| WM \_ MOUSEMOVE   | Mettre fin à l’économiseur d’écran.                                               |
| activation de WM \_    | Met fin à l’économiseur d’écran si le paramètre *wParam* est défini sur **false**. |



 

La deuxième fonction requise dans un module d’économiseur d’écran est [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Cette fonction affiche une boîte de dialogue qui permet à l’utilisateur de configurer l’économiseur d’écran (une application doit fournir un modèle de boîte de dialogue correspondant). Windows affiche la boîte de dialogue de configuration lorsque l’utilisateur sélectionne le bouton **configurer** dans la boîte de dialogue économiseur d’écran du panneau de configuration.

La troisième fonction requise dans un module d’économiseur d’écran est [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses). Cette fonction doit être appelée par toutes les applications de l’écran de veille. Toutefois, les applications qui ne nécessitent pas de contrôles personnalisés ou Windows spéciaux dans la boîte de dialogue de configuration peuvent simplement retourner la **valeur true**. Les applications nécessitant des contrôles personnalisés ou des fenêtres spéciales doivent utiliser cette fonction pour inscrire les classes de fenêtre correspondantes.

En plus de créer un module qui prend en charge les trois fonctions qui viennent d’être décrites, un écran de veille doit fournir une icône. Cette icône est visible uniquement lorsque l’économiseur d’écran est exécuté en tant qu’application autonome. (Pour qu’il soit exécuté par le panneau de configuration, un économiseur d’écran doit avoir l’extension de nom de fichier. SCR ; pour être exécuté en tant qu’application autonome, il doit avoir l’extension de nom de fichier. exe.) L’icône doit être identifiée dans le fichier de ressources de l’écran de veille par l’application d’ID de constante \_ , qui est définie dans le fichier d’en-tête scrnsave. h.

Une dernière exigence est une chaîne de description de l’économiseur d’écran. Le fichier de ressources d’un économiseur d’écran doit contenir une chaîne que le panneau de configuration affiche comme nom de l’économiseur d’écran. La chaîne de description doit être la première chaîne dans la table de chaînes du fichier de ressources (identifiée par la valeur ordinale 1). Toutefois, la chaîne de description est ignorée par le panneau de configuration si l’économiseur d’écran a un nom de fichier long. Dans ce cas, le nom de fichier sera utilisé comme chaîne de description.

## <a name="using-the-screen-saver-functions"></a>Utilisation des fonctions d’économiseur d’écran

Cette section utilise un exemple de code tiré d’une application d’écran de veille pour illustrer les tâches suivantes :

-   [Création d’un écran de veille](#creating-a-screen-saver)
-   [Installation des nouveaux économiseurs d’écran](#installing-new-screen-savers)
-   [Ajout de l’aide à la boîte de dialogue Configuration de l’écran de veille](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Création d’un écran de veille

À intervalles allant de 1 à 10 secondes, l’application dans cet exemple repeint l’écran avec l’une des quatre couleurs suivantes : blanc, gris clair, gris foncé et noir. L’application peint l’écran chaque fois qu’il reçoit un message de [ \_ minuteur WM](../winmsg/wm-timer.md) . L’utilisateur peut régler l’intervalle auquel ce message est envoyé en sélectionnant la boîte de dialogue de configuration de l’application et en ajustant une barre de défilement horizontale.

### <a name="screen-saver-library"></a>Bibliothèque de l’écran de veille

Les fonctions d’économiseur d’écran statiques sont contenues dans la bibliothèque de l’écran de veille. Deux versions de la bibliothèque sont disponibles : scrnsave. lib et Scrnsavw. lib. Vous devez lier votre projet avec l’un de ces. Scrnsave. lib est utilisé pour les économiseurs d’écran qui utilisent des caractères ANSI et Scrnsavw. lib est utilisé pour les économiseurs d’écran qui utilisent des caractères Unicode. Un économiseur d’écran qui est lié à Scrnsavw. lib s’exécutera uniquement sur les plateformes Windows qui prennent en charge Unicode, tandis qu’un économiseur d’écran lié à scrnsave. lib s’exécutera sur toute plateforme Windows.

### <a name="supporting-the-configuration-dialog-box"></a>Prise en charge de la boîte de dialogue de configuration

La plupart des économiseurs d’écran fournissent une boîte de dialogue de configuration pour permettre à l’utilisateur de spécifier des données de personnalisation, telles que des couleurs uniques, des vitesses de dessin, l’épaisseur de ligne, les polices, etc. Pour prendre en charge la boîte de dialogue de configuration, l’application doit fournir un modèle de boîte de dialogue et doit également prendre en charge la fonction [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) . Voici le modèle de boîte de dialogue pour l’exemple d’application.


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



Vous devez définir la constante utilisée pour identifier le modèle de boîte de dialogue à l’aide de la valeur décimale 2003, comme dans l’exemple suivant :


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



L’exemple suivant illustre la fonction [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) trouvée dans l’exemple d’application.


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



En plus de fournir le modèle de boîte de dialogue et de prendre en charge la fonction [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , une application doit également prendre en charge la fonction [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) . Cette fonction inscrit toutes les classes de fenêtre non standard requises par l’économiseur d’écran. Étant donné que l’exemple d’application a utilisé uniquement des classes de fenêtre standard dans sa procédure de boîte de dialogue, cette fonction retourne simplement **true**, comme dans l’exemple suivant :


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Prise en charge de la procédure de fenêtre de l’écran de veille

Chaque écran de veille doit prendre en charge une procédure de fenêtre nommée [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). À l’instar de la plupart des procédures de fenêtre, **ScreenSaverProc** traite un ensemble de messages spécifiques et transmet les messages non traités à une procédure par défaut. Toutefois, au lieu de les transmettre à la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , **ScreenSaverProc** passe des messages non traités à la fonction [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Une autre différence entre **ScreenSaverProc** et une procédure de fenêtre normale est que le handle passé à **ScreenSaverProc** identifie l’intégralité du Bureau plutôt qu’une fenêtre cliente. L’exemple suivant illustre la procédure de fenêtre **ScreenSaverProc** pour l’exemple d’économiseur d’écran.


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



### <a name="creating-a-module-definition-file"></a>Création d’un fichier de définition de module

Les fonctions [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) et [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) doivent être exportées dans le fichier de définition de module de l’application ; Toutefois, [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) ne doit pas être exporté. L’exemple suivant montre le fichier de définition de module pour l’exemple d’application.


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



### <a name="installing-new-screen-savers"></a>Installation des nouveaux économiseurs d’écran

Lors de la compilation de la liste des économiseurs d’écran disponibles, le panneau de configuration recherche dans le répertoire de démarrage Windows les fichiers portant l’extension. scr. Étant donné que les économiseurs d’écran sont des fichiers exécutables Windows standard avec des extensions. exe, vous devez les renommer pour qu’ils aient des extensions. SCR et les copier dans le répertoire approprié.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Ajout de l’aide à la boîte de dialogue Configuration de l’écran de veille

La boîte de dialogue de configuration d’un écran de veille comprend généralement un bouton **aide** . Les applications de l’écran de veille peuvent Rechercher l’identificateur du bouton d’aide et appeler la fonction [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) de la même façon que dans d’autres applications Windows.

 

 