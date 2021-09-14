---
title: Procédure de création d’un contrôle d’édition de ligne unique
description: Cette rubrique montre comment créer une boîte de dialogue qui contient un contrôle d’édition sur une seule ligne.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115385"
---
# <a name="how-to-create-a-single-line-edit-control"></a>Procédure de création d’un contrôle d’édition de ligne unique

Cette rubrique montre comment créer une boîte de dialogue qui contient un contrôle d’édition sur une seule ligne.

Le contrôle d’édition sur une seule ligne a le style [**\_ de mot de passe es**](edit-control-styles.md) . Par défaut, les contrôles d’édition avec ce style affichent un astérisque pour chaque caractère tapé par l’utilisateur. Toutefois, cet exemple utilise le message [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) pour remplacer le caractère par défaut par un astérisque par un signe plus (+). La capture d’écran suivante montre la boîte de dialogue une fois que l’utilisateur a entré un mot de passe.

![capture d’écran d’une boîte de dialogue contenant un contrôle d’édition pour la saisie d’un mot de passe](images/passworddlg.png)

> [!Note]  
> Comctl32.dll version 6 n’est pas redistribuable. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Étape 1 : créer une instance de la boîte de dialogue mot de passe.

L’exemple de code C++ suivant utilise la fonction DialogBox pour créer une boîte de dialogue modale. Le modèle de boîte **de dialogue IDD \_ mot_de_passe** est passé en tant que paramètre. Il définit, entre autres choses, les styles de fenêtre, les boutons et les dimensions de la boîte de dialogue de mot de passe.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Étape 2 : initialiser la boîte de dialogue et traiter l’entrée d’utilisateur.

La procédure de fenêtre de l’exemple suivant initialise la boîte de dialogue de mot de passe et traite les messages de notification et les entrées utilisateur.

Pendant l’initialisation, la procédure de fenêtre remplace le caractère de mot de passe par défaut par un **+** signe et définit le bouton de sélection par défaut sur **Annuler**.

Pendant le traitement des entrées utilisateur, la procédure de fenêtre remplace le bouton de commande par défaut **Annuler** par **OK** dès que l’utilisateur entre du texte dans le contrôle d’édition. Si l’utilisateur appuie sur le bouton **OK** , la procédure de fenêtre utilise les messages [**em \_ LINELENGTH**](em-linelength.md) et [**em \_ GETLINE**](em-getline.md) pour récupérer le texte.



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles d’édition](about-edit-controls.md)
</dt> <dt>

[Modifier la référence de contrôle](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Utilisation des contrôles d’édition](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Modifier le contrôle](edit-controls.md)
</dt> </dl>

 

 