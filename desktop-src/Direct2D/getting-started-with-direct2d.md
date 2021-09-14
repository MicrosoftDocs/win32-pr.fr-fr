---
title: Démarrage rapide de Direct2D
description: Résume les étapes requises pour dessiner avec Direct2D et fournit un exemple de code.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, exemple de code de rectangle de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113202"
---
# <a name="direct2d-quickstart"></a>Démarrage rapide de Direct2D

Direct2D est une API en mode immédiat et en code natif pour la création de graphiques 2D. Cette rubrique montre comment utiliser Direct2D dans une application Win32 classique pour dessiner sur un **HWND**.

> [!Note]  
> si vous souhaitez créer une application Windows Store qui utilise Direct2D, consultez la rubrique [démarrage rapide de direct2d pour Windows 8](direct2d-quickstart-with-device-context.md) .

 

Cette rubrique contient les sections suivantes :

-   [Dessin d’un rectangle simple](#drawing-a-simple-rectangle)
-   [Étape 1 : inclure l’en-tête Direct2D](#step-1-include-direct2d-header)
-   [Étape 2 : créer un ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Étape 3 : créer un ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Étape 4 : créer un pinceau](#step-4-create-a-brush)
-   [Étape 5 : dessiner le rectangle](#step-5-draw-the-rectangle)
-   [Étape 6 : libérer des ressources](#step-6-release-resources)
-   [Créer une application Direct2D simple](#create-a-simple-direct2d-application)
-   [Rubriques connexes](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Dessin d’un rectangle simple

Pour dessiner un rectangle à l’aide de [GDI](/windows/desktop/gdi/windows-gdi), vous pouvez gérer le message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , comme indiqué dans le code suivant.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



Le code permettant de dessiner le même rectangle avec Direct2D est similaire : il crée des ressources de dessin, décrit une forme à dessiner, dessine la forme, puis libère les ressources de dessin. Les sections qui suivent décrivent chacune de ces étapes en détail.

## <a name="step-1-include-direct2d-header"></a>Étape 1 : inclure l’en-tête Direct2D

En plus des en-têtes requis pour une application Win32, incluez l’en-tête d2d1. h.

## <a name="step-2-create-an-id2d1factory"></a>Étape 2 : créer un ID2D1Factory

L’un des premiers éléments d’un exemple Direct2D est la création d’un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) est le point de départ pour l’utilisation de Direct2D ; Utilisez un **ID2D1Factory** pour créer des ressources Direct2D.

Lorsque vous créez une fabrique, vous pouvez spécifier s’il s’agit d’un thread multiple ou d’un thread unique. (Pour plus d’informations sur les fabriques multithread, consultez les notes sur la [**page de référence ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Cet exemple crée une fabrique à thread unique.

En général, votre application doit créer la fabrique une seule fois et la conserver pendant toute la durée de vie de l’application.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Étape 3 : créer un ID2D1HwndRenderTarget

Une fois que vous avez créé une fabrique, utilisez-la pour créer une cible de rendu.


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



Une cible de rendu est un appareil qui peut effectuer des opérations de dessin et créer des ressources de dessin dépendantes de l’appareil, telles que des pinceaux. Les différents types de cibles de rendu sont rendus sur différents appareils. L’exemple précédent utilise un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), qui s’affiche sur une partie de l’écran.

Lorsque cela est possible, une cible de rendu utilise le GPU pour accélérer les opérations de rendu et créer des ressources de dessin. Dans le cas contraire, la cible de rendu utilise le processeur pour traiter les instructions de rendu et créer des ressources. (Vous pouvez modifier ce comportement en utilisant les indicateurs de [**\_ type de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) quand vous créez la cible de rendu.)

La méthode [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) accepte trois paramètres. Le premier paramètre, un struct de [**\_ Propriétés de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , spécifie les options d’affichage à distance, s’il faut forcer la cible de rendu à être rendue sur un logiciel ou un matériel, et la résolution PPP. Le code de cet exemple utilise la fonction d’assistance [**d2d1 :: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) pour accepter les propriétés de la cible de rendu par défaut.

Le deuxième paramètre, une structure de [**Propriétés de \_ \_ \_ cible \_ de rendu HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , spécifie le **HWND** vers lequel le contenu est restitué, la taille initiale de la cible de rendu (en pixels) et ses [**options de présentation**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options). Cet exemple utilise la fonction d’assistance [**d2d1 :: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) pour spécifier un HWND et une taille initiale. Il utilise les options de présentation par défaut.

Le troisième paramètre est l’adresse du pointeur qui reçoit la référence de la cible de rendu.

Lorsque vous créez une cible de rendu et que l’accélération matérielle est disponible, vous allouez des ressources sur le GPU de l’ordinateur. En créant une cible de rendu une fois et en la conservant le plus longtemps possible, vous obtenez des avantages en matière de performances. Votre application doit créer des cibles de rendu une seule fois pour la durée de vie de l’application ou jusqu’à la réception de l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) . Lorsque vous recevez cette erreur, vous devez recréer la cible de rendu (et toutes les ressources qu’elle a créées).

## <a name="step-4-create-a-brush"></a>Étape 4 : créer un pinceau

À l’instar d’une fabrique, une cible de rendu peut créer des ressources de dessin. Dans cet exemple, la cible de rendu crée un pinceau.


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



Un pinceau est un objet qui peint une zone, telle que le trait d’une forme ou le remplissage d’une géométrie. Dans cet exemple, le pinceau peint une zone avec une couleur unie prédéfinie, noire.

Direct2D fournit également d’autres types de pinceaux : les pinceaux de dégradé pour peindre des dégradés linéaires et radiaux, et un pinceau bitmap pour peindre avec des bitmaps et des modèles.

Certaines API de dessin fournissent des stylets pour dessiner des contours et des pinceaux pour remplir des formes. Direct2D est différent : il ne fournit pas d’objet Pen, mais utilise un pinceau pour dessiner des contours et des formes de remplissage. Lors du dessin de contours, utilisez l’interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) avec un pinceau pour contrôler les opérations de traçage de chemin.

Un pinceau peut uniquement être utilisé avec la cible de rendu qui l’a créé et avec d’autres cibles de rendu dans le même domaine de ressource. En général, vous devez créer des pinceaux une seule fois et les conserver pendant toute la durée de vie de la cible de rendu qui les a créés. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) est l’exception solitaire ; étant donné qu’il est relativement peu coûteux à créer, vous pouvez créer un **ID2D1SolidColorBrush** chaque fois que vous dessinez un cadre, sans toucher aux performances perceptibles. Vous pouvez également utiliser une seule **ID2D1SolidColorBrush** et modifier simplement sa couleur à chaque fois que vous l’utilisez.

## <a name="step-5-draw-the-rectangle"></a>Étape 5 : dessiner le rectangle

Ensuite, utilisez la cible de rendu pour dessiner le rectangle.


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



La méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accepte deux paramètres : le rectangle à dessiner et le pinceau à utiliser pour peindre le contour du rectangle. Si vous le souhaitez, vous pouvez également spécifier les options largeur du trait, motif des tirets, jointure de ligne et extrémité de fin.

Vous devez appeler la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) avant d’émettre des commandes de dessin, et vous devez appeler la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) une fois que vous avez terminé d’émettre des commandes de dessin. La méthode **EndDraw** retourne un **HRESULT** qui indique si les commandes de dessin ont réussi.

## <a name="step-6-release-resources"></a>Étape 6 : libérer des ressources

Lorsqu’il n’y a plus de frames à dessiner ou lorsque vous recevez l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) , libérez la cible de rendu et les appareils qu’elle a créés.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Lorsque votre application a terminé d’utiliser des ressources Direct2D (par exemple, quand elle est sur le point de quitter), libérez la fabrique Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Créer une application Direct2D simple

Le code de cette rubrique montre les éléments de base d’une application Direct2D. Par souci de concision, la rubrique omet l’infrastructure d’application et le code de gestion des erreurs qui est caractéristique d’une application bien écrite. Pour une procédure pas à pas détaillée qui montre le code complet pour la création d’une application Direct2D simple et présente les meilleures pratiques de conception, consultez [création d’une application Direct2d simple](direct2d-quickstart.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une application Direct2D simple](direct2d-quickstart.md)
</dt> </dl>

 

 