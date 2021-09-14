---
title: Comment créer une zone de liste modifiable simple
description: Cette rubrique explique comment créer, ajouter et récupérer des éléments à partir d’une zone de liste déroulante simple.
ms.assetid: E432AEC0-6C06-40C7-BBFE-B66C21DB8ACA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4175d435ac78795e7020fd84099d512cc65be20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095001"
---
# <a name="how-to-create-a-simple-combo-box"></a>Comment créer une zone de liste modifiable simple

Cette rubrique explique comment créer, ajouter et récupérer des éléments à partir d’une zone de liste déroulante simple. Plus précisément, les exemples de code associés montrent comment exécuter les fonctions suivantes :

-   Créer dynamiquement une zone de liste modifiable simple dans une fenêtre parente.
-   Ajoutez une liste d’éléments à la zone de liste déroulante et affichez un élément initial dans le champ de sélection de la zone de liste déroulante.
-   Détecte quand l’utilisateur a sélectionné un élément dans la zone de liste déroulante.
-   Récupérez l’élément sélectionné à partir de la zone de liste déroulante.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-combo-box"></a>Étape 1 : créer une instance de la zone de liste déroulante.

L’exemple d’application appelle la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre enfant de la fenêtre d’application. Le style de fenêtre [**\_ ComboBox de WC**](common-control-window-classes.md) spécifie qu’il s’agit d’une zone de liste déroulante.


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



### <a name="step-2-load-the-combo-box-with-the-item-list"></a>Étape 2 : chargez la zone de liste déroulante avec la liste d’éléments.

L’application envoie un message [**CB \_ ADDSTRING**](cb-addstring.md) pour chaque élément de la liste. Une fois la liste chargée, l’application envoie le message [**CB \_ SETCURSEL**](cb-setcursel.md) pour afficher un élément initial dans le champ de sélection de zone de liste déroulante.


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



### <a name="step-3-detect-when-the-user-selects-an-item-and-retrieve-it-from-the-combo-box"></a>Étape 3 : détecter quand l’utilisateur sélectionne un élément et le récupérer à partir de la zone de liste déroulante.

Lorsque l’utilisateur effectue une sélection dans la liste, la zone de liste déroulante envoie une notification [CBN \_ selChange](cbn-selchange.md) à la fenêtre parente par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . L’application récupère le handle de la zone de liste déroulante à partir du champ *lParam* du message de notification et envoie un message [**CB \_ GETCURSEL**](cb-getcursel.md) à la zone de liste déroulante pour récupérer l’index de l’élément de liste sélectionné. Après avoir obtenu l’index de l’élément, l’application envoie un message [**CB \_ GETLBTEXT**](cb-getlbtext.md) pour obtenir l’élément. Il affiche ensuite l’élément dans une boîte de message.

> [!Note]  
> La notification [CBN \_ selChange](cbn-selchange.md) est envoyée et traitée avant que l’élément ne soit placé dans le champ de sélection de zone de liste déroulante. Par conséquent, dans cet exemple, l’élément sélectionné n’apparaît pas dans le champ de sélection tant que la boîte de message n’a pas été fermée.

 


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



## <a name="complete-example"></a>Exemple complet


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


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des zones de liste modifiable](about-combo-boxes.md)
</dt> <dt>

[Référence du contrôle ComboBox](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[Utilisation de zones de liste déroulante](using-combo-boxes.md)
</dt> <dt>

[ComboBox](combo-boxes.md)
</dt> </dl>

 

 