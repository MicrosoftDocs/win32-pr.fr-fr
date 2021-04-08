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
# <a name="how-to-collect-print-job-information-from-the-user"></a><span data-ttu-id="bbcf0-103">Procédure : collecter des informations de travail d’impression à partir de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bbcf0-103">How To: Collect Print Job Information from the User</span></span>

<span data-ttu-id="bbcf0-104">Cette rubrique explique comment collecter des informations sur les travaux d’impression auprès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-104">This topic describes how to collect print job information from the user.</span></span>

## <a name="overview"></a><span data-ttu-id="bbcf0-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="bbcf0-105">Overview</span></span>

<span data-ttu-id="bbcf0-106">Collectez les informations de travail d’impression auprès de l’utilisateur en appelant la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bbcf0-106">Collect print job information from the user by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="bbcf0-107">Cette fonction affiche la boîte de dialogue d' **impression** commune à l’utilisateur et retourne les informations du travail d’impression dans une structure de données [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="bbcf0-107">This function displays the **Print** common dialog box to the user, and returns the print job information in a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>

<span data-ttu-id="bbcf0-108">La boîte de dialogue d' **impression** courante s’affiche lorsque l’utilisateur démarre un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-108">The **Print** common dialog box is displayed when the user starts a print job.</span></span> <span data-ttu-id="bbcf0-109">La boîte de dialogue **Imprimer** courante est une boîte de dialogue modale, ce qui signifie que l’utilisateur ne peut pas interagir avec la fenêtre principale tant que la boîte de dialogue commune n’est pas fermée.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-109">The **Print** common dialog box is a modal dialog box, which means that the user cannot interact with the main window until the common dialog box is closed.</span></span>

## <a name="collecting-print-job-information"></a><span data-ttu-id="bbcf0-110">Collecte des informations sur le travail d’impression</span><span class="sxs-lookup"><span data-stu-id="bbcf0-110">Collecting Print Job Information</span></span>

1.  <span data-ttu-id="bbcf0-111">Initialisez l’élément de structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="bbcf0-111">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure element.</span></span>

    <span data-ttu-id="bbcf0-112">Pour qu’un programme puisse afficher la boîte de dialogue d' **impression** commune, il doit allouer et initialiser une structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="bbcf0-112">Before a program can display the **Print** common dialog box , it must allocate and initialize a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="bbcf0-113">Il passe ensuite cette structure à la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , qui affiche la boîte de dialogue et retourne les données du travail d’impression dans la même structure.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-113">It then passes this structure to the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, which displays the dialog and returns the print job data in the same structure.</span></span> <span data-ttu-id="bbcf0-114">L’exemple de code suivant montre comment l’exemple de programme effectue cette étape.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-114">The following code example shows how the sample program performs this step.</span></span>

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

    

2.  <span data-ttu-id="bbcf0-115">Affiche la boîte de dialogue d' **impression** courante.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-115">Display the **Print** common dialog box.</span></span>

    <span data-ttu-id="bbcf0-116">Appelez [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) avec la structure [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) initialisée pour afficher la boîte de dialogue d' **impression** commune et collecter les données utilisateur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-116">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) with the initialized [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to display the **Print** common dialog box and collect the user data, as shown in the following code example.</span></span>

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  <span data-ttu-id="bbcf0-117">Enregistrez les champs de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et démarrez le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-117">Save the fields from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and start the print job.</span></span>

    <span data-ttu-id="bbcf0-118">La structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contient les données qui décrivent les sélections effectuées par l’utilisateur dans la boîte de dialogue Imprimer.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-118">The [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure contains the data that describes the selections that the user made in the print dialog box.</span></span> <span data-ttu-id="bbcf0-119">Certains membres de la structure **PRINTDLG** sont des handles d’objets mémoire globaux.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-119">Some members of the **PRINTDLG** structure are handles to global memory objects.</span></span> <span data-ttu-id="bbcf0-120">L' [exemple de programme Print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copie les données des objets mémoire globaux vers les blocs de mémoire que le programme gère et copie d’autres champs de la structure **PRINTDLG** vers les champs d’une structure de données que le programme a définie.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-120">The [Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copies the data from the global memory objects to memory blocks that the program manages and copies other fields from the **PRINTDLG** structure to fields in a data structure that the program defined.</span></span>

    <span data-ttu-id="bbcf0-121">Une fois que vous avez stocké les données à partir de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) dans la structure de données du programme, vous pouvez ouvrir la boîte de dialogue progression de l’impression.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-121">After you store the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure in the program's data structure, you can open the print progress dialog box.</span></span> <span data-ttu-id="bbcf0-122">La procédure de la boîte de dialogue progression de l’impression gère les messages de la boîte de dialogue et démarre le thread de traitement de l’impression.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-122">The print progress dialog box procedure handles the dialog box messages and starts the print processing thread.</span></span>

    <span data-ttu-id="bbcf0-123">L’exemple de code suivant montre comment copier les données de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) vers la structure de données du programme et comment démarrer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-123">The following code example shows how to copy the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to the program's data structure and how to start the print job.</span></span>

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

    

4.  <span data-ttu-id="bbcf0-124">Si l’utilisateur clique sur le bouton **Annuler** dans la boîte de dialogue d' **impression** commune, aucun traitement supplémentaire n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="bbcf0-124">If the user clicks the **Cancel** button in the **Print** common dialog box, no further processing is performed.</span></span>

 

 
