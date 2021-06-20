---
title: Affichage correct sur un affichage haute résolution
description: Décrit les étapes de création d’une fenêtre pour votre application qui s’affiche correctement sur les affichages haute résolution.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd45b4b654556fc251575410cc11f9b66961263
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406152"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="26792-103">Affichage correct sur un affichage haute résolution</span><span class="sxs-lookup"><span data-stu-id="26792-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="26792-104">Bien que Direct2D traite de nombreux problèmes de haute résolution pour vous, vous devez suivre deux étapes pour vous assurer que votre application fonctionne correctement sur les affichages haute résolution :</span><span class="sxs-lookup"><span data-stu-id="26792-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="26792-105">Étape 1 : utiliser la résolution système en cas de création de fenêtres</span><span class="sxs-lookup"><span data-stu-id="26792-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="26792-106">Étape 2 : déclarer que l’application prend en charge DPI</span><span class="sxs-lookup"><span data-stu-id="26792-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="26792-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26792-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="26792-108">Étape 1 : utiliser la résolution système en cas de création de fenêtres</span><span class="sxs-lookup"><span data-stu-id="26792-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="26792-109">L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fournit la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour récupérer la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="26792-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="26792-110">Il fournit les dimensions horizontales et verticales de l’affichage en points par pouce (DPI).</span><span class="sxs-lookup"><span data-stu-id="26792-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="26792-111">Pour utiliser ces valeurs pour définir la largeur d’une fenêtre, utilisez la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="26792-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="26792-112"><*PPP* >  \* horizontal  < *largeur*, en pixels>/<*PPP horizontal par défaut*></span><span class="sxs-lookup"><span data-stu-id="26792-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="26792-113">... où *PPP horizontal* est la valeur récupérée par [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) et la valeur *ppp horizontale par défaut* est 96.</span><span class="sxs-lookup"><span data-stu-id="26792-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="26792-114">La formule est similaire pour la taille verticale :</span><span class="sxs-lookup"><span data-stu-id="26792-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="26792-115"><*dpi* >  \* vertical  < *hauteur*, en pixels>/<*dpi vertical par défaut*></span><span class="sxs-lookup"><span data-stu-id="26792-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="26792-116">... où la valeur *PPP verticale* est la valeur récupérée par la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) et la valeur *ppp verticale par défaut* est 96.</span><span class="sxs-lookup"><span data-stu-id="26792-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="26792-117">Le code suivant utilise la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour récupérer la valeur PPP du système, puis crée une fenêtre 640 × 480, mise à l’échelle en dpi système.</span><span class="sxs-lookup"><span data-stu-id="26792-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


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



> [!Note]
>
> <span data-ttu-id="26792-118">À compter de Windows 8, vous pouvez utiliser la classe [**Windows :: Graphics ::D affichage ::D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) pour connaître la valeur PPP du système.</span><span class="sxs-lookup"><span data-stu-id="26792-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="26792-119">Étape 2 : déclarer que l’application est DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="26792-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="26792-120">Quand une application se déclare être prise en charge DPI, il s’agit d’une instruction spécifiant que l’application se comporte correctement aux paramètres ppp jusqu’à 200 ppp.</span><span class="sxs-lookup"><span data-stu-id="26792-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="26792-121">Dans Windows Vista et Windows 7, lorsque la virtualisation DPI est activée, les applications qui ne prennent pas en charge la résolution sont mises à l’échelle, et les applications reçoivent des données virtualisées à partir des API système, telles que la fonction [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="26792-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="26792-122">Pour déclarer que votre application prend en charge DPI, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="26792-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="26792-123">Créez un fichier appelé DeclareDPIAware. manifest.</span><span class="sxs-lookup"><span data-stu-id="26792-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="26792-124">Copiez le code XML suivant dans le fichier et enregistrez-le :</span><span class="sxs-lookup"><span data-stu-id="26792-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="26792-125">Dans le fichier. vcproj du projet, ajoutez l’entrée suivante dans chaque élément de configuration sous VisualStudioProject/configurations :</span><span class="sxs-lookup"><span data-stu-id="26792-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="26792-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26792-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26792-127">Direct2D et haute résolution</span><span class="sxs-lookup"><span data-stu-id="26792-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 