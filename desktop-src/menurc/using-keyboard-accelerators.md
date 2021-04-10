---
title: Utilisation des accélérateurs clavier
description: Cette section traite des tâches associées aux accélérateurs de clavier.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- entrée d’utilisateur, accélérateurs de clavier
- capture de l’entrée utilisateur, accélérateurs de clavier
- accélérateurs de clavier
- accélérateurs
- tables d’accélérateurs
- ressources de table d’accélérateurs
- fonction d’accélérateur translate
- Message WM_COMMAND
- WM_SYS message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031227"
---
# <a name="using-keyboard-accelerators"></a>Utilisation des accélérateurs clavier

Cette section traite des tâches associées aux accélérateurs de clavier.

-   [Utilisation d’une ressource de table d’accélérateurs](#using-an-accelerator-table-resource)
    -   [Création de la ressource de table d’accélérateurs](#creating-the-accelerator-table-resource)
    -   [Chargement de la ressource de table d’accélérateurs](#loading-the-accelerator-table-resource)
    -   [Appel de la fonction d’accélérateur translate](#calling-the-translate-accelerator-function)
    -   [Traitement des \_ messages de commande WM](/windows)
    -   [Destruction de la ressource de table d’accélérateurs](#destroying-the-accelerator-table-resource)
    -   [Création d’accélérateurs pour les attributs de police](#creating-accelerators-for-font-attributes)
-   [Utilisation d’une table d’accélérateurs créée au moment de l’exécution](#using-an-accelerator-table-created-at-run-time)
    -   [Création d’une table d’accélérateurs Run-Time](#creating-a-run-time-accelerator-table)
    -   [Accélérateurs de traitement](#processing-accelerators)
    -   [Destruction d’une table d’accélérateurs de Run-Time](#destroying-a-run-time-accelerator-table)
    -   [Création d’accélérateurs modifiables par l’utilisateur](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Utilisation d’une ressource de table d’accélérateurs

La méthode la plus courante pour ajouter la prise en charge des accélérateurs à une application consiste à inclure une ressource de table d’accélérateurs avec le fichier exécutable de l’application, puis à charger la ressource au moment de l’exécution.

Cette section couvre les rubriques suivantes :

-   [Création de la ressource de table d’accélérateurs](#creating-the-accelerator-table-resource)
-   [Chargement de la ressource de table d’accélérateurs](#loading-the-accelerator-table-resource)
-   [Appel de la fonction d’accélérateur translate](#calling-the-translate-accelerator-function)
-   [Traitement des \_ messages de commande WM](/windows)
-   [Destruction de la ressource de table d’accélérateurs](#destroying-the-accelerator-table-resource)
-   [Création d’accélérateurs pour les attributs de police](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Création de la ressource de table d’accélérateurs

Vous créez une ressource de table d’accélérateurs à l’aide de [l’instruction Accelerators dans le fichier](./accelerators-resource.md) de définition de ressource de votre application. Vous devez affecter un nom ou un identificateur de ressource à la table d’accélérateurs, de préférence à la différence de toute autre ressource. Le système utilise cet identificateur pour charger la ressource au moment de l’exécution.

Chaque accélérateur que vous définissez requiert une entrée distincte dans la table d’accélérateurs. Dans chaque entrée, vous définissez la séquence de touches (un code de caractère ASCII ou un code de clé virtuelle) qui génère l’accélérateur et l’identificateur de l’accélérateur. Vous devez également spécifier si la séquence de touches doit être utilisée dans une combinaison avec les touches ALT, Maj ou CTRL. Pour plus d’informations sur les clés virtuelles, consultez [entrée au clavier](/windows/desktop/inputdev/keyboard-input).

Une séquence de touches ASCII est spécifiée en plaçant le caractère ASCII entre des guillemets doubles ou en utilisant la valeur entière du caractère en combinaison avec l’indicateur ASCII. Les exemples suivants montrent comment définir des accélérateurs ASCII.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Une séquence de touches de code de touche virtuelle est spécifiée différemment selon que la séquence de touches est une clé alphanumérique ou une clé non alphanumérique. Pour une clé alphanumérique, la lettre ou le chiffre de la clé, placé entre guillemets doubles, est combiné avec l’indicateur **VIRTKEY** . Pour une clé non alphanumérique, le code de la clé virtuelle pour la clé spécifique est combiné avec l’indicateur **VIRTKEY** . Les exemples suivants montrent comment définir des accélérateurs de code de clé virtuelle.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

L’exemple suivant montre une ressource de table d’accélérateurs qui définit des accélérateurs pour les opérations de fichier. Le nom de la ressource est *FileAccel*.

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Si vous souhaitez que l’utilisateur appuie sur les touches ALT, Maj ou CTRL dans une combinaison avec la touche d’accès rapide, spécifiez les indicateurs ALT, Maj et contrôle dans la définition de l’accélérateur. Voici quelques exemples.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

Par défaut, lorsqu’une touche d’accès rapide correspond à un élément de menu, le système met en surbrillance l’élément de menu. Vous pouvez utiliser l’indicateur **noinverse** pour empêcher la mise en surbrillance d’un accélérateur individuel. L’exemple suivant montre comment utiliser l’indicateur **noinverse** :

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Pour définir des accélérateurs qui correspondent à des éléments de menu dans votre application, incluez les accélérateurs dans le texte des éléments de menu. L’exemple suivant montre comment inclure des accélérateurs dans un texte d’élément de menu dans un fichier de définition de ressource.

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a>Chargement de la ressource de table d’accélérateurs

Une application charge une ressource de table d’accélérateurs en appelant la fonction [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) et en spécifiant le handle d’instance pour l’application dont le fichier exécutable contient la ressource, ainsi que le nom ou l’identificateur de la ressource. **LoadAccelerators** charge la table d’accélérateurs spécifiée en mémoire et retourne le handle de la table d’accélérateurs.

Une application peut charger une ressource de table d’accélérateurs à tout moment. En règle générale, une application à thread unique charge sa table d’accélérateurs avant d’entrer dans sa boucle de message principale. Une application qui utilise plusieurs threads charge généralement la ressource de table d’accélérateurs pour un thread avant d’entrer dans la boucle de message pour le thread. Une application ou un thread peut également utiliser plusieurs tables d’accélérateurs, chacune associée à une fenêtre particulière dans l’application. Une telle application chargera la table d’accélérateurs pour la fenêtre chaque fois que l’utilisateur activera la fenêtre. Pour plus d’informations sur les threads, consultez [processus et threads](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Appel de la fonction d’accélérateur translate

Pour traiter les accélérateurs, la boucle de message d’une application (ou du thread) doit contenir un appel à la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . **TranslateAccelerator** compare les séquences de touches à une table d’accélérateurs et, s’il trouve une correspondance, traduit les séquences de touches en un message de [**\_ commande WM**](wm-command.md) (ou [**WM \_ SYSCOMMAND**](wm-syscommand.md)). La fonction envoie ensuite le message à une procédure de fenêtre. Les paramètres de la fonction **TranslateAccelerator** incluent le descripteur de la fenêtre qui doit recevoir les messages de **\_ commande WM** , le handle vers la table d’accélérateurs utilisée pour convertir les accélérateurs et un pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) contenant un message de la file d’attente. L’exemple suivant montre comment appeler **TranslateAccelerator** à partir d’une boucle de message.


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a>Traitement des \_ messages de commande WM

Quand un accélérateur est utilisé, la fenêtre spécifiée dans la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) reçoit une [**\_ commande WM**](wm-command.md) ou un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Le mot de poids faible du paramètre *wParam* contient l’identificateur de l’accélérateur. La procédure de fenêtre examine l’identificateur pour déterminer la source du message de **\_ commande WM** et traiter le message en conséquence.

En règle générale, si un accélérateur correspond à un élément de menu dans l’application, l’accélérateur et l’élément de menu se voient attribuer le même identificateur. Si vous avez besoin de savoir si un message de [**\_ commande WM**](wm-command.md) a été généré par un accélérateur ou par un élément de menu, vous pouvez examiner le mot de poids fort du paramètre *wParam* . Si un accélérateur a généré le message, le mot de poids fort est 1 ; Si un élément de menu a généré le message, le mot de poids fort est 0.

### <a name="destroying-the-accelerator-table-resource"></a>Destruction de la ressource de table d’accélérateurs

Le système détruit automatiquement les ressources de table d’accélérateurs chargées par la fonction [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , en supprimant la ressource de la mémoire après la fermeture de l’application.

### <a name="creating-accelerators-for-font-attributes"></a>Création d’accélérateurs pour les attributs de police

L’exemple de cette section montre comment effectuer les tâches suivantes :

-   Créez une ressource de table d’accélérateurs.
-   Chargez la table d’accélérateurs au moment de l’exécution.
-   Traduisez des accélérateurs dans une boucle de message.
-   Traitez les messages de [**\_ commande WM**](wm-command.md) générés par les accélérateurs.

Ces tâches sont démontrées dans le contexte d’une application qui comprend un menu de **caractères** et des accélérateurs correspondants qui permettent à l’utilisateur de sélectionner les attributs de la police actuelle.

La partie suivante d’un fichier de définition de ressource définit le menu **caractère** et la table d’accélérateurs associée. Notez que les éléments de menu affichent les séquences de touches d’accélérateur et que chaque accélérateur a le même identificateur que son élément de menu associé.


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



Les sections suivantes du fichier source de l’application montrent comment implémenter les accélérateurs.


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a>Utilisation d’une table d’accélérateurs créée au moment de l’exécution

Cette rubrique explique comment utiliser des tables d’accélérateurs créées au moment de l’exécution.

-   [Création d’une table d’accélérateurs Run-Time](#creating-a-run-time-accelerator-table)
-   [Accélérateurs de traitement](#processing-accelerators)
-   [Destruction d’une table d’accélérateurs de Run-Time](#destroying-a-run-time-accelerator-table)
-   [Création d’accélérateurs modifiables par l’utilisateur](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Création d’une table d’accélérateurs Run-Time

La première étape de la création d’une table d’accélérateurs au moment de l’exécution est le remplissage d’un tableau de structures d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) . Chaque structure du tableau définit un accélérateur dans la table. La définition d’un accélérateur comprend ses indicateurs, sa clé et son identificateur. La structure d' **accélération** se présente sous la forme suivante.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Vous définissez la séquence de touches d’un accélérateur en spécifiant un code de caractère ASCII ou une clé virtuelle dans le membre **clé** de la structure d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) . Si vous spécifiez un code de clé virtuelle, vous devez d’abord inclure l’indicateur **FVIRTKEY** dans le membre **fVirt** ; dans le cas contraire, le système interprète le code comme un code de caractère ASCII. Vous pouvez inclure l’indicateur **FCONTROL**, **Falt** ou **FSHIFT** , ou les trois, pour combiner la touche Ctrl, ALT ou Maj avec la séquence de touches.

Pour créer la table d’accélérateurs, transmettez un pointeur vers le tableau de structures d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) à la fonction [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . **CreateAcceleratorTable** crée la table d’accélérateurs et retourne le descripteur à la table.

### <a name="processing-accelerators"></a>Accélérateurs de traitement

Le processus de chargement et d’appel des accélérateurs fournis par une table d’accélérateurs créée au moment de l’exécution est identique au traitement de ceux fournis par une ressource de table d’accélérateurs. Pour plus d’informations, consultez [chargement de la ressource de table d’accélérateurs via le traitement des](#loading-the-accelerator-table-resource) messages de [ \_ commande WM](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Destruction d’une table d’accélérateurs de Run-Time

Le système détruit automatiquement les tables d’accélérateurs créées au moment de l’exécution, en supprimant les ressources de la mémoire après la fermeture de l’application. Vous pouvez détruire une table d’accélérateurs et la supprimer de la mémoire plus tôt en passant le handle de la table à la fonction [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

### <a name="creating-user-editable-accelerators"></a>Création d’accélérateurs modifiables par l’utilisateur

Cet exemple montre comment construire une boîte de dialogue qui permet à l’utilisateur de modifier l’accélérateur associé à un élément de menu. La boîte de dialogue se compose d’une zone de liste déroulante contenant des éléments de menu, d’une zone de liste déroulante contenant les noms des clés et de cases à cocher permettant de sélectionner les touches CTRL, ALT et Maj. L’illustration suivante montre la boîte de dialogue.

![boîte de dialogue avec des zones de liste déroulante et des cases à cocher](images/useredit.gif)

L’exemple suivant montre comment la boîte de dialogue est définie dans le fichier de définition de ressource.

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

La barre de menus de l’application contient un sous-menu de **caractères** dont les éléments sont associés à des accélérateurs.

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

Les valeurs d’élément de menu du modèle de menu sont des constantes définies comme suit dans le fichier d’en-tête de l’application.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

La boîte de dialogue utilise un tableau de structures VKEY définies par l’application, chacune contenant une chaîne de texte de frappe et une chaîne de texte d’accélérateur. Lorsque la boîte de dialogue est créée, elle analyse le tableau et ajoute chaque chaîne de texte de frappe à la zone de liste déroulante **Sélectionner une séquence de touches** . Quand l’utilisateur clique sur le bouton **OK** , la boîte de dialogue recherche la chaîne de texte de frappe sélectionnée et récupère la chaîne de texte d’accélérateur correspondante. La boîte de dialogue ajoute la chaîne de texte d’accélérateur au texte de l’élément de menu sélectionné par l’utilisateur. L’exemple suivant montre le tableau de structures VKEY :


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



La procédure d’initialisation de la boîte de dialogue remplit l' **élément sélectionné** et sélectionne des zones de liste déroulante de **frappe** . Une fois que l’utilisateur a sélectionné un élément de menu et un accélérateur associé, la boîte de dialogue examine les contrôles dans la boîte de dialogue pour obtenir la sélection de l’utilisateur, met à jour le texte de l’élément de menu, puis crée une nouvelle table d’accélérateurs qui contient le nouvel accélérateur défini par l’utilisateur. L’exemple suivant illustre la procédure de la boîte de dialogue. Notez que vous devez initialiser dans votre procédure de fenêtre.


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 