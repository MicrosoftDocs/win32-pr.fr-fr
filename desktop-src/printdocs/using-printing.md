---
description: Cette section décrit comment imprimer à partir d’un programme de bureau Windows natif.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Impression d’applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520725"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="65336-103">Impression d’applications de bureau</span><span class="sxs-lookup"><span data-stu-id="65336-103">Desktop App Printing</span></span>

<span data-ttu-id="65336-104">Cette section décrit comment imprimer à partir d’un programme de bureau Windows natif.</span><span class="sxs-lookup"><span data-stu-id="65336-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="65336-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="65336-105">Overview</span></span>

<span data-ttu-id="65336-106">Pour offrir une expérience utilisateur optimale lorsque vous imprimez à partir d’un programme Windows natif, le programme doit être conçu pour imprimer à partir d’un thread dédié.</span><span class="sxs-lookup"><span data-stu-id="65336-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="65336-107">Dans un programme Windows natif, le programme est responsable de la gestion des événements et des messages de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65336-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="65336-108">Les opérations d’impression peuvent nécessiter des périodes de calcul intense lorsque le contenu de l’application est rendu pour l’imprimante, ce qui peut empêcher le programme de répondre à l’interaction de l’utilisateur si ce traitement est effectué dans le même thread que le traitement des événements de l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65336-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="65336-109">Si vous êtes déjà familiarisé avec l’écriture d’un programme Windows natif multithread, passez directement à [la rubrique Comment imprimer à partir d’une application Windows](how-to--print-from-a-windows-application.md) et comment ajouter des fonctionnalités d’impression à votre programme.</span><span class="sxs-lookup"><span data-stu-id="65336-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="65336-110">Configuration de base des programmes Windows</span><span class="sxs-lookup"><span data-stu-id="65336-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="65336-111">Pour optimiser les performances et la réactivité du programme, n’effectuez pas le traitement du travail d’impression d’un programme dans le thread qui traite l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65336-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="65336-112">Cette séparation de l’interaction de l’utilisateur influencera la manière dont le programme gère les données d’application.</span><span class="sxs-lookup"><span data-stu-id="65336-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="65336-113">Vous devez parfaitement comprendre ces implications avant de commencer à écrire l’application.</span><span class="sxs-lookup"><span data-stu-id="65336-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="65336-114">Les rubriques suivantes décrivent les exigences de base de la gestion de l’impression dans un thread distinct d’un programme.</span><span class="sxs-lookup"><span data-stu-id="65336-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="65336-115">Notions de base des programmes Windows</span><span class="sxs-lookup"><span data-stu-id="65336-115">Windows Program Basics</span></span>

<span data-ttu-id="65336-116">Un programme Windows natif doit fournir la procédure de fenêtre principale pour traiter les messages de fenêtre qu’il reçoit du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="65336-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="65336-117">Chaque fenêtre d’un programme Windows dispose d’une fonction **WndProc** correspondante qui traite ces messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="65336-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="65336-118">Le thread dans lequel cette fonction s’exécute est appelé le thread de l’interface utilisateur ou de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65336-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="65336-119">**Utilisez des ressources pour les chaînes.**</span><span class="sxs-lookup"><span data-stu-id="65336-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="65336-120">Utilisez des ressources de type chaîne à partir du fichier de ressources du programme plutôt que des constantes de chaîne pour les chaînes qui devront peut-être être modifiées lorsque vous prenez en charge un autre langage.</span><span class="sxs-lookup"><span data-stu-id="65336-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="65336-121">Pour qu’un programme puisse utiliser une ressource de type chaîne comme chaîne, le programme doit récupérer la ressource à partir du fichier de ressources et la copier dans une mémoire tampon locale.</span><span class="sxs-lookup"><span data-stu-id="65336-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="65336-122">Cela nécessite une programmation supplémentaire au début, mais permet une modification, une traduction et une localisation plus faciles du programme à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="65336-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="65336-123">**Traiter les données en étapes.**</span><span class="sxs-lookup"><span data-stu-id="65336-123">**Process data in steps.**</span></span>  
<span data-ttu-id="65336-124">Traitez le travail d’impression dans les étapes qui peuvent être interrompues.</span><span class="sxs-lookup"><span data-stu-id="65336-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="65336-125">Cette conception permet à l’utilisateur d’annuler une longue opération de traitement avant qu’elle ne se termine et empêche le programme de bloquer d’autres programmes qui peuvent s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="65336-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="65336-126">**Utilisez les données utilisateur de la fenêtre.**</span><span class="sxs-lookup"><span data-stu-id="65336-126">**Use window user data.**</span></span>  
<span data-ttu-id="65336-127">L’impression d’applications a souvent plusieurs fenêtres et threads.</span><span class="sxs-lookup"><span data-stu-id="65336-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="65336-128">Pour conserver les données disponibles entre les threads et les étapes de traitement sans utiliser des variables globales statiques, référencez les structures de données à l’aide d’un pointeur de données qui fait partie de la fenêtre dans laquelle elles sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="65336-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="65336-129">L’exemple de code suivant montre un point d’entrée principal pour une application d’impression.</span><span class="sxs-lookup"><span data-stu-id="65336-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="65336-130">Cet exemple montre comment utiliser des ressources de type chaîne à la place de constantes de chaîne et affiche également la boucle de message principale qui traite les messages de fenêtre du programme.</span><span class="sxs-lookup"><span data-stu-id="65336-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="65336-131">Informations sur le document</span><span class="sxs-lookup"><span data-stu-id="65336-131">Document Information</span></span>

<span data-ttu-id="65336-132">Les programmes Windows natifs qui impriment doivent être conçus pour le traitement multithread.</span><span class="sxs-lookup"><span data-stu-id="65336-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="65336-133">L’une des exigences d’une conception multithread consiste à protéger les éléments de données du programme afin qu’ils puissent être utilisés simultanément par plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="65336-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="65336-134">Vous pouvez protéger les éléments de données en utilisant des objets de synchronisation et en organisant les données pour éviter les conflits entre les threads.</span><span class="sxs-lookup"><span data-stu-id="65336-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="65336-135">En même temps, le programme doit empêcher toute modification des données du programme pendant son impression.</span><span class="sxs-lookup"><span data-stu-id="65336-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="65336-136">L’exemple de programme utilise plusieurs techniques de programmation multithread différentes.</span><span class="sxs-lookup"><span data-stu-id="65336-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="65336-137">**Événements de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="65336-137">**Synchronization Events**</span></span>  
<span data-ttu-id="65336-138">L’exemple de programme utilise des événements, des handles de thread et des fonctions Wait pour synchroniser le traitement entre le thread d’impression et le programme principal et pour indiquer que les données sont en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="65336-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="65336-139">**Messages Windows spécifiques à l’application**</span><span class="sxs-lookup"><span data-stu-id="65336-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="65336-140">L’exemple de programme utilise des messages de fenêtre spécifiques à l’application pour rendre le programme plus compatible avec d’autres programmes Windows natifs.</span><span class="sxs-lookup"><span data-stu-id="65336-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="65336-141">Le fractionnement du traitement en étapes plus petites et la mise en file d’attente de ces étapes dans la boucle de message de fenêtre permet à Windows de gérer plus facilement le traitement sans bloquer d’autres applications qui peuvent également s’exécuter sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="65336-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="65336-142">**Structures de données**</span><span class="sxs-lookup"><span data-stu-id="65336-142">**Data Structures**</span></span>  
<span data-ttu-id="65336-143">L’exemple de programme n’est pas écrit dans un style orienté objet à l’aide d’objets et de classes, bien qu’il regroupe des éléments de données dans des structures de données.</span><span class="sxs-lookup"><span data-stu-id="65336-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="65336-144">L’exemple n’utilise pas une approche orientée objet pour éviter d’impliquer qu’une approche est mieux ou pire qu’une autre.</span><span class="sxs-lookup"><span data-stu-id="65336-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="65336-145">Vous pouvez utiliser les fonctions et les structures de données de l’exemple de programme comme point de départ lors de la conception de votre programme.</span><span class="sxs-lookup"><span data-stu-id="65336-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="65336-146">Que vous décidiez de concevoir un programme orienté objet ou non, il est important de se rappeler que vous devez regrouper les éléments de données associés afin de pouvoir les utiliser en toute sécurité dans différents threads si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="65336-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="65336-147">Contexte de périphérique d’impression</span><span class="sxs-lookup"><span data-stu-id="65336-147">Printer Device Context</span></span>

<span data-ttu-id="65336-148">Lors de l’impression, vous souhaiterez peut-être afficher le contenu à imprimer dans un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="65336-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="65336-149">[Comment : récupérer un contexte de périphérique d’impression](retrieving-a-printer-device-context.md) décrit les différentes façons dont vous pouvez obtenir un contexte de périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="65336-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65336-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65336-150">Related topics</span></span>



[<span data-ttu-id="65336-151">Comment imprimer à partir d’une application Windows</span><span class="sxs-lookup"><span data-stu-id="65336-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



