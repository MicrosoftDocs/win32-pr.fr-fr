---
description: Une classe de fenêtre est prise en charge par une procédure de fenêtre. Votre application peut inscrire une classe de fenêtre à l’aide de RegisterClassA ou RegisterClassW. Les nouvelles applications doivent généralement utiliser RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Inscription de classes de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121925"
---
# <a name="registering-window-classes"></a>Inscription de classes de fenêtre

Une classe de fenêtre est prise en charge par une procédure de fenêtre. Votre application peut inscrire une classe de fenêtre à l’aide de [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) ou [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa). Les nouvelles applications doivent généralement utiliser **RegisterClassW**.

si l’application inscrit la classe de fenêtre à l’aide de [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), la fonction informe le système d’exploitation que les fenêtres de la classe créée attendent des messages avec des paramètres texte ou caractère d’utiliser un jeu de caractères de [page de codes Windows (ANSI)](code-pages.md) . L’inscription à l’aide de [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) permet à l’application de demander au système d’exploitation de passer les paramètres de texte des messages au format [Unicode](unicode.md). La fonction [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permet à une application d’interroger la nature de chaque fenêtre.

l’exemple suivant montre comment inscrire une classe de fenêtre de page de codes Windows et une classe de fenêtre Unicode et comment écrire les procédures de fenêtre dans les deux cas. Dans le cadre de cet exemple, toutes les fonctions et structures sont affichées avec les types de données « A » (ANSI) ou « W » (larges, Unicode) spécifiques. à l’aide des techniques expliquées dans [utilisation des types de données génériques](using-generic-data-types.md), vous pouvez également écrire cet exemple pour utiliser des types de données génériques, afin qu’il puisse être compilé pour utiliser Windows pages de codes ou unicode, selon que « unicode » est défini ou non.


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



l’exemple suivant illustre la différence entre la gestion du message [**WM \_ CHAR**](../inputdev/wm-char.md) dans une Windows procédure de fenêtre de la page de codes et une procédure de fenêtre Unicode.


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



tout le texte des messages reçus par **AnsiWndProc** est composé de Windows des caractères de page de codes. Tout le texte des messages reçus par **UniWndProc** est composé de caractères Unicode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’Unicode et de jeux de caractères](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
