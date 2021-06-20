---
title: Comment garantir que votre application s’affiche correctement sur les affichages haute résolution (DirectWrite)
description: Décrit comment s’assurer que votre application crée une fenêtre qui s’affiche correctement sur les affichages haute résolution.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406422"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="c4a44-103">Comment garantir que votre application s’affiche correctement sur les affichages haute résolution</span><span class="sxs-lookup"><span data-stu-id="c4a44-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="c4a44-104">Bien que [DirectWrite](direct-write-portal.md) résout de nombreux problèmes de haute résolution pour vous, vous devez suivre deux étapes pour vous assurer que votre application fonctionne correctement sur les affichages haute résolution :</span><span class="sxs-lookup"><span data-stu-id="c4a44-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="c4a44-105">Étape 1 : utiliser la résolution système en cas de création de fenêtres</span><span class="sxs-lookup"><span data-stu-id="c4a44-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="c4a44-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="c4a44-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="c4a44-107">GDI</span><span class="sxs-lookup"><span data-stu-id="c4a44-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="c4a44-108">Étape 2 : déclarer que l’application prend en charge DPI</span><span class="sxs-lookup"><span data-stu-id="c4a44-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="c4a44-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4a44-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="c4a44-110">Étape 1 : utiliser la résolution système en cas de création de fenêtres</span><span class="sxs-lookup"><span data-stu-id="c4a44-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="c4a44-111">Cette opération peut être effectuée à l’aide de [Direct2D](../direct2d/direct2d-portal.md) ou de [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="c4a44-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="c4a44-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="c4a44-112">Direct2D</span></span>

<span data-ttu-id="c4a44-113">L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fournit la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour récupérer la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="c4a44-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="c4a44-114">Il fournit les dimensions horizontales et verticales de l’affichage en points par pouce (DPI).</span><span class="sxs-lookup"><span data-stu-id="c4a44-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="c4a44-115">Pour utiliser ces valeurs pour définir la largeur d’une fenêtre, utilisez la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="c4a44-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="c4a44-116"><*PPP* >  \* horizontal  < *largeur*, en pixels>/<*PPP horizontal par défaut*></span><span class="sxs-lookup"><span data-stu-id="c4a44-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="c4a44-117">... où *PPP horizontal* est la valeur récupérée par GetDpi et la valeur *PPP horizontale par défaut* est 96.</span><span class="sxs-lookup"><span data-stu-id="c4a44-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="c4a44-118">La formule est similaire pour la taille verticale :</span><span class="sxs-lookup"><span data-stu-id="c4a44-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="c4a44-119"><*dpi* >  \* vertical  < *hauteur*, en pixels>/<*dpi vertical par défaut*></span><span class="sxs-lookup"><span data-stu-id="c4a44-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="c4a44-120">... où la valeur *PPP verticale* est la valeur récupérée par la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) et la valeur *ppp verticale par défaut* est 96.</span><span class="sxs-lookup"><span data-stu-id="c4a44-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="c4a44-121">Le code suivant utilise la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour créer une fenêtre 640 x 480, mise à l’échelle en dpi système.</span><span class="sxs-lookup"><span data-stu-id="c4a44-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="c4a44-122">(Dans le code suivant, *m \_ spD2DFactory* est un pointeur intelligent vers une instance [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .)</span><span class="sxs-lookup"><span data-stu-id="c4a44-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


```C++
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
```



### <a name="gdi"></a><span data-ttu-id="c4a44-123">GDI</span><span class="sxs-lookup"><span data-stu-id="c4a44-123">GDI</span></span>

<span data-ttu-id="c4a44-124">[GDI](interoperating-with-gdi.md) fournit la fonction [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) pour la récupération des informations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c4a44-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="c4a44-125">Vous pouvez récupérer les informations PPP en passant les valeurs d’index *LOGPIXELSX* et *LOGPIXELSY* .</span><span class="sxs-lookup"><span data-stu-id="c4a44-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="c4a44-126">La formule permettant de déterminer la taille horizontale et verticale d’une fenêtre est la même que celle de l’exemple [Direct2D](../direct2d/direct2d-portal.md) ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c4a44-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="c4a44-127">Le code suivant utilise la fonction [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) pour créer une fenêtre 640 x 480, mise à l’échelle vers la résolution système.</span><span class="sxs-lookup"><span data-stu-id="c4a44-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="c4a44-128">Étape 2 : déclarer que l’application est DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="c4a44-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="c4a44-129">Quand une application se déclare être prise en charge DPI, il s’agit d’une instruction spécifiant que l’application se comporte correctement aux paramètres ppp jusqu’à 200 ppp.</span><span class="sxs-lookup"><span data-stu-id="c4a44-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="c4a44-130">Dans Windows Vista et Windows 7, lorsque la virtualisation DPI est activée, les applications qui ne prennent pas en charge la résolution sont mises à l’échelle, et les applications reçoivent des données virtualisées à partir des API système, telles que la fonction [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="c4a44-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="c4a44-131">Pour déclarer que votre application prend en charge DPI, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="c4a44-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="c4a44-132">Créez un fichier appelé DeclareDPIAware. manifest.</span><span class="sxs-lookup"><span data-stu-id="c4a44-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="c4a44-133">Copiez le code XML suivant dans le fichier et enregistrez-le :</span><span class="sxs-lookup"><span data-stu-id="c4a44-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="c4a44-134">Dans le fichier. vcproj du projet, ajoutez l’entrée suivante dans chaque élément de configuration sous VisualStudioProject/configurations :</span><span class="sxs-lookup"><span data-stu-id="c4a44-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c4a44-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4a44-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a44-136">Direct2D et haute résolution</span><span class="sxs-lookup"><span data-stu-id="c4a44-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 