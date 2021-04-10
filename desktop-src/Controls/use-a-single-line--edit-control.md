---
title: Procédure de création d’un contrôle d’édition de ligne unique
description: Cette rubrique montre comment créer une boîte de dialogue qui contient un contrôle d’édition sur une seule ligne.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032103"
---
# <a name="how-to-create-a-single-line-edit-control"></a><span data-ttu-id="7e4ea-103">Procédure de création d’un contrôle d’édition de ligne unique</span><span class="sxs-lookup"><span data-stu-id="7e4ea-103">How to Create a Single Line Edit Control</span></span>

<span data-ttu-id="7e4ea-104">Cette rubrique montre comment créer une boîte de dialogue qui contient un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-104">This topic demonstrates how to create a dialog box that contains a single-line edit control.</span></span>

<span data-ttu-id="7e4ea-105">Le contrôle d’édition sur une seule ligne a le style [**\_ de mot de passe es**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7e4ea-105">The single-line edit control has the [**ES\_PASSWORD**](edit-control-styles.md) style.</span></span> <span data-ttu-id="7e4ea-106">Par défaut, les contrôles d’édition avec ce style affichent un astérisque pour chaque caractère tapé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-106">By default, edit controls with this style display an asterisk for each character that is typed by the user.</span></span> <span data-ttu-id="7e4ea-107">Toutefois, cet exemple utilise le message [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) pour remplacer le caractère par défaut par un astérisque par un signe plus (+).</span><span class="sxs-lookup"><span data-stu-id="7e4ea-107">This example, however, uses the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message to change the default character from an asterisk to a plus sign (+).</span></span> <span data-ttu-id="7e4ea-108">La capture d’écran suivante montre la boîte de dialogue une fois que l’utilisateur a entré un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-108">The following screen shot shows the dialog box after the user has entered a password.</span></span>

![capture d’écran d’une boîte de dialogue contenant un contrôle d’édition pour la saisie d’un mot de passe](images/passworddlg.png)

> [!Note]  
> <span data-ttu-id="7e4ea-110">Comctl32.dll version 6 n’est pas redistribuable.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-110">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="7e4ea-111">Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="7e4ea-112">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7e4ea-112">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="7e4ea-113">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="7e4ea-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7e4ea-114">Technologies</span><span class="sxs-lookup"><span data-stu-id="7e4ea-114">Technologies</span></span>

-   [<span data-ttu-id="7e4ea-115">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="7e4ea-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7e4ea-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="7e4ea-116">Prerequisites</span></span>

-   <span data-ttu-id="7e4ea-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="7e4ea-117">C/C++</span></span>
-   <span data-ttu-id="7e4ea-118">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="7e4ea-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7e4ea-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="7e4ea-119">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a><span data-ttu-id="7e4ea-120">Étape 1 : créer une instance de la boîte de dialogue mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-120">Step 1: Create an instance of the password dialog box.</span></span>

<span data-ttu-id="7e4ea-121">L’exemple de code C++ suivant utilise la fonction DialogBox pour créer une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-121">The following C++ code example uses the DialogBox function to create a modal dialog box.</span></span> <span data-ttu-id="7e4ea-122">Le modèle de boîte **de dialogue IDD \_ mot_de_passe** est passé en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-122">The dialog box template **IDD\_PASSWORD** is passed as a parameter.</span></span> <span data-ttu-id="7e4ea-123">Il définit, entre autres choses, les styles de fenêtre, les boutons et les dimensions de la boîte de dialogue de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-123">It defines, among other things, the window styles, buttons, and dimensions of the password dialog box.</span></span>


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a><span data-ttu-id="7e4ea-124">Étape 2 : initialiser la boîte de dialogue et traiter l’entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-124">Step 2: Initialize the dialog box and process user input.</span></span>

<span data-ttu-id="7e4ea-125">La procédure de fenêtre de l’exemple suivant initialise la boîte de dialogue de mot de passe et traite les messages de notification et les entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-125">The window procedure in the following example initializes the password dialog box and processes notification messages and user input.</span></span>

<span data-ttu-id="7e4ea-126">Pendant l’initialisation, la procédure de fenêtre remplace le caractère de mot de passe par défaut par un **+** signe et définit le bouton de sélection par défaut sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-126">During initialization, the window procedure changes the default password character to a **+** sign and sets the default pushbutton to **Cancel**.</span></span>

<span data-ttu-id="7e4ea-127">Pendant le traitement des entrées utilisateur, la procédure de fenêtre remplace le bouton de commande par défaut **Annuler** par **OK** dès que l’utilisateur entre du texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-127">During user input processing, the window procedure changes the default push button from **CANCEL** to **OK** as soon as the user enters text in the edit control.</span></span> <span data-ttu-id="7e4ea-128">Si l’utilisateur appuie sur le bouton **OK** , la procédure de fenêtre utilise les messages [**em \_ LINELENGTH**](em-linelength.md) et [**em \_ GETLINE**](em-getline.md) pour récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="7e4ea-128">If the user presses the **OK** button, the window procedure uses the [**EM\_LINELENGTH**](em-linelength.md) and [**EM\_GETLINE**](em-getline.md) messages to retrieve the text.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="7e4ea-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e4ea-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e4ea-130">À propos des contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="7e4ea-130">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="7e4ea-131">Modifier la référence de contrôle</span><span class="sxs-lookup"><span data-stu-id="7e4ea-131">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7e4ea-132">Utilisation des contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="7e4ea-132">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="7e4ea-133">Modifier le contrôle</span><span class="sxs-lookup"><span data-stu-id="7e4ea-133">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 