---
title: Interopérabilité avec GDI
description: DirectWrite fournit un chemin de migration depuis et une certaine interopérabilité avec le modèle de police GDI, ainsi que des interfaces pour le rendu de texte dans une image bitmap qui peut ensuite être dessinée dans une fenêtre.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, interopérabilité GDI
- DirectWrite, interopérabilité
- interopérabilité
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031282"
---
# <a name="interoperating-with-gdi"></a>Interopérabilité avec GDI

[DirectWrite](direct-write-portal.md) fournit un chemin de migration depuis et une certaine interopérabilité avec le modèle de police GDI, ainsi que des interfaces pour le rendu de texte dans une image bitmap qui peut ensuite être dessinée dans une fenêtre.

Cette vue d’ensemble contient les éléments suivants :

-   [Introduction](#introduction)
-   [Partie 1 : IDWriteGdiInterop](#part-1-idwritegdiinterop)
-   [Partie 2 : objets de police](#part-2-font-objects)
-   [Partie 3 : rendu](#part-3-rendering)

## <a name="introduction"></a>Introduction

[DirectWrite](direct-write-portal.md) fournit des méthodes pour la conversion entre la structure LogFont de GDI et les interfaces de police DirectWrite. Cela vous permet d’utiliser GDI pour une partie ou la totalité de l’énumération et de la sélection des polices, tout en tirant parti des fonctionnalités et des performances améliorées de DirectWrite. DirectWrite possède également des interfaces pour le rendu sur une image bitmap si vous souhaitez afficher du texte sur une surface GDI.

## <a name="part-1-idwritegdiinterop"></a>Partie 1 : IDWriteGdiInterop

L’interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) est utilisée pour effectuer une conversion entre les structures de police GDI et les interfaces de police [DirectWrite](direct-write-portal.md) , ainsi que pour créer un objet [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) . Récupérez un objet **IDWriteGdiInterop** à l’aide de la méthode [**IDWriteFactory :: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , comme indiqué dans le code suivant.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Partie 2 : objets de police

GDI utilise la structure LOGFONT pour stocker des informations sur la police et le style de texte. La méthode [**IDWriteGdiInterop :: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) convertit une structure LogFont en objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , comme indiqué dans le code suivant.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



Toutefois, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) n’encapsule pas toutes les mêmes informations qu’un LogFont. Une structure LOGFONT contient la taille de la police, le poids, le style, le soulignement, le barré, le nom du type de police et d’autres informations. Les objets **IDWriteFont** contiennent des informations sur une police, son poids et son style, mais pas la taille de police, le soulignement, etc. Avec [DirectWrite](direct-write-portal.md), les éléments de mise en forme tels que ceux-ci sont encapsulés par un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou, pour des plages de texte spécifiques, un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Vous avez la possibilité de convertir un [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) en LogFont à l’aide de [**IDWriteGdiInterop :: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).

## <a name="part-3-rendering"></a>Partie 3 : rendu

Pour afficher du texte DirectWrite sur une surface GDI, vous utilisez un convertisseur de texte personnalisé. Consultez la rubrique [rendu dans une surface GDI](render-to-a-gdi-surface.md) .

 

 