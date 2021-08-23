---
description: Cette section explique comment effectuer des tâches associées à l’interface multidocument.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Utilisation de l’interface multidocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09453e6f4a9301c8cdfc9d675ae1efd7853594fc472a446a021e3bd3e075fc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028327"
---
# <a name="using-the-multiple-document-interface"></a>Utilisation de l’interface multidocument

Cette section explique comment effectuer les tâches suivantes :

-   [Inscription des classes de fenêtre frame et enfant](#registering-child-and-frame-window-classes)
-   [Création du frame et des Windows enfants](#creating-frame-and-child-windows)
-   [Écriture de la boucle de message principale](#writing-the-main-message-loop)
-   [Écriture de la procédure de fenêtre frame](#writing-the-frame-window-procedure)
-   [Écriture de la procédure de fenêtre enfant](#writing-the-child-window-procedure)
-   [Création d’une fenêtre enfant](#creating-a-child-window)

Pour illustrer ces tâches, cette section comprend des exemples de MULTIPAD, une application classique d’interface multidocument (MDI, multiple-document interface).

## <a name="registering-child-and-frame-window-classes"></a>Inscription des classes de fenêtre frame et enfant

Une application MDI classique doit inscrire deux classes de fenêtres : une pour sa fenêtre frame et une pour ses fenêtres enfants. Si une application prend en charge plusieurs types de document (par exemple, une feuille de calcul et un graphique), elle doit inscrire une classe de fenêtre pour chaque type.

La structure de classe de la fenêtre frame est semblable à celle de la fenêtre principale dans les applications non-MDI. La structure de la classe pour les fenêtres enfants MDI diffère légèrement de la structure des fenêtres enfants dans les applications non-MDI, comme suit :

-   La structure de la classe doit avoir une icône, car l’utilisateur peut réduire une fenêtre enfant MDI comme s’il s’agissait d’une fenêtre d’application normale.
-   Le nom du menu doit avoir la **valeur null**, car une fenêtre enfant MDI ne peut pas avoir son propre menu.
-   La structure de la classe doit réserver de l’espace supplémentaire dans la structure de la fenêtre. Avec cet espace, l’application peut associer des données, telles qu’un nom de fichier, à une fenêtre enfant particulière.

L’exemple suivant montre comment MULTIPAD inscrit son frame et les classes de fenêtre enfants.


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a>Création du frame et des Windows enfants

Après avoir inscrit ses classes de fenêtre, une application MDI peut créer ses fenêtres. Tout d’abord, elle crée sa fenêtre frame à l’aide de la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Après avoir créé sa fenêtre frame, l’application crée à nouveau sa fenêtre cliente à l’aide de **CreateWindow** ou de **CreateWindowEx**. L’application doit spécifier MDICLIENT comme nom de classe de la fenêtre cliente ; **MdiClient** est une classe de fenêtre préinscrite définie par le système. Le paramètre *lpvParam* de **CreateWindow** ou **CreateWindowEx** doit pointer vers une structure [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) . Cette structure contient les membres décrits dans le tableau suivant :



| Membre           | Description                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hWindowMenu**  | Handle vers le menu fenêtre utilisé pour contrôler les fenêtres enfants MDI. Lorsque les fenêtres enfants sont créées, l’application ajoute leurs titres au menu fenêtre en tant qu’éléments de menu. L’utilisateur peut ensuite activer une fenêtre enfant en cliquant sur son titre dans le menu fenêtre.                                                               |
| **idFirstChild** | Spécifie l’identificateur de la première fenêtre enfant MDI. Cet identificateur est affecté à la première fenêtre enfant MDI créée. Des fenêtres supplémentaires sont créées avec des identificateurs de fenêtre incrémentés. Quand une fenêtre enfant est détruite, le système réaffecte immédiatement les identificateurs de fenêtre pour maintenir la plage contiguë. |



 

Quand le titre d’une fenêtre enfant est ajouté au menu fenêtre, le système assigne un identificateur à la fenêtre enfant. Quand l’utilisateur clique sur le titre d’une fenêtre enfant, la fenêtre frame reçoit un message de [**\_ commande WM**](../menurc/wm-command.md) avec l’identificateur dans le paramètre *wParam* . Vous devez spécifier une valeur pour le membre **idFirstChild** qui n’est pas en conflit avec les identificateurs d’élément de menu dans le menu de la fenêtre frame.

La procédure de fenêtre frame de MULTIPAD crée la fenêtre cliente MDI lors du traitement du message [**WM \_ Create**](wm-create.md) . L’exemple suivant montre comment la fenêtre cliente est créée.


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



Les titres des fenêtres enfants sont ajoutés au bas du menu fenêtre. Si l’application ajoute des chaînes au menu fenêtre à l’aide de la fonction [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , ces chaînes peuvent être remplacées par les titres des fenêtres enfants lorsque le menu fenêtre est repeint (chaque fois qu’une fenêtre enfant est créée ou détruite). Une application MDI qui ajoute des chaînes à son menu fenêtre doit utiliser la fonction [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) et vérifier que les titres des fenêtres enfants n’ont pas remplacé ces nouvelles chaînes.

Utilisez le style **WS \_ CLIPCHILDREN** pour créer la fenêtre cliente MDI afin d’empêcher la fenêtre de se peindre sur ses fenêtres enfants.

## <a name="writing-the-main-message-loop"></a>Écriture de la boucle de message principale

La boucle de messages principale d’une application MDI est semblable à celle des touches accélérateur de gestion d’applications non-MDI. La différence est que la boucle de message MDI appelle la fonction [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) avant de vérifier les clés d’accélérateur définies par l’application ou avant de distribuer le message.

L’exemple suivant illustre la boucle de message d’une application MDI classique. Notez que [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) peut retourner-1 en cas d’erreur.


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



La fonction [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) traduit les messages de KeyOut [**WM \_**](../inputdev/wm-keydown.md) en messages [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) et les envoie à la fenêtre enfant MDI active. Si le message n’est pas un message d’accélérateur MDI, la fonction retourne **false**. dans ce cas, l’application utilise la fonction [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) pour déterminer si l’une des touches accélérateur définies par l’application a été enfoncée. Si ce n’est pas le cas, la boucle distribue le message à la procédure de fenêtre appropriée.

## <a name="writing-the-frame-window-procedure"></a>Écriture de la procédure de fenêtre frame

La procédure de fenêtre pour une fenêtre frame MDI est semblable à celle d’une fenêtre principale d’une application non-MDI. La différence est qu’une procédure de fenêtre frame transmet tous les messages qu’elle ne gère pas à la fonction [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) plutôt qu’à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . En outre, la procédure de fenêtre frame doit également transmettre certains messages qu’elle gère, y compris ceux qui sont listés dans le tableau suivant.



| Message                                  | Réponse                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM, \_ commande**](../menurc/wm-command.md)     | Active la fenêtre enfant MDI choisie par l’utilisateur. Ce message est envoyé lorsque l’utilisateur choisit une fenêtre enfant MDI dans le menu fenêtre de la fenêtre frame MDI. L’identificateur de fenêtre accompagnant ce message identifie la fenêtre enfant MDI à activer. |
| [**\_MENUCHAR WM**](../menurc/wm-menuchar.md)   | Ouvre le menu fenêtre de la fenêtre enfant MDI active quand l’utilisateur appuie sur la combinaison de touches ALT + – (moins).                                                                                                                                                      |
| [**WM \_ SetFocus**](../inputdev/wm-setfocus.md) | Passe le focus clavier à la fenêtre cliente MDI, qui à son tour la transmet à la fenêtre enfant MDI active.                                                                                                                                                         |
| [**taille du WM \_**](wm-size.md)              | Redimensionne la fenêtre du client MDI pour l’ajuster à la zone cliente de la nouvelle fenêtre frame. Si la procédure de fenêtre frame dimensionne la fenêtre du client MDI à une taille différente, elle ne doit pas passer le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                   |



 

La procédure de fenêtre frame dans MULTIPAD est appelée MPFrameWndProc. La gestion d’autres messages par MPFrameWndProc est similaire à celle des applications non-MDI. [**WM \_**](../menurc/wm-command.md) Les messages de commande dans MULTIPAD sont gérés par la fonction CommandHandler définie localement. Pour les messages de commande MULTIPAD ne gère pas, CommandHandler appelle la fonction [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) . Si MULTIPAD n’utilise pas **DefFrameProc** par défaut, l’utilisateur ne peut pas activer une fenêtre enfant à partir du menu fenêtre, car le message de **\_ commande WM** envoyé en cliquant sur l’élément de menu de la fenêtre est perdu.

## <a name="writing-the-child-window-procedure"></a>Écriture de la procédure de fenêtre enfant

À l’instar de la procédure de fenêtre frame, une procédure de fenêtre enfant MDI utilise une fonction spéciale pour le traitement des messages par défaut. Tous les messages que la procédure de fenêtre enfant ne gère pas doivent être passés à la fonction [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) plutôt qu’à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . En outre, certains messages de gestion de fenêtre doivent être transmis à **DefMDIChildProc**, même si l’application gère le message, afin que l’interface MDI fonctionne correctement. Voici les messages que l’application doit passer à **DefMDIChildProc**.



| Message                                       | Réponse                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CHILDACTIVATE WM**](wm-childactivate.md) | Effectue le traitement de l’activation lorsque les fenêtres enfants MDI sont dimensionnées, déplacées ou affichées. Ce message doit être transmis.                                                                                                                                        |
| [**\_GETMINMAXINFO WM**](wm-getminmaxinfo.md) | Calcule la taille d’une fenêtre enfant MDI agrandie, en fonction de la taille actuelle de la fenêtre du client MDI.                                                                                                                                                  |
| [**\_MENUCHAR WM**](../menurc/wm-menuchar.md)        | Transmet le message à la fenêtre frame MDI.                                                                                                                                                                                                               |
| [**déplacement de WM \_**](wm-move.md)                   | Recalcule les barres de défilement du client MDI, si elles sont présentes.                                                                                                                                                                                                 |
| [**WM \_ SetFocus**](../inputdev/wm-setfocus.md)      | Active la fenêtre enfant, s’il ne s’agit pas de la fenêtre enfant MDI active.                                                                                                                                                                                     |
| [**taille du WM \_**](wm-size.md)                   | Effectue les opérations nécessaires pour modifier la taille d’une fenêtre, en particulier pour l’optimisation ou la restauration d’une fenêtre enfant MDI. L’échec de la transmission de ce message à la fonction [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) produit des résultats très indésirables. |
| [**\_SYSCOMMAND WM**](../menurc/wm-syscommand.md)    | Commandes de menu de la fenêtre Handles (anciennement « système ») : **SC \_ NEXTWINDOW**, **SC \_ PREVWINDOW**, **SC \_ Move**, **SC \_ Size** et **SC \_ Maximize**.                                                                                                        |



 

## <a name="creating-a-child-window"></a>Création d’une fenêtre enfant

Pour créer une fenêtre enfant MDI, une application peut appeler la fonction [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou envoyer un message [**WM \_ MDICREATE**](wm-mdicreate.md) à la fenêtre cliente MDI. (L’application peut utiliser la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) avec le style **WS \_ ex \_ MDICHILD** pour créer des fenêtres enfants MDI.) Une application MDI à thread unique peut utiliser l’une ou l’autre méthode pour créer une fenêtre enfant. Un thread dans une application MDI multithread doit utiliser la fonction **CreateMDIWindow** ou **CreateWindowEx** pour créer une fenêtre enfant dans un thread différent.

Le paramètre *lParam* d’un message [**WM \_ MDICREATE**](wm-mdicreate.md) est un pointeur lointain vers une structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . La structure comprend quatre membres de dimension : **x** et **y**, qui indiquent les positions horizontale et verticale de la fenêtre, et **CX** et **CY**, qui indiquent les étendues horizontale et verticale de la fenêtre. Ces membres peuvent être attribués explicitement par l’application, ou ils peuvent être définis sur **CW \_ usedefault**, auquel cas le système sélectionne une position, une taille ou les deux, en fonction d’un algorithme en cascade. Dans tous les cas, les quatre membres doivent être initialisés. MULTIPAD utilise **des \_ usedefault en PV** pour toutes les dimensions.

Le dernier membre de la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) est le membre de **style** , qui peut contenir des bits de style pour la fenêtre. Pour créer une fenêtre enfant MDI qui peut avoir n’importe quelle combinaison de styles de fenêtre, spécifiez le style de fenêtre **MDIs \_ ALLCHILDSTYLES** . Quand ce style n’est pas spécifié, une fenêtre enfant MDI a les paramètres **WS \_ Minimize**, **WS \_ Maximize**, **WS \_ HSCROLL** et **WS \_ VSCROLL** comme paramètres par défaut.

MULTIPAD crée ses fenêtres enfants MDI en utilisant sa fonction AddFile définie localement (située dans le fichier source MPFILE. C). La fonction AddFile définit le titre de la fenêtre enfant en assignant le membre **szTitle** de la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) de la fenêtre au nom du fichier en cours de modification ou à « sans titre ». Le membre **szClass** est défini sur le nom de la classe de fenêtre enfant MDI inscrite dans la fonction InitializeApplication de MULTIPAD. Le membre **hOwner** est défini sur le handle d’instance de l’application.

L’exemple suivant illustre la fonction AddFile dans MULTIPAD.


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



Le pointeur passé dans le paramètre *lParam* du message [**WM \_ MDICREATE**](wm-mdicreate.md) est passé à la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) et apparaît en tant que premier membre de la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , passé dans le message [**WM \_ Create**](wm-create.md) . Dans MULTIPAD, la fenêtre enfant s’initialise elle-même lors de la **\_ création** du traitement des messages par l’initialisation des variables de document dans ses données supplémentaires et en créant la fenêtre enfant du contrôle d’édition.

 

 
