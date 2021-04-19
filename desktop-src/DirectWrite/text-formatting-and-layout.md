---
title: Mise en forme et disposition du texte
description: DirectWrite fournit deux interfaces pour mettre en forme le texte IDWriteTextFormat et IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, mise en forme du texte
- DirectWrite, disposition
- DirectWrite, interface IDWriteTextFormat
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextFormat
- Interface IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380753"
---
# <a name="text-formatting-and-layout"></a>Mise en forme et disposition du texte

[DirectWrite](direct-write-portal.md) fournit deux interfaces pour la mise en forme du texte : [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextFormat** décrit uniquement le format du texte et est utilisé dans les cas où une chaîne entière doit avoir la même taille de police, le même style, le même poids, et ainsi de suite. En revanche, **IDWriteTextLayout** encapsule une chaîne de texte et la mise en forme des plages spécifiées de la chaîne. Ce document décrit chaque interface et leurs utilisations. Pour plus d’informations sur la création et les méthodes de ces interfaces, consultez les pages de référence [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Ce document contient les éléments suivants :

-   [IDWriteTextFormat](#modifying-an-idwritetextformat)
    -   [Modification d’un IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [IDWriteTextLayout](#idwritetextlayout)
    -   [Mise en forme d’une plage de texte](#formatting-a-range-of-text)
    -   [Options de rendu](#rendering-options)

## <a name="idwritetextformat"></a>IDWriteTextFormat

Un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) est utilisé pour :

-   Décrit le format d’une chaîne entière lors du rendu. Pour restituer une chaîne avec plusieurs formats, utilisez un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
-   Spécifiez le format de texte par défaut lors de la création d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Pour créer un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , utilisez la méthode [**IDWriteFactory :: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) et spécifiez la famille de polices, la collection de polices, l’épaisseur de police, la taille de police (DIP), le nom des paramètres régionaux.

### <a name="modifying-an-idwritetextformat"></a>Modification d’un IDWriteTextFormat

Une fois qu’une interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) est créée, certaines valeurs ne peuvent pas être modifiées : la famille de polices, la collection, le poids et la taille, ainsi que le nom des paramètres régionaux. Pour modifier ces valeurs, vous devez créer un nouvel objet **IDWriteTextFormat** .

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vous permet de modifier les propriétés ci-dessus sans avoir à recréer quoi que ce soit. [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) vous permet d’apporter des modifications de format qui s’appliquent à l’intégralité du texte, par exemple l’alignement du texte. Si vous souhaitez appliquer une mise en forme à des plages de caractères spécifiques, vous devez le faire à l’aide d’un **IDWriteTextLayout**.

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fournit des méthodes permettant de définir l’alignement du texte, le sens du déroulement, le taquet de tabulation incrémentiel, l’interligne, l’alignement des paragraphes, le rognage et le retour automatique à la ligne. Ces propriétés peuvent être modifiées à tout moment après la création de l’objet **IDWriteTextFormat** .

## <a name="idwritetextlayout"></a>IDWriteTextLayout

L’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , contrairement à [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), représente à la fois un bloc de texte et la mise en forme associée. **IDWriteTextFormat** représente les informations de mise en forme initiales. L’exemple suivant montre comment créer un objet **IDWriteTextLayout** à l’aide de [**IDWriteFactory :: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



Le texte d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ne peut pas être modifié une fois que l’objet est créé. Pour modifier le texte, vous devez supprimer l’objet existant et créer un nouvel objet **IDWriteTextLayout** .

Vous pouvez utiliser un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pour mettre en forme des plages de texte spécifiées. **IDWriteTextLayout** fournit également des méthodes pour modifier le style et le poids de la police, et ajoute des fonctionnalités de police OpenType et un test de positionnement. Pour plus d’informations et pour obtenir la liste complète des méthodes, consultez la page de référence [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

### <a name="formatting-a-range-of-text"></a>Mise en forme d’une plage de texte

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fournit plusieurs méthodes pour mettre en forme des plages de texte. Chacune de ces méthodes prend une structure de [**\_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) comme paramètre pour spécifier la position du texte de départ dans la chaîne et la longueur de la plage à mettre en forme. L’exemple suivant montre comment affecter la valeur gras à l’épaisseur de la police d’une plage de texte.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Options de rendu

Le texte avec une mise en forme décrite par un seul objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) peut être rendu avec [Direct2D](../direct2d/direct2d-portal.md), toutefois, il existe quelques options supplémentaires pour le rendu d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

La chaîne décrite par un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) peut être rendue à l’aide des méthodes ci-dessous.

1.  [Rendu à l’aide de Direct2D](rendering-by-using-direct2d.md).
2.  [Rendu à l’aide d’un convertisseur de texte personnalisé](how-to-implement-a-custom-text-renderer.md).
3.  [Rendre sur une surface GDI](render-to-a-gdi-surface.md).

 

 
