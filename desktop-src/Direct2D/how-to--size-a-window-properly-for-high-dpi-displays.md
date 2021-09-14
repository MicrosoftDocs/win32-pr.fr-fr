---
title: Affichage correct sur un affichage haute résolution
description: Décrit les étapes de création d’une fenêtre pour votre application qui s’affiche correctement sur les affichages haute résolution.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd45b4b654556fc251575410cc11f9b66961263
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113165"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a>Affichage correct sur un affichage haute résolution

Bien que Direct2D traite de nombreux problèmes de haute résolution pour vous, vous devez suivre deux étapes pour vous assurer que votre application fonctionne correctement sur les affichages haute résolution :

-   [Étape 1 : utiliser la résolution système en cas de création de Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Étape 2 : déclarer que l’application prend en charge DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Rubriques connexes](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Étape 1 : utiliser la résolution système en cas de création de Windows

L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fournit la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour récupérer la résolution du système. Il fournit les dimensions horizontales et verticales de l’affichage en points par pouce (DPI). Pour utiliser ces valeurs pour définir la largeur d’une fenêtre, utilisez la formule suivante :

<*PPP* >  \* horizontal  < *largeur*, en pixels>/<*PPP horizontal par défaut*>

... où *PPP horizontal* est la valeur récupérée par [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) et la valeur *ppp horizontale par défaut* est 96. La formule est similaire pour la taille verticale :

<*dpi* >  \* vertical  < *hauteur*, en pixels>/<*dpi vertical par défaut*>

... où la valeur *PPP verticale* est la valeur récupérée par la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) et la valeur *ppp verticale par défaut* est 96.

Le code suivant utilise la méthode [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) pour récupérer la valeur PPP du système, puis crée une fenêtre 640 × 480, mise à l’échelle en dpi système.


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
> à partir de Windows 8, vous pouvez utiliser la classe [**Windows :: graphics ::Ds ::D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) pour récupérer la valeur ppp du système.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Étape 2 : déclarer que l’application est DPI-Aware

Quand une application se déclare être prise en charge DPI, il s’agit d’une instruction spécifiant que l’application se comporte correctement aux paramètres ppp jusqu’à 200 ppp. dans Windows Vista et Windows 7, lorsque la virtualisation DPI est activée, les applications qui ne prennent pas en charge dpi sont mises à l’échelle, et les applications reçoivent des données virtualisées à partir des api système, telles que la fonction [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Pour déclarer que votre application prend en charge DPI, procédez comme suit.

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

[Direct2D et haute résolution](direct2d-and-high-dpi.md)
</dt> </dl>

 

 