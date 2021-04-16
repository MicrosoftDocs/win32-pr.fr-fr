---
title: Module 1. Votre premier programme Windows
description: .
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27749cddabaefb4fd83b836887fbb2dac017d238
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104562437"
---
# <a name="module-1-your-first-windows-program"></a>Module 1. Votre premier programme Windows

Dans ce module, nous allons écrire un programme de bureau Windows minimal. Il s’agit de créer et d’afficher une fenêtre vide. Ce premier programme contient environ 50 lignes de code, sans compter les lignes vides et les commentaires. C’est notre point de départ. plus tard, nous ajouterons des graphiques, du texte, des entrées utilisateur et d’autres fonctionnalités.

Si vous souhaitez plus d’informations sur la création d’une application de bureau Windows traditionnelle dans Visual Studio, consultez  [procédure pas à pas : créer une application de bureau Windows traditionnelle (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).

![capture d’écran de l’exemple de programme](images/window01.png)

Voici le code complet du programme :


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





Vous pouvez télécharger le projet Visual Studio complet à partir de l' [exemple Windows Hello World](windows-hello-world-sample.md).

Il peut être utile de fournir une brève description de ce que fait ce code. Les rubriques ultérieures examinent le code en détail.

1.  **wWinMain** est le point d’entrée du programme. Lorsque le programme démarre, il enregistre des informations sur le comportement de la fenêtre d’application. L’un des éléments les plus importants est l’adresse d’une fonction, nommée `WindowProc` dans cet exemple. Cette fonction définit le comportement de la fenêtre : son apparence, son interaction avec l’utilisateur, etc.
2.  Ensuite, le programme crée la fenêtre et reçoit un handle qui identifie de façon unique la fenêtre.
3.  Si la fenêtre est créée avec succès, le programme entre une boucle **while** . Le programme reste dans cette boucle jusqu’à ce que l’utilisateur ferme la fenêtre et quitte l’application.

Notez que le programme n’appelle pas explicitement la `WindowProc` fonction, même si nous l’avons dit, c’est là que la plus grande partie de la logique d’application est définie. Windows communique avec votre programme en lui transmettant une série de *messages*. Le code à l’intérieur de la boucle **while** pilote ce processus. Chaque fois que le programme appelle la fonction [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , il force indirectement Windows à appeler la fonction WindowProc, une fois pour chaque message.

## <a name="in-this-section"></a>Dans cette section

-   [Création d’une fenêtre](creating-a-window.md)
-   [Messages de fenêtre](window-messages.md)
-   [Écriture de la procédure de fenêtre](writing-the-window-procedure.md)
-   [Peindre la fenêtre](painting-the-window.md)
-   [Fermeture de la fenêtre](closing-the-window.md)
-   [Gestion de l’état de l’application](managing-application-state-.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Apprendre à programmer pour Windows en C++](learn-to-program-for-windows.md)
</dt> <dt>

[Exemple de Hello World Windows](windows-hello-world-sample.md)
</dt> </dl>

 

 
