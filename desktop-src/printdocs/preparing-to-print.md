---
description: Cette rubrique explique comment collecter des informations sur les travaux d’impression auprès de l’utilisateur.
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: 'Procédure : collecter des informations de travail d’impression à partir de l’utilisateur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034498"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a>Procédure : collecter des informations de travail d’impression à partir de l’utilisateur

Cette rubrique explique comment collecter des informations sur les travaux d’impression auprès de l’utilisateur.

## <a name="overview"></a>Vue d’ensemble

Collectez les informations de travail d’impression auprès de l’utilisateur en appelant la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Cette fonction affiche la boîte de dialogue d' **impression** commune à l’utilisateur et retourne les informations du travail d’impression dans une structure de données [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

La boîte de dialogue d' **impression** courante s’affiche lorsque l’utilisateur démarre un travail d’impression. La boîte de dialogue **Imprimer** courante est une boîte de dialogue modale, ce qui signifie que l’utilisateur ne peut pas interagir avec la fenêtre principale tant que la boîte de dialogue commune n’est pas fermée.

## <a name="collecting-print-job-information"></a>Collecte des informations sur le travail d’impression

1.  Initialisez l’élément de structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

    Pour qu’un programme puisse afficher la boîte de dialogue d' **impression** commune, il doit allouer et initialiser une structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Il passe ensuite cette structure à la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , qui affiche la boîte de dialogue et retourne les données du travail d’impression dans la même structure. L’exemple de code suivant montre comment l’exemple de programme effectue cette étape.

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  Affiche la boîte de dialogue d' **impression** courante.

    Appelez [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) avec la structure [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) initialisée pour afficher la boîte de dialogue d' **impression** commune et collecter les données utilisateur, comme indiqué dans l’exemple de code suivant.

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  Enregistrez les champs de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et démarrez le travail d’impression.

    La structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contient les données qui décrivent les sélections effectuées par l’utilisateur dans la boîte de dialogue Imprimer. Certains membres de la structure **PRINTDLG** sont des handles d’objets mémoire globaux. L' [exemple de programme Print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copie les données des objets mémoire globaux vers les blocs de mémoire que le programme gère et copie d’autres champs de la structure **PRINTDLG** vers les champs d’une structure de données que le programme a définie.

    Une fois que vous avez stocké les données à partir de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) dans la structure de données du programme, vous pouvez ouvrir la boîte de dialogue progression de l’impression. La procédure de la boîte de dialogue progression de l’impression gère les messages de la boîte de dialogue et démarre le thread de traitement de l’impression.

    L’exemple de code suivant montre comment copier les données de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) vers la structure de données du programme et comment démarrer le travail d’impression.

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  Si l’utilisateur clique sur le bouton **Annuler** dans la boîte de dialogue d' **impression** commune, aucun traitement supplémentaire n’est effectué.

 

 
