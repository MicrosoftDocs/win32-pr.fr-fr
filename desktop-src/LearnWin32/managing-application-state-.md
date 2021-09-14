---
title: Gestion de l’état de l’application
description: Une procédure de fenêtre est simplement une fonction qui est appelée pour chaque message. par conséquent, elle est fondamentalement sans État. Par conséquent, vous avez besoin d’un moyen d’effectuer le suivi de l’état de votre application à partir d’un appel de fonction à la suivante.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094361"
---
# <a name="managing-application-state"></a>Gestion de l’état de l’application

Une procédure de fenêtre est simplement une fonction qui est appelée pour chaque message. par conséquent, elle est fondamentalement sans État. Par conséquent, vous avez besoin d’un moyen d’effectuer le suivi de l’état de votre application à partir d’un appel de fonction à la suivante.

L’approche la plus simple consiste simplement à tout placer dans des variables globales. Cela fonctionne suffisamment bien pour les petits programmes, et la plupart des exemples du kit de développement logiciel (SDK) utilisent cette approche. Toutefois, dans un programme volumineux, il s’agit d’une prolifération des variables globales. En outre, vous pouvez avoir plusieurs fenêtres, chacune avec sa propre procédure de fenêtre. Assurer le suivi de la fenêtre qui doit accéder aux variables qui deviennent confuses et sujettes aux erreurs.

La fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) offre un moyen de passer toute structure de données à une fenêtre. Lorsque cette fonction est appelée, elle envoie les deux messages suivants à votre procédure de fenêtre :

- [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)
- [**création de WM \_**](/windows/desktop/winmsg/wm-create)

Ces messages sont envoyés dans l’ordre indiqué. (Il ne s’agit pas des deux messages envoyés au cours de la transmission [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), mais nous pouvons ignorer les autres pour cette discussion.)

Le [**\_ NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate) et le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) sont envoyés avant que la fenêtre ne soit visible. Cela leur permet d’initialiser votre interface utilisateur, par exemple pour déterminer la disposition initiale de la fenêtre.

Le dernier paramètre de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) est un pointeur de type **void \** _. Vous pouvez passer n’importe quelle valeur de pointeur dans ce paramètre. Lorsque la procédure de fenêtre gère le message [_ *WM \_ NCCREATE* *](/windows/desktop/winmsg/wm-nccreate) ou [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , elle peut extraire cette valeur des données de message.

Voyons comment utiliser ce paramètre pour transmettre des données d’application à votre fenêtre. Tout d’abord, définissez une classe ou une structure qui contient les informations d’État.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Lorsque vous appelez [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), transmettez un pointeur vers cette structure dans le **paramètre \* void** final.

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

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
    pState      // Additional application data
    );
```

Quand vous recevez les [**messages \_ WM NCCREATE**](/windows/desktop/winmsg/wm-nccreate) et [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , le paramètre *lParam* de chaque message est un pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . La structure **CREATESTRUCT** contient, à son tour, le pointeur que vous avez passé à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

![diagramme qui affiche la disposition de la structure CREATESTRUCT](images/appstate01.png)

Voici comment extraire le pointeur vers votre structure de données. Tout d’abord, récupérez la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) en effectuant un cast du paramètre *lParam* .

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

Le membre **lpCreateParams** de la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) est le pointeur void d’origine que vous avez spécifié dans [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Obtenir un pointeur vers votre propre structure de données en convertissant **lpCreateParams**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Ensuite, appelez la fonction [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) et transmettez le pointeur à votre structure de données.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

L’objectif de ce dernier appel de fonction est de stocker le pointeur *fichier stateInfo* dans les données d’instance pour la fenêtre. Une fois que vous avez fait cela, vous pouvez toujours récupérer le pointeur à partir de la fenêtre en appelant [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Chaque fenêtre possède ses propres données d’instance, ce qui vous permet de créer plusieurs fenêtres et d’attribuer à chaque fenêtre sa propre instance de la structure de données. Cette approche est particulièrement utile si vous définissez une classe de fenêtres et que vous créez plusieurs fenêtres de cette classe, par exemple, si vous créez une classe de contrôle personnalisée. Il est pratique d’encapsuler l’appel [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) dans une fonction d’assistance de petite taille.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

Vous pouvez maintenant écrire votre procédure de fenêtre comme suit.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a>Une approche Object-Oriented

Nous pouvons étendre cette approche plus en détail. Nous avons déjà défini une structure de données pour contenir les informations d’État relatives à la fenêtre. Il est logique de fournir cette structure de données avec des fonctions membres (méthodes) qui opèrent sur les données. Cela amène naturellement une conception dans laquelle la structure (ou la classe) est responsable de toutes les opérations sur la fenêtre. La procédure de fenêtre devient alors partie intégrante de la classe.

En d’autres termes, nous aimerions :

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

Par ceci :

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

Le seul problème est la façon de raccorder la `MyWindow::WindowProc` méthode. La fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) s’attend à ce que la procédure de fenêtre soit un pointeur de fonction. Vous ne pouvez pas passer un pointeur vers une fonction membre (non statique) dans ce contexte. Toutefois, vous pouvez passer un pointeur vers une fonction membre *statique* , puis déléguer à la fonction membre. Voici un modèle de classe qui illustre cette approche :

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

La `BaseWindow` classe est une classe de base abstraite, à partir de laquelle des classes de fenêtre spécifiques sont dérivées. Par exemple, voici la déclaration d’une classe simple dérivée de `BaseWindow` :

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Pour créer la fenêtre, appelez `BaseWindow::Create` :

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

La méthode virtuelle pure `BaseWindow::HandleMessage` est utilisée pour implémenter la procédure de fenêtre. Par exemple, l’implémentation suivante est équivalente à la procédure de fenêtre indiquée au début du [module 1](your-first-windows-program.md).

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

Notez que le descripteur de fenêtre est stocké dans une variable membre (*m \_ HWND*). nous n’avons donc pas besoin de le passer en tant que paramètre à `HandleMessage` .

la plupart des infrastructures de programmation d’Windows existantes, telles que Microsoft Foundation Classes (MFC) et Active Template Library (ATL), utilisent des approches qui sont fondamentalement similaires à celle présentée ici. Bien entendu, un Framework entièrement généralisé comme MFC est plus complexe que cet exemple relativement simpliste.

## <a name="next"></a>Suivant

[Module 2 : utilisation de COM dans votre programme Windows](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Rubriques connexes

[Exemple BaseWindow](basewindow-sample.md)