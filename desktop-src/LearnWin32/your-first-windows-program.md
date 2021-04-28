---
title: Module 1. Votre premier programme Windows
description: Module 1. Votre premier programme Windows
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110947"
---
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="29295-105">Module 1.</span><span class="sxs-lookup"><span data-stu-id="29295-105">Module 1.</span></span> <span data-ttu-id="29295-106">Votre premier programme Windows</span><span class="sxs-lookup"><span data-stu-id="29295-106">Your First Windows Program</span></span>

<span data-ttu-id="29295-107">Dans ce module, nous allons écrire un programme de bureau Windows minimal.</span><span class="sxs-lookup"><span data-stu-id="29295-107">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="29295-108">Il s’agit de créer et d’afficher une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="29295-108">All it does is create and show a blank window.</span></span> <span data-ttu-id="29295-109">Ce premier programme contient environ 50 lignes de code, sans compter les lignes vides et les commentaires.</span><span class="sxs-lookup"><span data-stu-id="29295-109">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="29295-110">C’est notre point de départ. plus tard, nous ajouterons des graphiques, du texte, des entrées utilisateur et d’autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="29295-110">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="29295-111">Si vous souhaitez plus d’informations sur la création d’une application de bureau Windows traditionnelle dans Visual Studio, consultez  [procédure pas à pas : créer une application de bureau Windows traditionnelle (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="29295-111">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![capture d’écran de l’exemple de programme](images/window01.png)

<span data-ttu-id="29295-113">Voici le code complet du programme :</span><span class="sxs-lookup"><span data-stu-id="29295-113">Here is the complete code for the program:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





<span data-ttu-id="29295-114">Vous pouvez télécharger le projet Visual Studio complet à partir de l' [exemple Windows Hello World](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="29295-114">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="29295-115">Il peut être utile de fournir une brève description de ce que fait ce code.</span><span class="sxs-lookup"><span data-stu-id="29295-115">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="29295-116">Les rubriques ultérieures examinent le code en détail.</span><span class="sxs-lookup"><span data-stu-id="29295-116">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="29295-117">**wWinMain** est le point d’entrée du programme.</span><span class="sxs-lookup"><span data-stu-id="29295-117">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="29295-118">Lorsque le programme démarre, il enregistre des informations sur le comportement de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="29295-118">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="29295-119">L’un des éléments les plus importants est l’adresse d’une fonction, nommée `WindowProc` dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="29295-119">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="29295-120">Cette fonction définit le comportement de la fenêtre : son apparence, son interaction avec l’utilisateur, etc.</span><span class="sxs-lookup"><span data-stu-id="29295-120">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="29295-121">Ensuite, le programme crée la fenêtre et reçoit un handle qui identifie de façon unique la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="29295-121">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="29295-122">Si la fenêtre est créée avec succès, le programme entre une boucle **while** .</span><span class="sxs-lookup"><span data-stu-id="29295-122">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="29295-123">Le programme reste dans cette boucle jusqu’à ce que l’utilisateur ferme la fenêtre et quitte l’application.</span><span class="sxs-lookup"><span data-stu-id="29295-123">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="29295-124">Notez que le programme n’appelle pas explicitement la `WindowProc` fonction, même si nous l’avons dit, c’est là que la plus grande partie de la logique d’application est définie.</span><span class="sxs-lookup"><span data-stu-id="29295-124">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="29295-125">Windows communique avec votre programme en lui transmettant une série de *messages*.</span><span class="sxs-lookup"><span data-stu-id="29295-125">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="29295-126">Le code à l’intérieur de la boucle **while** pilote ce processus.</span><span class="sxs-lookup"><span data-stu-id="29295-126">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="29295-127">Chaque fois que le programme appelle la fonction [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , il force indirectement Windows à appeler la fonction WindowProc, une fois pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="29295-127">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29295-128">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="29295-128">In this section</span></span>

-   [<span data-ttu-id="29295-129">Création d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="29295-129">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="29295-130">Messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="29295-130">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="29295-131">Écriture de la procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="29295-131">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="29295-132">Peindre la fenêtre</span><span class="sxs-lookup"><span data-stu-id="29295-132">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="29295-133">Fermeture de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="29295-133">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="29295-134">Gestion de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="29295-134">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="29295-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29295-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29295-136">Apprendre à programmer pour Windows en C++</span><span class="sxs-lookup"><span data-stu-id="29295-136">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="29295-137">Exemple de Hello World Windows</span><span class="sxs-lookup"><span data-stu-id="29295-137">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
