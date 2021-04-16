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
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104558571"
---
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="566b4-108">Création d’une application Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="566b4-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="566b4-109">Cette rubrique vous guide tout au long du processus de création de la classe DemoApp, qui crée une fenêtre et utilise Direct2D pour dessiner une grille et deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="566b4-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="566b4-110">Dans ce didacticiel, vous allez apprendre à créer des ressources Direct2D et à dessiner des formes de base.</span><span class="sxs-lookup"><span data-stu-id="566b4-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="566b4-111">Vous allez également apprendre à structurer votre application afin d’améliorer les performances en minimisant la création des ressources.</span><span class="sxs-lookup"><span data-stu-id="566b4-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="566b4-112">Pour suivre le didacticiel, vous pouvez utiliser Microsoft Visual Studio 2008 pour créer un projet Win32, puis remplacer le code dans l’en-tête d’application principal et le fichier CPP par le code décrit dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="566b4-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="566b4-113">Si vous souhaitez créer une application du Windows Store qui utilise Direct2D, consultez la rubrique [Direct2d QuickStart pour Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="566b4-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="566b4-114">Pour obtenir une vue d’ensemble des interfaces que vous pouvez utiliser pour créer du contenu Direct2D, consultez [vue d’ensemble de l’API Direct2D](the-direct2d-api.md).</span><span class="sxs-lookup"><span data-stu-id="566b4-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="566b4-115">Ce didacticiel contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="566b4-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="566b4-116">Partie 1 : créer l’en-tête DemoApp</span><span class="sxs-lookup"><span data-stu-id="566b4-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="566b4-117">Partie 2 : implémenter l’infrastructure de classe</span><span class="sxs-lookup"><span data-stu-id="566b4-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="566b4-118">Partie 3 : créer des ressources Direct2D</span><span class="sxs-lookup"><span data-stu-id="566b4-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="566b4-119">Partie 4 : afficher le contenu Direct2D</span><span class="sxs-lookup"><span data-stu-id="566b4-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="566b4-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="566b4-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="566b4-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="566b4-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="566b4-122">Une fois l’opération terminée, la classe DemoApp génère la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="566b4-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![illustration de deux rectangles sur un arrière-plan de grille](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="566b4-124">Partie 1 : créer l’en-tête DemoApp</span><span class="sxs-lookup"><span data-stu-id="566b4-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="566b4-125">Dans cette étape, vous configurez votre application pour utiliser Direct2D en ajoutant les en-têtes et les macros nécessaires.</span><span class="sxs-lookup"><span data-stu-id="566b4-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="566b4-126">Vous pouvez également déclarer les méthodes et les membres de données que vous utiliserez dans les parties ultérieures de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="566b4-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="566b4-127">Dans le fichier d’en-tête de votre application, incluez les en-têtes fréquemment utilisés suivants.</span><span class="sxs-lookup"><span data-stu-id="566b4-127">In your application header file, include the following frequently used headers.</span></span>
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

    

2.  <span data-ttu-id="566b4-128">Déclarez des fonctions supplémentaires pour libérer des interfaces et des macros afin de gérer les erreurs et de récupérer l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="566b4-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
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

    

3.  <span data-ttu-id="566b4-129">Déclarez les méthodes d’initialisation de la classe, de création et d’abandon des ressources, de gestion de la boucle de message, de rendu du contenu et de la procédure Windows.</span><span class="sxs-lookup"><span data-stu-id="566b4-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
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



    

4.  <span data-ttu-id="566b4-130">Déclarez des pointeurs pour un objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , un objet [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) et deux objets [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) comme membres de classe.</span><span class="sxs-lookup"><span data-stu-id="566b4-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="566b4-131">Partie 2 : implémenter l’infrastructure de classe</span><span class="sxs-lookup"><span data-stu-id="566b4-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="566b4-132">Dans cette partie, vous allez implémenter le constructeur et le destructeur DemoApp, ses méthodes d’initialisation et de bouclage de message, ainsi que la fonction WinMain.</span><span class="sxs-lookup"><span data-stu-id="566b4-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="566b4-133">La plupart de ces méthodes sont identiques à celles figurant dans toutes les autres applications Win32.</span><span class="sxs-lookup"><span data-stu-id="566b4-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="566b4-134">La seule exception est la méthode Initialize, qui appelle la méthode CreateDeviceIndependentResources (que vous définissez dans la partie suivante) qui crée plusieurs ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="566b4-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="566b4-135">Dans le fichier d’implémentation de classe, implémentez le constructeur de classe et le destructeur.</span><span class="sxs-lookup"><span data-stu-id="566b4-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="566b4-136">Le constructeur doit initialiser ses membres avec la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="566b4-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="566b4-137">Le destructeur doit libérer toutes les interfaces stockées en tant que membres de classe.</span><span class="sxs-lookup"><span data-stu-id="566b4-137">The destructor should release any interfaces stored as class members.</span></span>
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



    

2.  <span data-ttu-id="566b4-138">Implémentez la méthode DemoApp :: RunMessageLoop qui traduit et distribue les messages.</span><span class="sxs-lookup"><span data-stu-id="566b4-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
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

    

3.  <span data-ttu-id="566b4-139">Implémentez la méthode Initialize qui crée la fenêtre, l’affiche et appelle la méthode DemoApp :: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="566b4-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="566b4-140">Vous implémentez la méthode CreateDeviceIndependentResources dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="566b4-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
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

    

4.  <span data-ttu-id="566b4-141">Créez la méthode WinMain qui sert de point d’entrée d’application.</span><span class="sxs-lookup"><span data-stu-id="566b4-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="566b4-142">Initialisez une instance de la classe DemoApp et commencez sa boucle de message.</span><span class="sxs-lookup"><span data-stu-id="566b4-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
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

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="566b4-143">Partie 3 : créer des ressources Direct2D</span><span class="sxs-lookup"><span data-stu-id="566b4-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="566b4-144">Dans cette partie, vous créez les ressources Direct2D que vous utilisez pour dessiner.</span><span class="sxs-lookup"><span data-stu-id="566b4-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="566b4-145">Direct2D fournit deux types de ressources : les ressources indépendantes du périphérique qui peuvent durer pour la durée de l’application et les ressources dépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="566b4-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="566b4-146">Les ressources dépendantes de l’appareil sont associées à un périphérique de rendu particulier et cessent de fonctionner si l’appareil est supprimé.</span><span class="sxs-lookup"><span data-stu-id="566b4-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="566b4-147">Implémentez la méthode DemoApp :: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="566b4-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="566b4-148">Dans la méthode, créez un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), une ressource indépendante du périphérique, pour la création d’autres ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="566b4-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="566b4-149">Utilisez le membre de classe **m \_ pDirect2DdFactory** pour stocker la fabrique.</span><span class="sxs-lookup"><span data-stu-id="566b4-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="566b4-150">Implémentez la méthode DemoApp :: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="566b4-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="566b4-151">Cette méthode crée les ressources dépendantes du périphérique de la fenêtre, une cible de rendu et deux pinceaux.</span><span class="sxs-lookup"><span data-stu-id="566b4-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="566b4-152">Récupérez la taille de la zone cliente et créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) de la même taille que celle qui est restituée dans le **HWND** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="566b4-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="566b4-153">Stockez la cible de rendu dans le membre de la classe **m \_ pRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="566b4-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
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

    

3.  <span data-ttu-id="566b4-154">Utilisez la cible de rendu pour créer un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) en gris et un **ID2D1SolidColorBrush** bleu bleuet.</span><span class="sxs-lookup"><span data-stu-id="566b4-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
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

    

4.  <span data-ttu-id="566b4-155">Étant donné que cette méthode sera appelée à plusieurs reprises, ajoutez une instruction if pour vérifier si la cible de rendu (**m \_ pRenderTarget** ) existe déjà.</span><span class="sxs-lookup"><span data-stu-id="566b4-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="566b4-156">Le code suivant illustre la méthode CreateDeviceResources complète.</span><span class="sxs-lookup"><span data-stu-id="566b4-156">The following code shows the complete CreateDeviceResources method.</span></span>
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

    

5.  <span data-ttu-id="566b4-157">Implémentez la méthode DemoApp ::D iscardDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="566b4-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="566b4-158">Dans cette méthode, libérez la cible de rendu et les deux pinceaux que vous avez créés dans la méthode DemoApp :: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="566b4-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="566b4-159">Partie 4 : afficher le contenu Direct2D</span><span class="sxs-lookup"><span data-stu-id="566b4-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="566b4-160">Dans cette partie, vous allez implémenter la procédure Windows, la méthode OnRender qui peint le contenu et la méthode OnResize qui ajuste la taille de la cible de rendu lorsque la fenêtre est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="566b4-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="566b4-161">Implémentez la méthode DemoApp :: WndProc pour gérer les messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="566b4-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="566b4-162">Pour le message de [**\_ taille WM**](../winmsg/wm-size.md) , appelez la méthode demoApp :: OnResize et transmettez-lui les nouvelles largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="566b4-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="566b4-163">Pour les messages [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) et [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , appelez la méthode demoApp :: OnRender pour peindre la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="566b4-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="566b4-164">Vous implémentez les méthodes OnRender et OnResize dans les étapes qui suivent.</span><span class="sxs-lookup"><span data-stu-id="566b4-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
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

    

2.  <span data-ttu-id="566b4-165">Implémentez la méthode DemoApp :: OnRender.</span><span class="sxs-lookup"><span data-stu-id="566b4-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="566b4-166">Tout d’abord, créez un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="566b4-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="566b4-167">Appelez ensuite la méthode CreateDeviceResource.</span><span class="sxs-lookup"><span data-stu-id="566b4-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="566b4-168">Cette méthode est appelée chaque fois que la fenêtre est peinte.</span><span class="sxs-lookup"><span data-stu-id="566b4-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="566b4-169">Rappelez-vous que, à l’étape 4 de la partie 3, vous avez ajouté une instruction **If** pour empêcher la méthode d’effectuer des tâches si la cible de rendu existe déjà.</span><span class="sxs-lookup"><span data-stu-id="566b4-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="566b4-170">Vérifiez que la méthode CreateDeviceResource a réussi.</span><span class="sxs-lookup"><span data-stu-id="566b4-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="566b4-171">Si ce n’est pas le cas, n’effectuez aucun dessin.</span><span class="sxs-lookup"><span data-stu-id="566b4-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="566b4-172">Dans l’instruction **If** que vous venez de créer, commencez le dessin en appelant la méthode BeginDraw de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="566b4-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="566b4-173">Définissez la transformation de la cible de rendu sur la matrice d’identité et effacez la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="566b4-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="566b4-174">Récupérez la taille de la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="566b4-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="566b4-175">Dessinez un arrière-plan de grille à l’aide d’une boucle **for** et de la méthode [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) de la cible de rendu pour dessiner une série de lignes.</span><span class="sxs-lookup"><span data-stu-id="566b4-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
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

    

7.  <span data-ttu-id="566b4-176">Créez deux primitives rectangle qui sont centrées sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="566b4-176">Create two rectangle primitives that are centered on the screen.</span></span>
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

    

8.  <span data-ttu-id="566b4-177">Utilisez la méthode [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) de la cible de rendu pour peindre l’intérieur du premier rectangle avec le pinceau gris.</span><span class="sxs-lookup"><span data-stu-id="566b4-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="566b4-178">Utilisez la méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) de la cible de rendu pour peindre le contour du deuxième rectangle avec le pinceau bleu bleuet.</span><span class="sxs-lookup"><span data-stu-id="566b4-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="566b4-179">Appelez la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="566b4-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="566b4-180">La méthode **EndDraw** retourne un **HRESULT** pour indiquer si les opérations de dessin ont réussi.</span><span class="sxs-lookup"><span data-stu-id="566b4-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="566b4-181">Fermez l’instruction **If** que vous avez commencée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="566b4-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="566b4-182">Vérifiez le **HRESULT** retourné par [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="566b4-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="566b4-183">Si elle indique que la cible de rendu doit être recréée, appelez la méthode DemoApp ::D iscardDeviceResources pour la libérer ; elle sera recréée la prochaine fois que la fenêtre recevra un message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) ou [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="566b4-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="566b4-184">Retournez la valeur **HRESULT** et fermez la méthode.</span><span class="sxs-lookup"><span data-stu-id="566b4-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="566b4-185">Implémentez la méthode DemoApp :: OnResize afin qu’elle redimensionne la cible de rendu avec la nouvelle taille de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="566b4-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
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

    

<span data-ttu-id="566b4-186">Vous avez terminé le tutoriel.</span><span class="sxs-lookup"><span data-stu-id="566b4-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="566b4-187">Pour utiliser Direct2D, assurez-vous que votre application comprend le fichier d’en-tête d2d1. h et qu’elle est compilée par rapport à la bibliothèque d2d1. lib.</span><span class="sxs-lookup"><span data-stu-id="566b4-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="566b4-188">Vous pouvez trouver d2d1. h et d2d1. lib dans le [Kit de développement logiciel (SDK) Windows pour Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="566b4-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="566b4-189">Résumé</span><span class="sxs-lookup"><span data-stu-id="566b4-189">Summary</span></span>

<span data-ttu-id="566b4-190">Dans ce didacticiel, vous avez appris à créer des ressources Direct2D et à dessiner des formes de base.</span><span class="sxs-lookup"><span data-stu-id="566b4-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="566b4-191">Vous avez également appris à structurer votre application pour améliorer les performances en minimisant la création des ressources.</span><span class="sxs-lookup"><span data-stu-id="566b4-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="566b4-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="566b4-192">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="566b4-193">[Vue d’ensemble de l’API Direct2D](the-direct2d-api.md).</span><span class="sxs-lookup"><span data-stu-id="566b4-193">[Direct2D API Overview](the-direct2d-api.md)</span></span>
</dt> <dt>

[<span data-ttu-id="566b4-194">Amélioration des performances de Direct2D</span><span class="sxs-lookup"><span data-stu-id="566b4-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 