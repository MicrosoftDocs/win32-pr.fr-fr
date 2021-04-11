---
title: Utilisation des boîtes de dialogue
description: Vous utilisez les boîtes de dialogue pour afficher des informations et inviter l’utilisateur à entrer des informations.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Interface utilisateur Windows, fenêtrage
- Interface utilisateur Windows, boîtes de dialogue
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
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031669"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="e82c7-115">Utilisation des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="e82c7-115">Using Dialog Boxes</span></span>

<span data-ttu-id="e82c7-116">Vous utilisez les boîtes de dialogue pour afficher des informations et inviter l’utilisateur à entrer des informations.</span><span class="sxs-lookup"><span data-stu-id="e82c7-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="e82c7-117">Votre application charge et initialise la boîte de dialogue, traite l’entrée d’utilisateur et détruit la boîte de dialogue lorsque l’utilisateur termine la tâche.</span><span class="sxs-lookup"><span data-stu-id="e82c7-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="e82c7-118">Le processus de gestion des boîtes de dialogue varie selon que la boîte de dialogue est modale ou non modale.</span><span class="sxs-lookup"><span data-stu-id="e82c7-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="e82c7-119">Une boîte de dialogue modale oblige l’utilisateur à fermer la boîte de dialogue avant d’activer une autre fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="e82c7-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="e82c7-120">Toutefois, l’utilisateur peut activer Windows dans différentes applications.</span><span class="sxs-lookup"><span data-stu-id="e82c7-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="e82c7-121">Une boîte de dialogue non modale ne nécessite pas de réponse immédiate de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e82c7-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="e82c7-122">Elle est similaire à une fenêtre principale contenant des contrôles.</span><span class="sxs-lookup"><span data-stu-id="e82c7-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="e82c7-123">Les sections suivantes expliquent comment utiliser les deux types de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="e82c7-124">Affichage d’une boîte de message</span><span class="sxs-lookup"><span data-stu-id="e82c7-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="e82c7-125">Création d’une boîte de dialogue modale</span><span class="sxs-lookup"><span data-stu-id="e82c7-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="e82c7-126">Création d’une boîte de dialogue non modale</span><span class="sxs-lookup"><span data-stu-id="e82c7-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="e82c7-127">Initialisation d’une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="e82c7-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="e82c7-128">Création d’un modèle en mémoire</span><span class="sxs-lookup"><span data-stu-id="e82c7-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="e82c7-129">Affichage d’une boîte de message</span><span class="sxs-lookup"><span data-stu-id="e82c7-129">Displaying a Message Box</span></span>

<span data-ttu-id="e82c7-130">La forme la plus simple de la boîte de dialogue modale est la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="e82c7-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="e82c7-131">La plupart des applications utilisent des boîtes de message pour avertir l’utilisateur des erreurs et pour demander des instructions sur la procédure à suivre après qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e82c7-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="e82c7-132">Vous créez une boîte de message à l’aide de la fonction [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , en spécifiant le message et le nombre et le type de boutons à afficher.</span><span class="sxs-lookup"><span data-stu-id="e82c7-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="e82c7-133">Le système crée une boîte de dialogue modale, en fournissant son propre modèle et procédure de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="e82c7-134">Une fois que l’utilisateur a fermé la boîte de message, **MessageBox** ou **MessageBoxEx** retourne une valeur identifiant le bouton choisi par l’utilisateur pour fermer la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="e82c7-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="e82c7-135">Dans l’exemple suivant, l’application affiche une boîte de message qui invite l’utilisateur à entrer une action après qu’une condition d’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e82c7-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="e82c7-136">La boîte de message affiche le message qui décrit la condition d’erreur et comment la résoudre.</span><span class="sxs-lookup"><span data-stu-id="e82c7-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="e82c7-137">Le style **MB \_ YesNo** dirige [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) pour fournir deux boutons avec lesquels l’utilisateur peut choisir comment procéder :</span><span class="sxs-lookup"><span data-stu-id="e82c7-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


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



<span data-ttu-id="e82c7-138">L’illustration suivante montre la sortie de l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="e82c7-138">The following image shows the output from the preceding code example:</span></span>

![boîte de message](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="e82c7-140">Création d’une boîte de dialogue modale</span><span class="sxs-lookup"><span data-stu-id="e82c7-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="e82c7-141">Vous créez une boîte de dialogue modale à l’aide de la fonction [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="e82c7-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="e82c7-142">Vous devez spécifier l’identificateur ou le nom d’une ressource de modèle de boîte de dialogue et un pointeur vers la procédure de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="e82c7-143">La fonction **DialogBox** charge le modèle, affiche la boîte de dialogue et traite toutes les entrées d’utilisateur jusqu’à ce que l’utilisateur ferme la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="e82c7-144">Dans l’exemple suivant, l’application affiche une boîte de dialogue modale quand l’utilisateur clique sur **supprimer un élément** dans un menu d’application.</span><span class="sxs-lookup"><span data-stu-id="e82c7-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="e82c7-145">La boîte de dialogue contient un contrôle d’édition (dans lequel l’utilisateur entre le nom d’un élément) et des boutons **OK** et **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="e82c7-146">Les identificateurs de contrôle pour ces contrôles sont ID \_ ITEMNAME, IDOK et IDCANCEL, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e82c7-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="e82c7-147">La première partie de l’exemple se compose des instructions qui créent la boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="e82c7-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="e82c7-148">Ces instructions, dans la procédure de fenêtre pour la fenêtre principale de l’application, créent la boîte de dialogue lorsque le système reçoit un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l' \_ identificateur de menu IDM DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="e82c7-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="e82c7-149">La deuxième partie de l’exemple est la procédure de boîte de dialogue, qui récupère le contenu du contrôle d’édition et ferme la boîte de dialogue lors de la réception d’un message de **\_ commande WM** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="e82c7-150">Les instructions suivantes créent la boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="e82c7-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="e82c7-151">Le modèle de boîte de dialogue est une ressource dans le fichier exécutable de l’application et possède l’identificateur de ressource DLG \_ DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="e82c7-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


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



<span data-ttu-id="e82c7-152">Dans cet exemple, l’application spécifie sa fenêtre principale comme fenêtre propriétaire de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="e82c7-153">Quand le système affiche initialement la boîte de dialogue, sa position est relative au coin supérieur gauche de la zone cliente de la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e82c7-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="e82c7-154">L’application utilise la valeur de retour de [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) pour déterminer s’il faut poursuivre l’opération ou l’annuler.</span><span class="sxs-lookup"><span data-stu-id="e82c7-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="e82c7-155">Les instructions suivantes définissent la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-155">The following statements define the dialog box procedure.</span></span>


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



<span data-ttu-id="e82c7-156">Dans cet exemple, la procédure utilise [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) pour récupérer le texte actuel à partir du contrôle d’édition identifié par l’ID \_ ITEMNAME.</span><span class="sxs-lookup"><span data-stu-id="e82c7-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="e82c7-157">La procédure appelle ensuite la fonction [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) pour définir la valeur de retour de la boîte de dialogue sur IDOK ou IDCANCEL, selon le message reçu, et pour commencer le processus de fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="e82c7-158">Les identificateurs IDOK et IDCANCEL correspondent aux boutons **OK** et **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="e82c7-159">Une fois que la procédure a appelé **EndDialog**, le système envoie des messages supplémentaires à la procédure pour détruire la boîte de dialogue et retourner la valeur de retour de la boîte de dialogue à la fonction qui a créé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="e82c7-160">Création d’une boîte de dialogue non modale</span><span class="sxs-lookup"><span data-stu-id="e82c7-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="e82c7-161">Vous créez une boîte de dialogue non modale à l’aide de la fonction [**createDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , en spécifiant l’identificateur ou le nom d’une ressource de modèle de boîte de dialogue et un pointeur vers la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="e82c7-162">**CreateDialog** charge le modèle, crée la boîte de dialogue et l’affiche éventuellement.</span><span class="sxs-lookup"><span data-stu-id="e82c7-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="e82c7-163">Votre application est chargée de récupérer et de distribuer les messages d’entrée utilisateur à la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="e82c7-164">Dans l’exemple suivant, l’application affiche une boîte de dialogue non modale (si elle n’est pas déjà affichée) quand l’utilisateur clique sur **accéder au** à partir d’un menu d’application.</span><span class="sxs-lookup"><span data-stu-id="e82c7-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="e82c7-165">La boîte de dialogue contient un contrôle d’édition, une case à cocher et des boutons **OK** et **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="e82c7-166">Le modèle de boîte de dialogue est une ressource dans le fichier exécutable de l’application et a l’identificateur de ressource DLG \_ goto.</span><span class="sxs-lookup"><span data-stu-id="e82c7-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="e82c7-167">L’utilisateur entre un numéro de ligne dans le contrôle d’édition et active la case à cocher pour spécifier que le numéro de ligne est relatif à la ligne active.</span><span class="sxs-lookup"><span data-stu-id="e82c7-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="e82c7-168">Les identificateurs de contrôle sont \_ ligne ID, ID \_ ABSREL, IDOK et IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="e82c7-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="e82c7-169">Les instructions de la première partie de l’exemple créent la boîte de dialogue non modale.</span><span class="sxs-lookup"><span data-stu-id="e82c7-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="e82c7-170">Ces instructions, dans la procédure de fenêtre pour la fenêtre principale de l’application, créent la boîte de dialogue lorsque la procédure de fenêtre reçoit un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l' \_ identificateur de menu IDM Goto, mais uniquement si la variable globale ne contient pas déjà un handle valide.</span><span class="sxs-lookup"><span data-stu-id="e82c7-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="e82c7-171">La deuxième partie de l’exemple correspond à la boucle de message principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="e82c7-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="e82c7-172">La boucle comprend la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) pour garantir que l’utilisateur peut utiliser l’interface de clavier de la boîte de dialogue dans cette boîte de dialogue non modale.</span><span class="sxs-lookup"><span data-stu-id="e82c7-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="e82c7-173">La troisième partie de l’exemple est la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="e82c7-174">La procédure récupère le contenu du contrôle d’édition et la case à cocher lorsque l’utilisateur clique sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="e82c7-175">La procédure détruit la boîte de dialogue lorsque l’utilisateur clique sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


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



<span data-ttu-id="e82c7-176">Dans les instructions précédentes, [**createDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) est appelé uniquement si `hwndGoto` ne contient pas de handle de fenêtre valide.</span><span class="sxs-lookup"><span data-stu-id="e82c7-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="e82c7-177">Cela permet de s’assurer que l’application n’affiche pas deux boîtes de dialogue en même temps.</span><span class="sxs-lookup"><span data-stu-id="e82c7-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="e82c7-178">Pour prendre en charge cette méthode de vérification, la procédure de dialogue doit avoir la valeur **null** lorsqu’elle détruit la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="e82c7-179">La boucle de message pour une application se compose des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e82c7-179">The message loop for an application consists of the following statements.</span></span>


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



<span data-ttu-id="e82c7-180">La boucle vérifie la validité du handle de fenêtre dans la boîte de dialogue et appelle la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) uniquement si le handle est valide.</span><span class="sxs-lookup"><span data-stu-id="e82c7-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="e82c7-181">**IsDialogMessage** traite uniquement le message s’il appartient à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="e82c7-182">Dans le cas contraire, elle retourne **false** et la boucle distribue le message à la fenêtre appropriée.</span><span class="sxs-lookup"><span data-stu-id="e82c7-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="e82c7-183">Les instructions suivantes définissent la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-183">The following statements define the dialog box procedure.</span></span>


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



<span data-ttu-id="e82c7-184">Dans les instructions précédentes, la procédure traite les messages de [**\_ commande**](/windows/desktop/menurc/wm-command) [**WM \_ INITDIALOG**](wm-initdialog.md) et WM.</span><span class="sxs-lookup"><span data-stu-id="e82c7-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="e82c7-185">Lors du traitement du **\_ INITDIALOG WM** , la procédure initialise la case à cocher en passant la valeur actuelle de la variable globale à [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span><span class="sxs-lookup"><span data-stu-id="e82c7-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="e82c7-186">La procédure renvoie ensuite la **valeur true** pour indiquer au système de définir le focus d’entrée par défaut.</span><span class="sxs-lookup"><span data-stu-id="e82c7-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="e82c7-187">Lors du traitement de la [**\_ commande WM**](/windows/desktop/menurc/wm-command) , la procédure ferme la boîte de dialogue uniquement si l’utilisateur clique sur le bouton **Annuler** (c’est-à-dire, sur le bouton ayant l’identificateur IDCANCEL).</span><span class="sxs-lookup"><span data-stu-id="e82c7-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="e82c7-188">La procédure doit appeler [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour fermer une boîte de dialogue non modale.</span><span class="sxs-lookup"><span data-stu-id="e82c7-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="e82c7-189">Notez que la procédure définit également la variable sur la **valeur null** pour s’assurer que les autres instructions qui dépendent de cette variable fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="e82c7-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="e82c7-190">Si l’utilisateur clique sur le bouton **OK** , la procédure récupère l’état actuel de la case à cocher et l’assigne à la variable **fRelative** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="e82c7-191">Il utilise ensuite la variable pour récupérer le numéro de ligne à partir du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e82c7-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="e82c7-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) convertit le texte du contrôle d’édition en entier.</span><span class="sxs-lookup"><span data-stu-id="e82c7-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="e82c7-193">La valeur de **fRelative** détermine si la fonction interprète le nombre comme une valeur signée ou non signée.</span><span class="sxs-lookup"><span data-stu-id="e82c7-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="e82c7-194">Si le texte du contrôle d’édition n’est pas un nombre valide, **GetDlgItemInt** définit la valeur de la variable de l' **ferror** sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e82c7-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="e82c7-195">La procédure vérifie cette valeur pour déterminer s’il faut afficher un message d’erreur ou exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="e82c7-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="e82c7-196">En cas d’erreur, la procédure de boîte de dialogue envoie un message au contrôle d’édition, en le dirigeant pour sélectionner le texte dans le contrôle afin que l’utilisateur puisse le remplacer facilement.</span><span class="sxs-lookup"><span data-stu-id="e82c7-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="e82c7-197">Si **GetDlgItemInt** ne retourne pas d’erreur, la procédure peut exécuter la tâche demandée elle-même ou envoyer un message à la fenêtre propriétaire, en la dirigeant pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e82c7-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="e82c7-198">Initialisation d’une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="e82c7-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="e82c7-199">Vous initialisez la boîte de dialogue et son contenu lors du traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="e82c7-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="e82c7-200">La tâche la plus courante consiste à initialiser les contrôles pour refléter les paramètres de la boîte de dialogue active.</span><span class="sxs-lookup"><span data-stu-id="e82c7-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="e82c7-201">Une autre tâche courante consiste à centrer une boîte de dialogue à l’écran ou dans sa fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e82c7-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="e82c7-202">Une tâche utile pour certaines boîtes de dialogue consiste à définir le focus d’entrée sur un contrôle spécifié plutôt que d’accepter le focus d’entrée par défaut.</span><span class="sxs-lookup"><span data-stu-id="e82c7-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="e82c7-203">Dans l’exemple suivant, la procédure de boîte de dialogue Centre la boîte de dialogue et définit le focus d’entrée lors du traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="e82c7-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="e82c7-204">Pour centrer la boîte de dialogue, la procédure récupère les rectangles de la fenêtre de la boîte de dialogue et de la fenêtre propriétaire et calcule une nouvelle position pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="e82c7-205">Pour définir le focus d’entrée, la procédure vérifie le paramètre *wParam* afin de déterminer l’identificateur du focus d’entrée par défaut.</span><span class="sxs-lookup"><span data-stu-id="e82c7-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


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



<span data-ttu-id="e82c7-206">Dans les instructions précédentes, la procédure utilise la fonction [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) pour récupérer le descripteur de fenêtre propriétaire d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e82c7-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="e82c7-207">La fonction retourne le handle de la fenêtre propriétaire aux boîtes de dialogue et le handle de la fenêtre parente aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="e82c7-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="e82c7-208">Étant donné qu’une application peut créer une boîte de dialogue qui n’a pas de propriétaire, la procédure vérifie le handle retourné et utilise la fonction [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) pour récupérer le handle de la fenêtre du bureau, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e82c7-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="e82c7-209">Après avoir calculé la nouvelle position, la procédure utilise la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour déplacer la boîte de dialogue, en spécifiant la \_ valeur supérieure HWND pour garantir que la boîte de dialogue reste au-dessus de la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e82c7-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="e82c7-210">Avant de définir le focus d’entrée, la procédure vérifie l’identificateur de contrôle du focus d’entrée par défaut.</span><span class="sxs-lookup"><span data-stu-id="e82c7-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="e82c7-211">Le système passe le handle de fenêtre du focus d’entrée par défaut dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e82c7-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="e82c7-212">La fonction [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) retourne l’identificateur pour le contrôle identifié par le handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e82c7-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="e82c7-213">Si l’identificateur ne correspond pas à l’identificateur correct, la procédure utilise la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) pour définir le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e82c7-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="e82c7-214">La fonction [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) est requise pour récupérer le handle de fenêtre du contrôle souhaité.</span><span class="sxs-lookup"><span data-stu-id="e82c7-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="e82c7-215">Création d’un modèle en mémoire</span><span class="sxs-lookup"><span data-stu-id="e82c7-215">Creating a Template in Memory</span></span>

<span data-ttu-id="e82c7-216">Les applications adaptent ou modifient parfois le contenu des boîtes de dialogue en fonction de l’état actuel des données en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="e82c7-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="e82c7-217">Dans ce cas, il n’est pas pratique de fournir tous les modèles de boîte de dialogue possibles en tant que ressources dans le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="e82c7-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="e82c7-218">Toutefois, la création de modèles en mémoire offre à l’application une plus grande flexibilité pour s’adapter à toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="e82c7-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="e82c7-219">Dans l’exemple suivant, l’application crée un modèle en mémoire pour une boîte de dialogue modale qui contient un message et des boutons **OK** et **aide** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="e82c7-220">Dans un modèle de boîte de dialogue, toutes les chaînes de caractères, telles que la boîte de dialogue et les titres de bouton, doivent être des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="e82c7-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="e82c7-221">Cet exemple utilise la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) pour générer ces chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="e82c7-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="e82c7-222">Les structures [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) dans un modèle de boîte de dialogue doivent être alignées sur les limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="e82c7-223">Pour aligner ces structures, cet exemple utilise une routine d’assistance qui prend un pointeur d’entrée et retourne le pointeur le plus proche aligné sur une limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e82c7-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


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



 

 