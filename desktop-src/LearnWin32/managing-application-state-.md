---
title: Gestion de l’état de l’application
description: Une procédure de fenêtre est simplement une fonction qui est appelée pour chaque message. par conséquent, elle est fondamentalement sans État. Par conséquent, vous avez besoin d’un moyen d’effectuer le suivi de l’état de votre application à partir d’un appel de fonction à la suivante.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031215"
---
# <a name="managing-application-state"></a><span data-ttu-id="bc11c-104">Gestion de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="bc11c-104">Managing Application State</span></span>

<span data-ttu-id="bc11c-105">Une procédure de fenêtre est simplement une fonction qui est appelée pour chaque message. par conséquent, elle est fondamentalement sans État.</span><span class="sxs-lookup"><span data-stu-id="bc11c-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="bc11c-106">Par conséquent, vous avez besoin d’un moyen d’effectuer le suivi de l’état de votre application à partir d’un appel de fonction à la suivante.</span><span class="sxs-lookup"><span data-stu-id="bc11c-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="bc11c-107">L’approche la plus simple consiste simplement à tout placer dans des variables globales.</span><span class="sxs-lookup"><span data-stu-id="bc11c-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="bc11c-108">Cela fonctionne suffisamment bien pour les petits programmes, et la plupart des exemples du kit de développement logiciel (SDK) utilisent cette approche.</span><span class="sxs-lookup"><span data-stu-id="bc11c-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="bc11c-109">Toutefois, dans un programme volumineux, il s’agit d’une prolifération des variables globales.</span><span class="sxs-lookup"><span data-stu-id="bc11c-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="bc11c-110">En outre, vous pouvez avoir plusieurs fenêtres, chacune avec sa propre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="bc11c-111">Assurer le suivi de la fenêtre qui doit accéder aux variables qui deviennent confuses et sujettes aux erreurs.</span><span class="sxs-lookup"><span data-stu-id="bc11c-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="bc11c-112">La fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) offre un moyen de passer toute structure de données à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="bc11c-113">Lorsque cette fonction est appelée, elle envoie les deux messages suivants à votre procédure de fenêtre :</span><span class="sxs-lookup"><span data-stu-id="bc11c-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="bc11c-114">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="bc11c-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="bc11c-115">**création de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bc11c-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="bc11c-116">Ces messages sont envoyés dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="bc11c-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="bc11c-117">(Il ne s’agit pas des deux messages envoyés au cours de la transmission [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), mais nous pouvons ignorer les autres pour cette discussion.)</span><span class="sxs-lookup"><span data-stu-id="bc11c-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="bc11c-118">Le [**\_ NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate) et le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) sont envoyés avant que la fenêtre ne soit visible.</span><span class="sxs-lookup"><span data-stu-id="bc11c-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="bc11c-119">Cela leur permet d’initialiser votre interface utilisateur, par exemple pour déterminer la disposition initiale de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="bc11c-120">Le dernier paramètre de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) est un pointeur de type **void \***.</span><span class="sxs-lookup"><span data-stu-id="bc11c-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="bc11c-121">Vous pouvez passer n’importe quelle valeur de pointeur dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="bc11c-122">Lorsque la procédure de fenêtre gère le message [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) ou [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , elle peut extraire cette valeur des données de message.</span><span class="sxs-lookup"><span data-stu-id="bc11c-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="bc11c-123">Voyons comment utiliser ce paramètre pour transmettre des données d’application à votre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="bc11c-124">Tout d’abord, définissez une classe ou une structure qui contient les informations d’État.</span><span class="sxs-lookup"><span data-stu-id="bc11c-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="bc11c-125">Lorsque vous appelez [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), transmettez un pointeur vers cette structure dans le **paramètre \* void** final.</span><span class="sxs-lookup"><span data-stu-id="bc11c-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

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

<span data-ttu-id="bc11c-126">Quand vous recevez les [**messages \_ WM NCCREATE**](/windows/desktop/winmsg/wm-nccreate) et [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , le paramètre *lParam* de chaque message est un pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="bc11c-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="bc11c-127">La structure **CREATESTRUCT** contient, à son tour, le pointeur que vous avez passé à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="bc11c-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![diagramme qui affiche la disposition de la structure CREATESTRUCT](images/appstate01.png)

<span data-ttu-id="bc11c-129">Voici comment extraire le pointeur vers votre structure de données.</span><span class="sxs-lookup"><span data-stu-id="bc11c-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="bc11c-130">Tout d’abord, récupérez la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) en effectuant un cast du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="bc11c-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="bc11c-131">Le membre **lpCreateParams** de la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) est le pointeur void d’origine que vous avez spécifié dans [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="bc11c-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="bc11c-132">Obtenir un pointeur vers votre propre structure de données en convertissant **lpCreateParams**.</span><span class="sxs-lookup"><span data-stu-id="bc11c-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="bc11c-133">Ensuite, appelez la fonction [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) et transmettez le pointeur à votre structure de données.</span><span class="sxs-lookup"><span data-stu-id="bc11c-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="bc11c-134">L’objectif de ce dernier appel de fonction est de stocker le pointeur *fichier stateInfo* dans les données d’instance pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="bc11c-135">Une fois que vous avez fait cela, vous pouvez toujours récupérer le pointeur à partir de la fenêtre en appelant [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span><span class="sxs-lookup"><span data-stu-id="bc11c-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="bc11c-136">Chaque fenêtre possède ses propres données d’instance, ce qui vous permet de créer plusieurs fenêtres et d’attribuer à chaque fenêtre sa propre instance de la structure de données.</span><span class="sxs-lookup"><span data-stu-id="bc11c-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="bc11c-137">Cette approche est particulièrement utile si vous définissez une classe de fenêtres et que vous créez plusieurs fenêtres de cette classe, par exemple, si vous créez une classe de contrôle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="bc11c-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="bc11c-138">Il est pratique d’encapsuler l’appel [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) dans une fonction d’assistance de petite taille.</span><span class="sxs-lookup"><span data-stu-id="bc11c-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="bc11c-139">Vous pouvez maintenant écrire votre procédure de fenêtre comme suit.</span><span class="sxs-lookup"><span data-stu-id="bc11c-139">Now you can write your window procedure as follows.</span></span>

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

## <a name="an-object-oriented-approach"></a><span data-ttu-id="bc11c-140">Une approche Object-Oriented</span><span class="sxs-lookup"><span data-stu-id="bc11c-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="bc11c-141">Nous pouvons étendre cette approche plus en détail.</span><span class="sxs-lookup"><span data-stu-id="bc11c-141">We can extend this approach further.</span></span> <span data-ttu-id="bc11c-142">Nous avons déjà défini une structure de données pour contenir les informations d’État relatives à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="bc11c-143">Il est logique de fournir cette structure de données avec des fonctions membres (méthodes) qui opèrent sur les données.</span><span class="sxs-lookup"><span data-stu-id="bc11c-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="bc11c-144">Cela amène naturellement une conception dans laquelle la structure (ou la classe) est responsable de toutes les opérations sur la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="bc11c-145">La procédure de fenêtre devient alors partie intégrante de la classe.</span><span class="sxs-lookup"><span data-stu-id="bc11c-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="bc11c-146">En d’autres termes, nous aimerions :</span><span class="sxs-lookup"><span data-stu-id="bc11c-146">In other words, we would like to go from this:</span></span>

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

<span data-ttu-id="bc11c-147">Par ceci :</span><span class="sxs-lookup"><span data-stu-id="bc11c-147">To this:</span></span>

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

<span data-ttu-id="bc11c-148">Le seul problème est la façon de raccorder la `MyWindow::WindowProc` méthode.</span><span class="sxs-lookup"><span data-stu-id="bc11c-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="bc11c-149">La fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) s’attend à ce que la procédure de fenêtre soit un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="bc11c-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="bc11c-150">Vous ne pouvez pas passer un pointeur vers une fonction membre (non statique) dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="bc11c-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="bc11c-151">Toutefois, vous pouvez passer un pointeur vers une fonction membre *statique* , puis déléguer à la fonction membre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="bc11c-152">Voici un modèle de classe qui illustre cette approche :</span><span class="sxs-lookup"><span data-stu-id="bc11c-152">Here is a class template that shows this approach:</span></span>

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

<span data-ttu-id="bc11c-153">La `BaseWindow` classe est une classe de base abstraite, à partir de laquelle des classes de fenêtre spécifiques sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="bc11c-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="bc11c-154">Par exemple, voici la déclaration d’une classe simple dérivée de `BaseWindow` :</span><span class="sxs-lookup"><span data-stu-id="bc11c-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="bc11c-155">Pour créer la fenêtre, appelez `BaseWindow::Create` :</span><span class="sxs-lookup"><span data-stu-id="bc11c-155">To create the window, call `BaseWindow::Create`:</span></span>

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

<span data-ttu-id="bc11c-156">La méthode virtuelle pure `BaseWindow::HandleMessage` est utilisée pour implémenter la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bc11c-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="bc11c-157">Par exemple, l’implémentation suivante est équivalente à la procédure de fenêtre indiquée au début du [module 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="bc11c-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

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

<span data-ttu-id="bc11c-158">Notez que le descripteur de fenêtre est stocké dans une variable membre (*m \_ HWND*). nous n’avons donc pas besoin de le passer en tant que paramètre à `HandleMessage` .</span><span class="sxs-lookup"><span data-stu-id="bc11c-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="bc11c-159">La plupart des infrastructures de programmation Windows existantes, telles que Microsoft Foundation Classes (MFC) et Active Template Library (ATL), utilisent des approches qui sont fondamentalement similaires à celle illustrée ici.</span><span class="sxs-lookup"><span data-stu-id="bc11c-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="bc11c-160">Bien entendu, un Framework entièrement généralisé comme MFC est plus complexe que cet exemple relativement simpliste.</span><span class="sxs-lookup"><span data-stu-id="bc11c-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="bc11c-161">Suivant</span><span class="sxs-lookup"><span data-stu-id="bc11c-161">Next</span></span>

[<span data-ttu-id="bc11c-162">Module 2 : utilisation de COM dans votre programme Windows</span><span class="sxs-lookup"><span data-stu-id="bc11c-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="bc11c-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc11c-163">Related topics</span></span>

[<span data-ttu-id="bc11c-164">Exemple BaseWindow</span><span class="sxs-lookup"><span data-stu-id="bc11c-164">BaseWindow Sample</span></span>](basewindow-sample.md)