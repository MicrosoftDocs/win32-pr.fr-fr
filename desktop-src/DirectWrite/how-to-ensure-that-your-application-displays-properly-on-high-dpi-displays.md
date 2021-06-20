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
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Comment garantir que votre application s’affiche correctement sur les affichages haute résolution

Bien que [DirectWrite](direct-write-portal.md) résout de nombreux problèmes de haute résolution pour vous, vous devez suivre deux étapes pour vous assurer que votre application fonctionne correctement sur les affichages haute résolution :

-   [Étape 1 : utiliser la résolution système en cas de création de fenêtres](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [GDI](#gdi)
-   [Étape 2 : déclarer que l’application prend en charge DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Rubriques connexes](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Étape 1 : utiliser la résolution système en cas de création de fenêtres

Cette opération peut être effectuée à l’aide de [Direct2D](../direct2d/direct2d-portal.md) ou de [GDI](../gdi/windows-gdi.md).

### <a name="direct2d"></a>Direct2D

L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fournit la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour récupérer la résolution du système. Il fournit les dimensions horizontales et verticales de l’affichage en points par pouce (DPI). Pour utiliser ces valeurs pour définir la largeur d’une fenêtre, utilisez la formule suivante :

<*PPP* >  \* horizontal  < *largeur*, en pixels>/<*PPP horizontal par défaut*>

... où *PPP horizontal* est la valeur récupérée par GetDpi et la valeur *PPP horizontale par défaut* est 96. La formule est similaire pour la taille verticale :

<*dpi* >  \* vertical  < *hauteur*, en pixels>/<*dpi vertical par défaut*>

... où la valeur *PPP verticale* est la valeur récupérée par la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) et la valeur *ppp verticale par défaut* est 96.

Le code suivant utilise la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour créer une fenêtre 640 x 480, mise à l’échelle en dpi système. (Dans le code suivant, *m \_ spD2DFactory* est un pointeur intelligent vers une instance [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .)


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



### <a name="gdi"></a>GDI

[GDI](interoperating-with-gdi.md) fournit la fonction [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) pour la récupération des informations de l’appareil. Vous pouvez récupérer les informations PPP en passant les valeurs d’index *LOGPIXELSX* et *LOGPIXELSY* . La formule permettant de déterminer la taille horizontale et verticale d’une fenêtre est la même que celle de l’exemple [Direct2D](../direct2d/direct2d-portal.md) ci-dessus.

Le code suivant utilise la fonction [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) pour créer une fenêtre 640 x 480, mise à l’échelle vers la résolution système.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Étape 2 : déclarer que l’application est DPI-Aware

Quand une application se déclare être prise en charge DPI, il s’agit d’une instruction spécifiant que l’application se comporte correctement aux paramètres ppp jusqu’à 200 ppp. Dans Windows Vista et Windows 7, lorsque la virtualisation DPI est activée, les applications qui ne prennent pas en charge la résolution sont mises à l’échelle, et les applications reçoivent des données virtualisées à partir des API système, telles que la fonction [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) . Pour déclarer que votre application prend en charge DPI, procédez comme suit.

1.  Créez un fichier appelé DeclareDPIAware. manifest.
2.  Copiez le code XML suivant dans le fichier et enregistrez-le :
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  Dans le fichier. vcproj du projet, ajoutez l’entrée suivante dans chaque élément de configuration sous VisualStudioProject/configurations :
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Direct2D et haute résolution](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 