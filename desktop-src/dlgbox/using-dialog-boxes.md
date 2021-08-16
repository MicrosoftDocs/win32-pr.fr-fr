---
title: Utilisation des boîtes de dialogue
description: Vous utilisez les boîtes de dialogue pour afficher des informations et inviter l’utilisateur à entrer des informations.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows Interface utilisateur, fenêtrage
- Windows Interface utilisateur, boîtes de dialogue
- fenêtrage, boîtes de dialogue
- boîtes de dialogue, à propos de
- boîtes de dialogue, affichage
- boîtes de dialogue modales
- boîtes de dialogue non modales
- boîtes de dialogue, modales
- boîtes de dialogue, non modales
- boîtes de dialogue, initialiser
- modèles de boîte de dialogue
- boîtes de dialogue, modèles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ec5e97060697388224ac92f60b6043a188d4259520aaf151fb188c43f6bb64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720791"
---
# <a name="using-dialog-boxes"></a>Utilisation des boîtes de dialogue

Vous utilisez les boîtes de dialogue pour afficher des informations et inviter l’utilisateur à entrer des informations. Votre application charge et initialise la boîte de dialogue, traite l’entrée d’utilisateur et détruit la boîte de dialogue lorsque l’utilisateur termine la tâche. Le processus de gestion des boîtes de dialogue varie selon que la boîte de dialogue est modale ou non modale. Une boîte de dialogue modale oblige l’utilisateur à fermer la boîte de dialogue avant d’activer une autre fenêtre de l’application. Toutefois, l’utilisateur peut activer Windows dans différentes applications. Une boîte de dialogue non modale ne nécessite pas de réponse immédiate de l’utilisateur. Elle est similaire à une fenêtre principale contenant des contrôles.

Les sections suivantes expliquent comment utiliser les deux types de boîtes de dialogue.

-   [Affichage d’une boîte de message](#displaying-a-message-box)
-   [Création d’une boîte de dialogue modale](#creating-a-modal-dialog-box)
-   [Création d’une boîte de dialogue non modale](#creating-a-modeless-dialog-box)
-   [Initialisation d’une boîte de dialogue](#initializing-a-dialog-box)
-   [Création d’un modèle en mémoire](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Affichage d’une boîte de message

La forme la plus simple de la boîte de dialogue modale est la boîte de message. La plupart des applications utilisent des boîtes de message pour avertir l’utilisateur des erreurs et pour demander des instructions sur la procédure à suivre après qu’une erreur s’est produite. Vous créez une boîte de message à l’aide de la fonction [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , en spécifiant le message et le nombre et le type de boutons à afficher. Le système crée une boîte de dialogue modale, en fournissant son propre modèle et procédure de boîte de dialogue. Une fois que l’utilisateur a fermé la boîte de message, **MessageBox** ou **MessageBoxEx** retourne une valeur identifiant le bouton choisi par l’utilisateur pour fermer la boîte de message.

Dans l’exemple suivant, l’application affiche une boîte de message qui invite l’utilisateur à entrer une action après qu’une condition d’erreur s’est produite. La boîte de message affiche le message qui décrit la condition d’erreur et comment la résoudre. Le style **MB \_ YesNo** dirige [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) pour fournir deux boutons avec lesquels l’utilisateur peut choisir comment procéder :


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



L’illustration suivante montre la sortie de l’exemple de code précédent :

![boîte de message](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Création d’une boîte de dialogue modale

Vous créez une boîte de dialogue modale à l’aide de la fonction [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Vous devez spécifier l’identificateur ou le nom d’une ressource de modèle de boîte de dialogue et un pointeur vers la procédure de boîte de dialogue. La fonction **DialogBox** charge le modèle, affiche la boîte de dialogue et traite toutes les entrées d’utilisateur jusqu’à ce que l’utilisateur ferme la boîte de dialogue.

Dans l’exemple suivant, l’application affiche une boîte de dialogue modale quand l’utilisateur clique sur **supprimer un élément** dans un menu d’application. La boîte de dialogue contient un contrôle d’édition (dans lequel l’utilisateur entre le nom d’un élément) et des boutons **OK** et **Annuler** . Les identificateurs de contrôle pour ces contrôles sont ID \_ ITEMNAME, IDOK et IDCANCEL, respectivement.

La première partie de l’exemple se compose des instructions qui créent la boîte de dialogue modale. Ces instructions, dans la procédure de fenêtre pour la fenêtre principale de l’application, créent la boîte de dialogue lorsque le système reçoit un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l' \_ identificateur de menu IDM DELETEITEM. La deuxième partie de l’exemple est la procédure de boîte de dialogue, qui récupère le contenu du contrôle d’édition et ferme la boîte de dialogue lors de la réception d’un message de **\_ commande WM** .

Les instructions suivantes créent la boîte de dialogue modale. Le modèle de boîte de dialogue est une ressource dans le fichier exécutable de l’application et possède l’identificateur de ressource DLG \_ DELETEITEM.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



Dans cet exemple, l’application spécifie sa fenêtre principale comme fenêtre propriétaire de la boîte de dialogue. Quand le système affiche initialement la boîte de dialogue, sa position est relative au coin supérieur gauche de la zone cliente de la fenêtre propriétaire. L’application utilise la valeur de retour de [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) pour déterminer s’il faut poursuivre l’opération ou l’annuler. Les instructions suivantes définissent la procédure de la boîte de dialogue.


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



Dans cet exemple, la procédure utilise [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) pour récupérer le texte actuel à partir du contrôle d’édition identifié par l’ID \_ ITEMNAME. La procédure appelle ensuite la fonction [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) pour définir la valeur de retour de la boîte de dialogue sur IDOK ou IDCANCEL, selon le message reçu, et pour commencer le processus de fermeture de la boîte de dialogue. Les identificateurs IDOK et IDCANCEL correspondent aux boutons **OK** et **Annuler** . Une fois que la procédure a appelé **EndDialog**, le système envoie des messages supplémentaires à la procédure pour détruire la boîte de dialogue et retourner la valeur de retour de la boîte de dialogue à la fonction qui a créé la boîte de dialogue.

## <a name="creating-a-modeless-dialog-box"></a>Création d’une boîte de dialogue non modale

Vous créez une boîte de dialogue non modale à l’aide de la fonction [**createDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , en spécifiant l’identificateur ou le nom d’une ressource de modèle de boîte de dialogue et un pointeur vers la procédure de la boîte de dialogue. **CreateDialog** charge le modèle, crée la boîte de dialogue et l’affiche éventuellement. Votre application est chargée de récupérer et de distribuer les messages d’entrée utilisateur à la procédure de la boîte de dialogue.

Dans l’exemple suivant, l’application affiche une boîte de dialogue non modale (si elle n’est pas déjà affichée) quand l’utilisateur clique sur **accéder au** à partir d’un menu d’application. La boîte de dialogue contient un contrôle d’édition, une case à cocher et des boutons **OK** et **Annuler** . Le modèle de boîte de dialogue est une ressource dans le fichier exécutable de l’application et a l’identificateur de ressource DLG \_ goto. L’utilisateur entre un numéro de ligne dans le contrôle d’édition et active la case à cocher pour spécifier que le numéro de ligne est relatif à la ligne active. Les identificateurs de contrôle sont \_ ligne ID, ID \_ ABSREL, IDOK et IDCANCEL.

Les instructions de la première partie de l’exemple créent la boîte de dialogue non modale. Ces instructions, dans la procédure de fenêtre pour la fenêtre principale de l’application, créent la boîte de dialogue lorsque la procédure de fenêtre reçoit un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l' \_ identificateur de menu IDM Goto, mais uniquement si la variable globale ne contient pas déjà un handle valide. La deuxième partie de l’exemple correspond à la boucle de message principale de l’application. La boucle comprend la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) pour garantir que l’utilisateur peut utiliser l’interface de clavier de la boîte de dialogue dans cette boîte de dialogue non modale. La troisième partie de l’exemple est la procédure de la boîte de dialogue. La procédure récupère le contenu du contrôle d’édition et la case à cocher lorsque l’utilisateur clique sur le bouton **OK** . La procédure détruit la boîte de dialogue lorsque l’utilisateur clique sur le bouton **Annuler** .


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



Dans les instructions précédentes, [**createDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) est appelé uniquement si `hwndGoto` ne contient pas de handle de fenêtre valide. Cela permet de s’assurer que l’application n’affiche pas deux boîtes de dialogue en même temps. Pour prendre en charge cette méthode de vérification, la procédure de dialogue doit avoir la valeur **null** lorsqu’elle détruit la boîte de dialogue.

La boucle de message pour une application se compose des instructions suivantes.


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



La boucle vérifie la validité du handle de fenêtre dans la boîte de dialogue et appelle la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) uniquement si le handle est valide. **IsDialogMessage** traite uniquement le message s’il appartient à la boîte de dialogue. Dans le cas contraire, elle retourne **false** et la boucle distribue le message à la fenêtre appropriée.

Les instructions suivantes définissent la procédure de la boîte de dialogue.


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



Dans les instructions précédentes, la procédure traite les messages de [**\_ commande**](/windows/desktop/menurc/wm-command) [**WM \_ INITDIALOG**](wm-initdialog.md) et WM. Lors du traitement du **\_ INITDIALOG WM** , la procédure initialise la case à cocher en passant la valeur actuelle de la variable globale à [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). La procédure renvoie ensuite la **valeur true** pour indiquer au système de définir le focus d’entrée par défaut.

Lors du traitement de la [**\_ commande WM**](/windows/desktop/menurc/wm-command) , la procédure ferme la boîte de dialogue uniquement si l’utilisateur clique sur le bouton **Annuler** (c’est-à-dire, sur le bouton ayant l’identificateur IDCANCEL). La procédure doit appeler [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour fermer une boîte de dialogue non modale. Notez que la procédure définit également la variable sur la **valeur null** pour s’assurer que les autres instructions qui dépendent de cette variable fonctionnent correctement.

Si l’utilisateur clique sur le bouton **OK** , la procédure récupère l’état actuel de la case à cocher et l’assigne à la variable **fRelative** . Il utilise ensuite la variable pour récupérer le numéro de ligne à partir du contrôle d’édition. [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) convertit le texte du contrôle d’édition en entier. La valeur de **fRelative** détermine si la fonction interprète le nombre comme une valeur signée ou non signée. Si le texte du contrôle d’édition n’est pas un nombre valide, **GetDlgItemInt** définit la valeur de la variable de l' **ferror** sur une valeur différente de zéro. La procédure vérifie cette valeur pour déterminer s’il faut afficher un message d’erreur ou exécuter la tâche. En cas d’erreur, la procédure de boîte de dialogue envoie un message au contrôle d’édition, en le dirigeant pour sélectionner le texte dans le contrôle afin que l’utilisateur puisse le remplacer facilement. Si **GetDlgItemInt** ne retourne pas d’erreur, la procédure peut exécuter la tâche demandée elle-même ou envoyer un message à la fenêtre propriétaire, en la dirigeant pour effectuer l’opération.

## <a name="initializing-a-dialog-box"></a>Initialisation d’une boîte de dialogue

Vous initialisez la boîte de dialogue et son contenu lors du traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) . La tâche la plus courante consiste à initialiser les contrôles pour refléter les paramètres de la boîte de dialogue active. Une autre tâche courante consiste à centrer une boîte de dialogue à l’écran ou dans sa fenêtre propriétaire. Une tâche utile pour certaines boîtes de dialogue consiste à définir le focus d’entrée sur un contrôle spécifié plutôt que d’accepter le focus d’entrée par défaut.

Dans l’exemple suivant, la procédure de boîte de dialogue Centre la boîte de dialogue et définit le focus d’entrée lors du traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) . Pour centrer la boîte de dialogue, la procédure récupère les rectangles de la fenêtre de la boîte de dialogue et de la fenêtre propriétaire et calcule une nouvelle position pour la boîte de dialogue. Pour définir le focus d’entrée, la procédure vérifie le paramètre *wParam* afin de déterminer l’identificateur du focus d’entrée par défaut.


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



Dans les instructions précédentes, la procédure utilise la fonction [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) pour récupérer le descripteur de fenêtre propriétaire d’une boîte de dialogue. La fonction retourne le handle de la fenêtre propriétaire aux boîtes de dialogue et le handle de la fenêtre parente aux fenêtres enfants. Étant donné qu’une application peut créer une boîte de dialogue qui n’a pas de propriétaire, la procédure vérifie le handle retourné et utilise la fonction [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) pour récupérer le handle de la fenêtre du bureau, si nécessaire. Après avoir calculé la nouvelle position, la procédure utilise la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour déplacer la boîte de dialogue, en spécifiant la \_ valeur supérieure HWND pour garantir que la boîte de dialogue reste au-dessus de la fenêtre propriétaire.

Avant de définir le focus d’entrée, la procédure vérifie l’identificateur de contrôle du focus d’entrée par défaut. Le système passe le handle de fenêtre du focus d’entrée par défaut dans le paramètre *wParam* . La fonction [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) retourne l’identificateur pour le contrôle identifié par le handle de fenêtre. Si l’identificateur ne correspond pas à l’identificateur correct, la procédure utilise la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) pour définir le focus d’entrée. La fonction [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) est requise pour récupérer le handle de fenêtre du contrôle souhaité.

## <a name="creating-a-template-in-memory"></a>Création d’un modèle en mémoire

Les applications adaptent ou modifient parfois le contenu des boîtes de dialogue en fonction de l’état actuel des données en cours de traitement. Dans ce cas, il n’est pas pratique de fournir tous les modèles de boîte de dialogue possibles en tant que ressources dans le fichier exécutable de l’application. Toutefois, la création de modèles en mémoire offre à l’application une plus grande flexibilité pour s’adapter à toutes les circonstances.

Dans l’exemple suivant, l’application crée un modèle en mémoire pour une boîte de dialogue modale qui contient un message et des boutons **OK** et **aide** .

Dans un modèle de boîte de dialogue, toutes les chaînes de caractères, telles que la boîte de dialogue et les titres de bouton, doivent être des chaînes Unicode. Cet exemple utilise la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) pour générer ces chaînes Unicode.

Les structures [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) dans un modèle de boîte de dialogue doivent être alignées sur les limites **DWORD** . Pour aligner ces structures, cet exemple utilise une routine d’assistance qui prend un pointeur d’entrée et retourne le pointeur le plus proche aligné sur une limite **DWORD** .


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 