---
title: Création d’une application Direct2D simple
description: Vous guide tout au long du processus de création d’une fenêtre qui restitue le contenu Direct2D.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, didacticiel
- Direct2D, procédure pas à pas
- Direct2D, création d’applications
- Direct2D, applications
- applications pour Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907ec9a026005fec03b034978873f012cd956a8a7533d97b85b9122664ef1163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825336"
---
# <a name="creating-a-simple-direct2d-application"></a>Création d’une application Direct2D simple

Cette rubrique vous guide tout au long du processus de création de la classe DemoApp, qui crée une fenêtre et utilise Direct2D pour dessiner une grille et deux rectangles. Dans ce didacticiel, vous allez apprendre à créer des ressources Direct2D et à dessiner des formes de base. Vous allez également apprendre à structurer votre application afin d’améliorer les performances en minimisant la création des ressources.

pour suivre le didacticiel, vous pouvez utiliser Microsoft Visual Studio 2008 pour créer un projet Win32, puis remplacer le code dans l’en-tête d’application principal et le fichier cpp par le code décrit dans ce didacticiel.

> [!Note]  
> si vous souhaitez créer une application Windows Store qui utilise Direct2D, consultez la rubrique [démarrage rapide de direct2d pour Windows 8](direct2d-quickstart-with-device-context.md) .

 

Pour obtenir une vue d’ensemble des interfaces que vous pouvez utiliser pour créer du contenu Direct2D, consultez [vue d’ensemble de l’API Direct2D](the-direct2d-api.md).

Ce didacticiel contient les éléments suivants :

-   [Partie 1 : créer l’en-tête DemoApp](#part-1-create-the-demoapp-header)
-   [Partie 2 : implémenter l’infrastructure de classe](#part-2-implement-the-class-infrastructure)
-   [Partie 3 : créer des ressources Direct2D](#part-3-create-direct2d-resources)
-   [Partie 4 : afficher le contenu Direct2D](#part-4-render-direct2d-content)
-   [Résumé](#summary)
-   [Rubriques connexes](#related-topics)

Une fois l’opération terminée, la classe DemoApp génère la sortie représentée dans l’illustration suivante.

![illustration de deux rectangles sur un arrière-plan de grille](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>Partie 1 : créer l’en-tête DemoApp

Dans cette étape, vous configurez votre application pour utiliser Direct2D en ajoutant les en-têtes et les macros nécessaires. Vous pouvez également déclarer les méthodes et les membres de données que vous utiliserez dans les parties ultérieures de ce didacticiel.

1.  Dans le fichier d’en-tête de votre application, incluez les en-têtes fréquemment utilisés suivants.
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  Déclarez des fonctions supplémentaires pour libérer des interfaces et des macros afin de gérer les erreurs et de récupérer l’adresse de base du module.
```C++
    template<class Interface>
    inline void SafeRelease(
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
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  Déclarez les méthodes d’initialisation de la classe, de création et d’abandon des ressources, de gestion de la boucle de message, de rendu du contenu et de la procédure Windows.
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  Déclarez des pointeurs pour un objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , un objet [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) et deux objets [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) comme membres de classe.
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>Partie 2 : implémenter l’infrastructure de classe

Dans cette partie, vous allez implémenter le constructeur et le destructeur DemoApp, ses méthodes d’initialisation et de bouclage de message, ainsi que la fonction WinMain. La plupart de ces méthodes sont identiques à celles figurant dans toutes les autres applications Win32. La seule exception est la méthode Initialize, qui appelle la méthode CreateDeviceIndependentResources (que vous définissez dans la partie suivante) qui crée plusieurs ressources Direct2D.

1.  Dans le fichier d’implémentation de classe, implémentez le constructeur de classe et le destructeur. Le constructeur doit initialiser ses membres avec la **valeur null**. Le destructeur doit libérer toutes les interfaces stockées en tant que membres de classe.
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  Implémentez la méthode DemoApp :: RunMessageLoop qui traduit et distribue les messages.
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  Implémentez la méthode Initialize qui crée la fenêtre, l’affiche et appelle la méthode DemoApp :: CreateDeviceIndependentResources. Vous implémentez la méthode CreateDeviceIndependentResources dans la section suivante.
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
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
        }

        return hr;
    }
```

    

4.  Créez la méthode WinMain qui sert de point d’entrée d’application. Initialisez une instance de la classe DemoApp et commencez sa boucle de message.
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
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
```

    

## <a name="part-3-create-direct2d-resources"></a>Partie 3 : créer des ressources Direct2D

Dans cette partie, vous créez les ressources Direct2D que vous utilisez pour dessiner. Direct2D fournit deux types de ressources : les ressources indépendantes du périphérique qui peuvent durer pour la durée de l’application et les ressources dépendantes de l’appareil. Les ressources dépendantes de l’appareil sont associées à un périphérique de rendu particulier et cessent de fonctionner si l’appareil est supprimé.

1.  Implémentez la méthode DemoApp :: CreateDeviceIndependentResources. Dans la méthode, créez un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), une ressource indépendante du périphérique, pour la création d’autres ressources Direct2D. Utilisez le membre de classe **m \_ pDirect2DdFactory** pour stocker la fabrique.
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  Implémentez la méthode DemoApp :: CreateDeviceResources. Cette méthode crée les ressources dépendantes du périphérique de la fenêtre, une cible de rendu et deux pinceaux. Récupérez la taille de la zone cliente et créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) de la même taille que celle qui est restituée dans le **HWND** de la fenêtre. Stockez la cible de rendu dans le membre de la classe **m \_ pRenderTarget** .
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  Utilisez la cible de rendu pour créer un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) en gris et un **ID2D1SolidColorBrush** bleu bleuet.
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  Étant donné que cette méthode sera appelée à plusieurs reprises, ajoutez une instruction if pour vérifier si la cible de rendu (**m \_ pRenderTarget** ) existe déjà. Le code suivant illustre la méthode CreateDeviceResources complète.
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  Implémentez la méthode DemoApp ::D iscardDeviceResources. Dans cette méthode, libérez la cible de rendu et les deux pinceaux que vous avez créés dans la méthode DemoApp :: CreateDeviceResources.
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>Partie 4 : afficher le contenu Direct2D

Dans cette partie, vous allez implémenter la procédure Windows, la méthode OnRender qui peint le contenu et la méthode OnResize qui ajuste la taille de la cible de rendu lorsque la fenêtre est redimensionnée.

1.  Implémentez la méthode DemoApp :: WndProc pour gérer les messages de fenêtre. Pour le message de [**\_ taille WM**](../winmsg/wm-size.md) , appelez la méthode demoApp :: OnResize et transmettez-lui les nouvelles largeur et hauteur. Pour les messages [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) et [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , appelez la méthode demoApp :: OnRender pour peindre la fenêtre. Vous implémentez les méthodes OnRender et OnResize dans les étapes qui suivent.
```C++
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
                reinterpret_cast<LONG_PTR>(pDemoApp)
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
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
                    break;
                }
            }

            if (!wasHandled)
            {
                result = DefWindowProc(hwnd, message, wParam, lParam);
            }
        }

        return result;
    }
    
```

    

2.  Implémentez la méthode DemoApp :: OnRender. Tout d’abord, créez un **HRESULT**. Appelez ensuite la méthode CreateDeviceResource. Cette méthode est appelée chaque fois que la fenêtre est peinte. Rappelez-vous que, à l’étape 4 de la partie 3, vous avez ajouté une instruction **If** pour empêcher la méthode d’effectuer des tâches si la cible de rendu existe déjà.
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  Vérifiez que la méthode CreateDeviceResource a réussi. Si ce n’est pas le cas, n’effectuez aucun dessin.
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  Dans l’instruction **If** que vous venez de créer, commencez le dessin en appelant la méthode BeginDraw de la cible de rendu. Définissez la transformation de la cible de rendu sur la matrice d’identité et effacez la fenêtre.
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  Récupérez la taille de la zone de dessin.
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  Dessinez un arrière-plan de grille à l’aide d’une boucle **for** et de la méthode [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) de la cible de rendu pour dessiner une série de lignes.
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  Créez deux primitives rectangle qui sont centrées sur l’écran.
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  Utilisez la méthode [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) de la cible de rendu pour peindre l’intérieur du premier rectangle avec le pinceau gris.
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  Utilisez la méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) de la cible de rendu pour peindre le contour du deuxième rectangle avec le pinceau bleu bleuet.
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. Appelez la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) de la cible de rendu. La méthode **EndDraw** retourne un **HRESULT** pour indiquer si les opérations de dessin ont réussi. Fermez l’instruction **If** que vous avez commencée à l’étape 3.
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. Vérifiez le **HRESULT** retourné par [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Si elle indique que la cible de rendu doit être recréée, appelez la méthode DemoApp ::D iscardDeviceResources pour la libérer ; elle sera recréée la prochaine fois que la fenêtre recevra un message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) ou [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. Retournez la valeur **HRESULT** et fermez la méthode.
```C++
        return hr;
    }
```

    

13. Implémentez la méthode DemoApp :: OnResize afin qu’elle redimensionne la cible de rendu avec la nouvelle taille de la fenêtre.
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

Vous avez terminé le tutoriel.

> [!Note]  
> Pour utiliser Direct2D, assurez-vous que votre application comprend le fichier d’en-tête d2d1. h et qu’elle est compilée par rapport à la bibliothèque d2d1. lib. vous pouvez trouver d2d1. h et d2d1. lib dans [Windows kit de développement logiciel (SDK) pour Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

 

## <a name="summary"></a>Résumé

Dans ce didacticiel, vous avez appris à créer des ressources Direct2D et à dessiner des formes de base. Vous avez également appris à structurer votre application pour améliorer les performances en minimisant la création des ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de l’API Direct2D](the-direct2d-api.md).
</dt> <dt>

[Amélioration des performances de Direct2D](improving-direct2d-performance.md)
</dt> </dl>

 

 