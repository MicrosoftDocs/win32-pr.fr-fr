---
title: Comment créer une zone de liste modifiable simple
description: Cette rubrique explique comment créer, ajouter et récupérer des éléments à partir d’une zone de liste déroulante simple.
ms.assetid: E432AEC0-6C06-40C7-BBFE-B66C21DB8ACA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4175d435ac78795e7020fd84099d512cc65be20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463774"
---
# <a name="how-to-create-a-simple-combo-box"></a><span data-ttu-id="0bf77-103">Comment créer une zone de liste modifiable simple</span><span class="sxs-lookup"><span data-stu-id="0bf77-103">How to Create a Simple Combo Box</span></span>

<span data-ttu-id="0bf77-104">Cette rubrique explique comment créer, ajouter et récupérer des éléments à partir d’une zone de liste déroulante simple.</span><span class="sxs-lookup"><span data-stu-id="0bf77-104">This topic describes how to create, add items to, and retrieve items from a simple combo box.</span></span> <span data-ttu-id="0bf77-105">Plus précisément, les exemples de code associés montrent comment exécuter les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0bf77-105">Specifically, the accompanying code examples demonstrate how to perform the following functions:</span></span>

-   <span data-ttu-id="0bf77-106">Créer dynamiquement une zone de liste modifiable simple dans une fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="0bf77-106">Dynamically create a simple combo box in a parent window.</span></span>
-   <span data-ttu-id="0bf77-107">Ajoutez une liste d’éléments à la zone de liste déroulante et affichez un élément initial dans le champ de sélection de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-107">Add a list of items to the combo box and display an initial item in the selection field of the combo box.</span></span>
-   <span data-ttu-id="0bf77-108">Détecte quand l’utilisateur a sélectionné un élément dans la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-108">Detect when the user has selected an item from the combo box.</span></span>
-   <span data-ttu-id="0bf77-109">Récupérez l’élément sélectionné à partir de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-109">Retrieve the selected item from the combo box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0bf77-110">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="0bf77-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0bf77-111">Technologies</span><span class="sxs-lookup"><span data-stu-id="0bf77-111">Technologies</span></span>

-   [<span data-ttu-id="0bf77-112">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="0bf77-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0bf77-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0bf77-113">Prerequisites</span></span>

-   <span data-ttu-id="0bf77-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="0bf77-114">C/C++</span></span>
-   <span data-ttu-id="0bf77-115">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="0bf77-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0bf77-116">Instructions</span><span class="sxs-lookup"><span data-stu-id="0bf77-116">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-combo-box"></a><span data-ttu-id="0bf77-117">Étape 1 : créer une instance de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-117">Step 1: Create an instance of the combo box.</span></span>

<span data-ttu-id="0bf77-118">L’exemple d’application appelle la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre enfant de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="0bf77-118">The example application calls the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a child window of the application window.</span></span> <span data-ttu-id="0bf77-119">Le style de fenêtre [**\_ ComboBox de WC**](common-control-window-classes.md) spécifie qu’il s’agit d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-119">The [**WC\_COMBOBOX**](common-control-window-classes.md) window style specifies that it is a combo box.</span></span>


```C++
// Create the Combobox
//
// Uses the CreateWindow function to create a child window of 
// the application window. The WC_COMBOBOX window style specifies  
// that it is a combobox.

 int xpos = 100;            // Horizontal position of the window.
 int ypos = 100;            // Vertical position of the window.
 int nwidth = 200;          // Width of the window
 int nheight = 200;         // Height of the window
 HWND hwndParent =  m_hwnd; // Handle to the parent window

 HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
     CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
     xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
     NULL);

```



### <a name="step-2-load-the-combo-box-with-the-item-list"></a><span data-ttu-id="0bf77-120">Étape 2 : chargez la zone de liste déroulante avec la liste d’éléments.</span><span class="sxs-lookup"><span data-stu-id="0bf77-120">Step 2: Load the combo box with the item list.</span></span>

<span data-ttu-id="0bf77-121">L’application envoie un message [**CB \_ ADDSTRING**](cb-addstring.md) pour chaque élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="0bf77-121">The application sends a [**CB\_ADDSTRING**](cb-addstring.md) message for each item in the list.</span></span> <span data-ttu-id="0bf77-122">Une fois la liste chargée, l’application envoie le message [**CB \_ SETCURSEL**](cb-setcursel.md) pour afficher un élément initial dans le champ de sélection de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-122">After the list is loaded, the application sends the [**CB\_SETCURSEL**](cb-setcursel.md) message to display an initial item in the combo box selection field.</span></span>


```C++
// load the combobox with item list.  
// Send a CB_ADDSTRING message to load each item

TCHAR Planets[9][10] =  
{
    TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
    TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
    TEXT("Pluto??") 
};
       
TCHAR A[16]; 
int  k = 0; 

memset(&A,0,sizeof(A));       
for (k = 0; k <= 8; k += 1)
{
    wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

    // Add string to combobox.
    SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
}
  
// Send the CB_SETCURSEL message to display an initial item 
//  in the selection field  
SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);
```



### <a name="step-3-detect-when-the-user-selects-an-item-and-retrieve-it-from-the-combo-box"></a><span data-ttu-id="0bf77-123">Étape 3 : détecter quand l’utilisateur sélectionne un élément et le récupérer à partir de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-123">Step 3: Detect when the user selects an item and retrieve it from the combo box.</span></span>

<span data-ttu-id="0bf77-124">Lorsque l’utilisateur effectue une sélection dans la liste, la zone de liste déroulante envoie une notification [CBN \_ selChange](cbn-selchange.md) à la fenêtre parente par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0bf77-124">When the user makes a selection from the list, the combo box sends a [CBN\_SELCHANGE](cbn-selchange.md) notification to the parent window via a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="0bf77-125">L’application récupère le handle de la zone de liste déroulante à partir du champ *lParam* du message de notification et envoie un message [**CB \_ GETCURSEL**](cb-getcursel.md) à la zone de liste déroulante pour récupérer l’index de l’élément de liste sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0bf77-125">The application retrieves the handle to the combo box from the *lParam* field of the notification message and sends a [**CB\_GETCURSEL**](cb-getcursel.md) message to the combo box to retrieve the index of the selected list item.</span></span> <span data-ttu-id="0bf77-126">Après avoir obtenu l’index de l’élément, l’application envoie un message [**CB \_ GETLBTEXT**](cb-getlbtext.md) pour obtenir l’élément.</span><span class="sxs-lookup"><span data-stu-id="0bf77-126">After obtaining the item index, the application sends a [**CB\_GETLBTEXT**](cb-getlbtext.md) message to get the item.</span></span> <span data-ttu-id="0bf77-127">Il affiche ensuite l’élément dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="0bf77-127">It then displays the item in a message box.</span></span>

> [!Note]  
> <span data-ttu-id="0bf77-128">La notification [CBN \_ selChange](cbn-selchange.md) est envoyée et traitée avant que l’élément ne soit placé dans le champ de sélection de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0bf77-128">The [CBN\_SELCHANGE](cbn-selchange.md) notification is sent and processed before the item is placed in the combo box selection field.</span></span> <span data-ttu-id="0bf77-129">Par conséquent, dans cet exemple, l’élément sélectionné n’apparaît pas dans le champ de sélection tant que la boîte de message n’a pas été fermée.</span><span class="sxs-lookup"><span data-stu-id="0bf77-129">As result, in this example, the selected item won't appear in selection field until after the message box is closed.</span></span>

 


```C++
switch (message)
{   
    case WM_COMMAND:

        if(HIWORD(wParam) == CBN_SELCHANGE)
        // If the user makes a selection from the list:
        //   Send CB_GETCURSEL message to get the index of the selected list item.
        //   Send CB_GETLBTEXT message to get the item.
        //   Display the item in a messagebox.
        { 
            int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                (WPARAM) 0, (LPARAM) 0);
                TCHAR  ListItem[256];
                (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                (WPARAM) ItemIndex, (LPARAM) ListItem);
            MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
        }
        
        wasHandled = true;
    result = 0;
    break;
```



## <a name="complete-example"></a><span data-ttu-id="0bf77-130">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="0bf77-130">Complete example</span></span>


```C++
// Windows Header Files:
#include <windows.h>
#include <CommCtrl.h>

// C RunTime Header Files
#include <math.h>

#include <objbase.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef Assert
#if defined( DEBUG ) || defined( _DEBUG )
#define Assert(b) if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}
#else
#define Assert(b)
#endif //DEBUG || _DEBUG
#endif


#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT CreateResources();
    void DiscardResources();

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;

 };
```


```C++
#include "SimpleComboBox.h"

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE     /* hInstance */,
    HINSTANCE     /* hPrevInstance */,
    LPSTR     /* lpCmdLine */,
    int     /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                        *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()        
{
    // TODO: Release app resource here.
}

/*******************************************************************
*                                                                  *
*  Create the application window and the combobox.                 *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = TEXT("DemoApp");

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        TEXT("DemoApp"),
        TEXT("Simple Combo Box Example"),
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwnd, SW_SHOWNORMAL);
        UpdateWindow(m_hwnd);
    }


    // Create the Combobox
    //
    // Uses the CreateWindow function to create a child window of 
    // the application window. The WC_COMBOBOX window style specifies  
    // that it is a combobox.

     int xpos = 100;            // Horizontal position of the window.
     int ypos = 100;            // Vertical position of the window.
     int nwidth = 200;          // Width of the window
     int nheight = 200;         // Height of the window
     HWND hwndParent =  m_hwnd; // Handle to the parent window

     HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
         CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
         xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
         NULL);


    
    // load the combobox with item list.  
    // Send a CB_ADDSTRING message to load each item

    TCHAR Planets[9][10] =  
    {
        TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
        TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
        TEXT("Pluto??") 
    };
           
    TCHAR A[16]; 
    int  k = 0; 

    memset(&A,0,sizeof(A));       
    for (k = 0; k <= 8; k += 1)
    {
        wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

        // Add string to combobox.
        SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
    }
      
    // Send the CB_SETCURSEL message to display an initial item 
    //  in the selection field  
    SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);

    return hr;
}


/******************************************************************
*                                                                 *
*  The main window's message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}


/******************************************************************
*                                                                 *
*  The window's message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {   
                case WM_COMMAND:

                    if(HIWORD(wParam) == CBN_SELCHANGE)
                    // If the user makes a selection from the list:
                    //   Send CB_GETCURSEL message to get the index of the selected list item.
                    //   Send CB_GETLBTEXT message to get the item.
                    //   Display the item in a messagebox.
                    { 
                        int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                            (WPARAM) 0, (LPARAM) 0);
                            TCHAR  ListItem[256];
                            (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                            (WPARAM) ItemIndex, (LPARAM) ListItem);
                        MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
                    }
                    
                    wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
```


## <a name="related-topics"></a><span data-ttu-id="0bf77-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0bf77-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf77-132">À propos des zones de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="0bf77-132">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="0bf77-133">Référence du contrôle ComboBox</span><span class="sxs-lookup"><span data-stu-id="0bf77-133">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0bf77-134">Utilisation de zones de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="0bf77-134">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="0bf77-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="0bf77-135">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 