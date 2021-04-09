---
title: Présentation de DirectWrite
description: Les personnes communiquent avec le texte tout le temps de leur vie quotidienne.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, à propos de
- DirectWrite, fonctionnalités typographiques
- typographie
- DirectWrite, texte international
- DirectWrite, polices OpenType
- Polices OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, vue d’ensemble de l’API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, rendu de texte
- DirectWrite, modes de rendu
- DirectWrite, interopérabilité GDI
- DirectWrite, interopérabilité
- interopérabilité, DirectWrite
- interopérabilité, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842678"
---
# <a name="introducing-directwrite"></a>Présentation de DirectWrite

Les personnes communiquent avec le texte tout le temps de leur vie quotidienne. C’est le principal moyen pour les utilisateurs de consommer un volume d’informations en plus important. Dans le passé, il était utilisé par le contenu imprimé, principalement des documents, des journaux, des livres, etc. De plus en plus, il s’agit d’un contenu en ligne sur son PC Windows. Un utilisateur Windows classique passe beaucoup de temps à lire à partir de son écran d’ordinateur. Ils peuvent surfer sur le Web, analyser le courrier électronique, rédiger un rapport, remplir une feuille de calcul ou écrire des logiciels, mais ce qu’ils font vraiment, c’est la lecture. Même si le texte et les polices sont performants presque toutes les parties de l’expérience utilisateur dans Windows, pour la plupart des utilisateurs, la lecture sur l’écran n’est pas aussi agréable que la lecture imprimée.

Pour les développeurs d’applications Windows, l’écriture de code de gestion de texte est un défi en raison des exigences accrues pour une meilleure lisibilité, une mise en forme et un contrôle de disposition sophistiqués, ainsi que la prise en charge de plusieurs langues que l’application doit afficher. Même le système de gestion de texte le plus basique doit autoriser la saisie de texte, la mise en page, l’affichage, la modification et la copie et le collage. Les utilisateurs de Windows attendent généralement plus que ces fonctionnalités de base, nécessitant des éditeurs simples pour la prise en charge de plusieurs polices, de divers styles de paragraphes, d’images incorporées, d’une vérification orthographique et d’autres fonctionnalités. La conception d’interface utilisateur moderne n’est pas non plus limitée à un format simple, du texte brut, mais doit présenter une meilleure expérience en matière de polices de texte et de polices riches.

Il s’agit d’une introduction à la façon dont [DirectWrite](direct-write-portal.md) permet aux applications Windows d’améliorer l’expérience de texte pour l’interface utilisateur et les documents.

## <a name="improving-the-text-experience"></a>Amélioration de l’expérience de texte

Les applications Windows modernes ont des exigences sophistiquées pour le texte dans leur interface utilisateur et leurs documents. Celles-ci incluent une meilleure lisibilité, la prise en charge d’une grande variété de langages et de scripts et des performances de rendu supérieures. En outre, la plupart des applications existantes nécessitent un moyen de transférer les investissements existants dans la base de code WindowsWin32.

[DirectWrite](direct-write-portal.md) fournit les trois fonctionnalités suivantes qui permettent aux développeurs d’applications Windows d’améliorer l’expérience de texte dans leurs applications : l’indépendance par rapport au système de rendu, la typographie de haute qualité et plusieurs couches de fonctionnalités.

## <a name="rendering-system-independence"></a>Indépendance Rendering-System

[DirectWrite](direct-write-portal.md) est indépendant de toute technologie graphique particulière. Les applications sont libres d’utiliser la technologie de rendu qui convient le mieux à leurs besoins. Cela permet aux applications de continuer à afficher certaines parties de leur application via GDI et d’autres parties via Direct3D ou [Direct2D](../direct2d/direct2d-portal.md). En fait, une application peut choisir d’afficher DirectWrite via une pile de rendu propriétaire.

## <a name="high-quality-typography"></a>Typographie High-Quality

[DirectWrite](direct-write-portal.md) tire parti des avancées de la technologie de police [OpenType](../intl/opentype-font-format.md) pour permettre une typographie de haute qualité dans une application Windows. Le système de police DirectWrite fournit des services pour gérer l’énumération des polices, la police de substitution et la mise en cache des polices, qui sont toutes nécessaires aux applications pour la gestion des polices.

La prise en charge [OpenType](../intl/opentype-font-format.md) fournie par [DirectWrite](direct-write-portal.md) permet aux développeurs d’ajouter à leurs applications des fonctionnalités typographiques avancées et la prise en charge du texte international.

## <a name="support-for-advanced-typographic-features"></a>Prise en charge des fonctionnalités typographiques avancées

[DirectWrite](direct-write-portal.md) permet aux développeurs d’applications de déverrouiller les fonctionnalités des polices OpenType qu’ils n’ont pas pu utiliser dans WINFORMS ou GDI. L’objet DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) expose un grand nombre des fonctionnalités avancées des polices OpenType, telles que les variantes stylistiques et les paraphes. Le kit de développement logiciel (SDK) Microsoft Windows fournit un ensemble d’exemples de polices [OpenType](../intl/opentype-font-format.md) conçues avec des fonctionnalités riches, telles que les polices Pericles et Pescadero. Pour plus d’informations sur les fonctionnalités OpenType, consultez [caractéristiques des polices OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).

## <a name="support-for-international-text"></a>Prise en charge du texte international

[DirectWrite](direct-write-portal.md) utilise des polices [OpenType](../intl/opentype-font-format.md) pour permettre une prise en charge étendue du texte international. Les fonctionnalités Unicode telles que les substituts, BIDI, saut de ligne et UVS sont prises en charge. L’élément de script guidé dans le langage, la substitution de nombres et la mise en forme de glyphes garantissent que le texte de n’importe quel script possède une disposition et un rendu corrects.

Les scripts suivants sont pris en charge :

> [!Note]  
> Pour les scripts marqués avec un \* , il n’y a pas de polices système par défaut. Les applications doivent installer les polices qui prennent en charge ces scripts.

 

-   Arabe
-   Arménien
-   Bengala
-   Bopomofo
-   Braille\*
-   SYLLABE autochtones canadienne
-   Cherokee
-   Chinois (simplifié & traditionnel)
-   Cyrillique
-   Copte\*
-   Dévanâgarî
-   Éthiopien
-   Géorgien
-   Lettre\*
-   Grec
-   Goudjrati
-   Gurmukhi
-   Hébreu
-   Japonais
-   Kannada
-   Khmer
-   Coréen
-   Lao
-   Latin
-   Malayalam
-   Mongol
-   Myanmar
-   Nouveau taï lü
-   OGAM\*
-   Odia
-   'PHAGS-PA
-   Lettre\*
-   Cingalais
-   Syriaque
-   LETTRE TAÏ le
-   Tamoul
-   Télougou
-   Tana
-   Thaï
-   Tibétain
-   Yi

## <a name="multiple-layers-of-functionality"></a>Plusieurs couches de fonctionnalités

[DirectWrite](direct-write-portal.md) fournit des couches de fonctionnalités pondérées, chaque couche interagissant en toute transparence avec la suivante. La conception d’API offre aux développeurs d’applications la liberté et la flexibilité nécessaires pour adopter des couches individuelles en fonction de leurs besoins et de leur planification. Le diagramme suivant illustre la relation entre ces couches.

![diagramme des couches DirectWrite et de la façon dont elles communiquent avec une application ou une infrastructure d’interface utilisateur et l’API Graphics](images/intro-01.png)

L’API Text Layout fournit les fonctionnalités de niveau le plus élevé disponibles dans [DirectWrite](direct-write-portal.md). Il fournit des services permettant à l’application de mesurer, d’afficher et d’interagir avec des chaînes de texte riches en format. Cette API Text peut être utilisée dans les applications qui utilisent actuellement Win32 DrawText pour générer une interface utilisateur moderne avec du texte riche en format.

Les applications gourmandes en texte qui implémentent leur propre moteur de disposition peuvent utiliser la couche suivante : le processeur de script. Le processeur de script décompose un segment de texte en blocs de script et gère le mappage entre les représentations Unicode et la représentation de glyphe appropriée dans la police afin que le texte du script puisse s’afficher correctement dans la langue appropriée. Le système de disposition utilisé par la couche de l’API Text Layout est basé sur le système de polices et de traitement des scripts.

La couche de rendu de glyphes est la couche de fonctionnalités la plus basse et fournit des fonctionnalités de rendu de glyphes pour les applications qui implémentent leur propre moteur de disposition de texte. La couche de rendu des glyphes est également utile pour les applications qui implémentent un convertisseur personnalisé pour modifier le comportement de dessin de glyphe par le biais de la fonction de rappel dans l’API de mise en forme du texte [DirectWrite](direct-write-portal.md) .

Le système de polices [DirectWrite](direct-write-portal.md) est disponible pour toutes les couches fonctionnelles de DirectWrite et permet à une application d’accéder aux informations sur les polices et les glyphes. Il est conçu pour gérer les technologies de polices et les formats de données courants. Le modèle de police DirectWrite suit la pratique typographique courante qui consiste à prendre en charge un nombre quelconque de poids, de styles et d’étirements dans la même famille de polices. Ce modèle, le même modèle suivi par WPF et CSS, spécifie que les polices qui diffèrent uniquement en poids (gras, clair, etc.), style (vertical, italique ou oblique) ou Stretch (étroit, condensé, large, etc.) sont considérées comme des membres d’une même famille de polices.

### <a name="improved-text-rendering-with-cleartype"></a>Amélioration du rendu du texte avec ClearType

L’amélioration de la lisibilité sur l’écran est une condition essentielle pour toutes les applications Windows. La preuve de la recherche en psychologie cognitive indique que nous devons être en mesure de reconnaître toutes les lettres avec précision et que même l’espacement entre les lettres est essentiel pour un traitement rapide. Les lettres et les mots qui ne sont pas symétriques sont perçus comme insupportable et dégradent l’expérience de lecture. Kevin Larson, Microsoft Advanced Read Technologies Group, a écrit un article sur le sujet qui a été publié dans Spectrum IEEE. L’article est appelé « technologie de texte » ( https://www.spectrum.ieee.org/print/5049) .

Le texte de [DirectWrite](direct-write-portal.md) est rendu à l’aide de Microsoft ClearType, ce qui améliore la clarté et la lisibilité du texte. ClearType tire parti du fait que les écrans LCD modernes affichent des bandes RVB pour chaque pixel pouvant être contrôlé individuellement. DirectWrite utilise les dernières améliorations apportées à ClearType, d’abord inclus avec Windows Vista avec Windows Presentation Foundation, qui lui permet d’évaluer non seulement les lettres individuelles, mais également l’espacement entre les lettres. Avant ces améliorations ClearType, le texte avec une taille de « lecture » de 10 ou 12 points était difficile à afficher : nous pourrions placer 1 pixel entre les lettres, ce qui était souvent trop faible, ou 2 pixels, ce qui était souvent trop grand. L’utilisation de la résolution supplémentaire dans les sous-pixels nous fournit un espacement fractionnaire qui améliore l’uniformité et la symétrie de la page entière.

Les deux illustrations suivantes montrent comment les glyphes peuvent commencer sur n’importe quelle limite de sous-pixel lorsque le positionnement du sous-pixel est utilisé.

L’illustration suivante est rendue à l’aide de la version GDI du convertisseur ClearType, qui n’utilisait pas le positionnement du sous-pixel.

![illustration de la « technologie » rendue sans le positionnement des sous-pixels](images/intro-03.png)

L’illustration suivante est rendue à l’aide de la version [DirectWrite](direct-write-portal.md) du convertisseur ClearType, qui utilise le positionnement de sous-pixel.

![illustration de la « technologie » rendue avec le positionnement des sous-pixels](images/intro-04.png)

Notez que l’espacement entre les lettres h et n est plus pair dans la deuxième image et que la lettre o est plus espacée de la lettre n, plus même avec la lettre l. Notez également que les tiges sur les lettres l sont plus naturelles.

Le positionnement ClearType de sous-pixel offre l’espace de caractères le plus précis à l’écran, en particulier pour les petites tailles où la différence entre un sous-pixel et un pixel entier représente une proportion significative de la largeur de glyphe. Il permet de mesurer le texte dans un espace de résolution idéal et de le rendre à sa position naturelle à l’aide de la bande de couleur de l’écran LCD, avec une granularité de sous-pixel. Le texte mesuré et rendu à l’aide de cette technologie est, par définition, indépendant de la résolution, ce qui signifie que la même disposition du texte est obtenue sur la plage de différentes résolutions d’affichage.

Contrairement à l’un ou l’autre type de rendu ClearType GDI, le ClearType sous-pixel offre la largeur de caractères la plus précise.

L’API de chaîne de texte adopte par défaut le rendu de texte de sous-pixel, ce qui signifie qu’elle mesure le texte à sa résolution idéale indépendamment de la résolution d’affichage actuelle, et produit le résultat de positionnement du glyphe en fonction des largeurs d’avance de glyphe réellement mis à l’échelle et des décalages de positionnement.

Pour le texte de grande taille, [DirectWrite](direct-write-portal.md) permet également l’anticrénelage le long de l’axe y pour rendre les bords plus lisses et rendre les lettres plus lisses comme le concepteur de polices. L’illustration suivante montre l’anticrénelage de direction y.

![illustration de « ClearType » rendue sous forme de texte GDI et de texte DirectWrite avec l’anticrénelage de direction y](images/intro-05.png)

Bien que le texte [DirectWrite](direct-write-portal.md) soit positionné et rendu à l’aide de l’option ClearType sous-pixel par défaut, d’autres options de rendu sont disponibles. De nombreuses applications existantes utilisent GDI pour restituer la plupart de leur interface utilisateur, et certaines applications utilisent des contrôles d’édition du système qui continuent d’utiliser GDI pour le rendu du texte. Lorsque vous ajoutez du texte DirectWrite à ces applications, il peut être nécessaire de sacrifier les améliorations apportées à l’expérience de lecture fournies par la fonction ClearType de sous-pixel afin que le texte ait une apparence cohérente dans l’application.

Pour répondre à ces exigences, [DirectWrite](direct-write-portal.md) prend également en charge les options de rendu suivantes :

-   Sous-pixel ClearType (valeur par défaut).
-   ClearType sous-pixel avec anticrénelage à la fois dans les dimensions horizontales et verticales.
-   Texte avec alias.
-   GDI-largeur naturelle (utilisée par Microsoft Word Mode Lecture, par exemple).
-   Compatible GDI-largeur (y compris l’image bitmap incorporée d’Extrême-Orient).

Chacun de ces modes de rendu peut être affiné par le biais de l’API DirectWrite et du nouveau tuner ClearType de la boîte de réception Windows 7.

> [!Note]  
> À compter de Windows 8, vous devez utiliser l’anticrénelage de texte en nuances de gris dans la plupart des cas. Pour en savoir plus, consultez la section suivante.

 

### <a name="support-for-natural-layout"></a>Prise en charge de la disposition naturelle

La disposition naturelle est indépendante de la résolution, de sorte que l’espacement des caractères ne change pas au fur et à mesure que vous effectuez un zoom avant ou arrière, ou en fonction de la résolution de l’affichage. L’un des avantages secondaires est que l’espacement est vrai pour la conception de la police. La disposition naturelle est rendue possible par la prise en charge de DirectWrite pour le rendu naturel, ce qui signifie que les glyphes individuels peuvent être positionnés sur une fraction d’un pixel.

Bien que la disposition naturelle soit la valeur par défaut, certaines applications doivent restituer du texte avec le même espace et l’même apparence que GDI. Pour ces applications, DirectWrite fournit des modes de mesure naturel GDI et GDI classiques et des modes de rendu correspondants.

L’un des modes de rendu ci-dessus peut être combiné à l’un ou l’autre des deux modes d’anticrénelage : ClearType ou nuances de gris. L’anticrénelage ClearType simule une résolution plus élevée en manipulant individuellement les valeurs de couleur rouge, verte et bleue de chaque pixel. L’anticrénelage de nuances de gris calcule une seule valeur de couverture (ou alpha) pour chaque pixel. ClearType est la valeur par défaut, mais l’anticrénelage en nuances de gris est recommandé pour les applications du Windows Store, car il est plus rapide et compatible avec l’anticrénelage standard, tout en étant très lisible.

## <a name="api-overview"></a>Présentation de l’API

L’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) est le point de départ pour l’utilisation de la fonctionnalité DirectWrite. La fabrique est l’objet racine qui crée un ensemble d’objets qui peuvent être utilisés ensemble.

L’opération de mise en forme et de mise en page est un prérequis pour les opérations, car le texte doit être correctement mis en forme et disposé sur un ensemble de contraintes spécifié avant de pouvoir être dessiné ou testé. Pour ce faire, deux objets clés que vous pouvez créer avec un [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) sont [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). Un objet **IDWriteTextFormat** représente les informations de mise en forme d’un paragraphe de texte. La fonction [**IDWriteFactory :: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) prend la chaîne d’entrée, les contraintes associées telles que la dimension de l’espace à remplir et l’objet **IDWriteTextFormat** , puis place le résultat entièrement analysé et mis en forme dans **IDWriteTextLayout** à utiliser dans les opérations suivantes.

L’application peut ensuite restituer le texte à l’aide de la fonction [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) fournie par [Direct2D](../direct2d/direct2d-portal.md) ou en implémentant une fonction de rappel qui peut utiliser GDI, Direct2D ou d’autres systèmes graphiques pour restituer les glyphes. Dans le cas d’un texte de format unique, la fonction [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) sur Direct2D offre un moyen plus simple de dessiner du texte sans avoir à créer d’abord un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>Mise en forme et dessin de « Hello World » à l’aide de DirectWrite

L’exemple de code suivant montre comment une application peut mettre en forme un seul paragraphe à l’aide de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et la dessiner à l’aide de la fonction [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) de [Direct2D](../direct2d/direct2d-portal.md).


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a>Accès au système de polices

En plus de spécifier un nom de famille de polices pour la chaîne de texte à l’aide de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) dans l’exemple ci-dessus, [DirectWrite](direct-write-portal.md) offre aux applications davantage de contrôle sur la sélection des polices grâce à l’énumération des polices et à la possibilité de créer une collection de polices personnalisée basée sur des polices de document incorporées.

L’objet [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) est une collection de familles de polices. DirectWrite permet d’accéder à l’ensemble de polices installées sur le système par le biais d’une collection de polices spéciale appelée collection de polices système. Cela est obtenu en appelant la méthode [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) de l’objet [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . Une application peut également créer une collection de polices personnalisée à partir d’un ensemble de polices énumérées par un rappel défini par l’application, c’est-à-dire des polices privées installées par une application, ou des polices incorporées dans un document.

L’application peut ensuite appeler [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) pour accéder à un objet FontFamily spécifique dans la collection, puis appeler [**IDWriteFontFamily :: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) pour atteindre un objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) spécifique. L’objet **IDWriteFont** représente une police dans une collection de polices et expose des propriétés et quelques métriques de police de base.

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) est un autre objet qui représente une police et expose un jeu complet de métriques sur une police. Le **IDWriteFontFace** peut être créé directement à partir d’un nom de police ; une application n’a pas besoin d’obtenir une collection de polices pour y accéder. Elle est utile pour une application de disposition de texte telle que Microsoft Word qui doit interroger les détails d’une police spécifique.

Le diagramme suivant illustre la relation entre ces objets.

![diagramme de la relation entre une collection de polices, une famille de polices et un type de police](images/fontcollection.png)

### <a name="idwritefontface"></a>IDWriteFontFace

L’objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) représente une police et fournit des informations plus détaillées sur la police que l’objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) . Les métriques de police et de glyphe du **IDWriteFontFace** sont utiles pour les applications qui implémentent la disposition du texte.

La plupart des applications courantes n’utilisent pas directement ces API et utilisent [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) ou spécifient directement le nom de famille de polices.

Le tableau suivant récapitule les scénarios d’utilisation des deux objets.



| Category                                                                                                         | [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| API pour prendre en charge l’interaction de l’utilisateur, telle qu’une interface utilisateur de sélection de polices : description et autres API d’informations | Oui                                        | Non                                                 |
| API pour la prise en charge du mappage des polices : famille, style, poids, étirement, couverture des caractères                                 | Oui                                        | Non                                                 |
| API DrawText                                                                                                     | Oui                                        | Non                                                 |
| API utilisées pour le rendu                                                                                          | Non                                         | Oui                                                |
| API utilisées pour la disposition du texte : métriques de glyphe, etc.                                                              | Non                                         | Oui                                                |
| API pour le contrôle de l’interface utilisateur et la disposition du texte : métriques à l’ensemble des polices                                                           | Oui                                        | Oui                                                |



 

Voici un exemple d’application qui énumère les polices de la collection de polices système.


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a>Rendu du texte

Les API de rendu de texte permettent le rendu des glyphes dans une police [DirectWrite](direct-write-portal.md) sur une surface [Direct2D](../direct2d/direct2d-portal.md) ou une image bitmap indépendante du périphérique GDI, ou à convertir en plans ou bitmaps. Le rendu ClearType dans DirectWrite prend en charge le positionnement des sous-pixels avec une netteté et un contraste améliorés par rapport aux implémentations précédentes sur Windows. DirectWrite prend également en charge le texte noir et blanc avec alias pour prendre en charge les scénarios impliquant des polices d’Extrême-Orient avec des bitmaps incorporées, ou lorsque l’utilisateur a désactivé le lissage des polices de n’importe quel type.

Toutes les options sont réglables par tous les boutons ClearType disponibles accessibles par le biais des API [DirectWrite](direct-write-portal.md) , ainsi que par l’intermédiaire de la nouvelle applet du panneau de configuration du tuner ClearType Windows 7.

Deux API sont disponibles pour le rendu des glyphes : l’un fournissant un rendu accéléré par le matériel via [Direct2D](../direct2d/direct2d-portal.md) et l’autre fournissant un rendu logiciel à une image bitmap GDI. Une application utilisant [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) et l’implémentation du rappel [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) peuvent appeler l’une de ces fonctions en réponse à un rappel [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) . En outre, les applications qui implémentent leur propre disposition ou gèrent les données de niveau glyphe peuvent utiliser ces API.

1.  [**ID2DRenderTarget ::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    Les applications peuvent utiliser l’API [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) pour fournir une accélération matérielle pour le rendu de texte à l’aide du GPU. L’accélération matérielle affecte toutes les phases du pipeline de rendu de texte, de la fusion des glyphes aux exécutions de glyphes et du filtrage de la bitmap d’exécution de glyphes, à l’application de l’algorithme de fusion ClearType à la sortie affichée finale. Il s’agit de l’API recommandée pour obtenir les meilleures performances de rendu.

2.  [**IDWriteBitmapRenderTarget ::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    Les applications peuvent utiliser la méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour effectuer un rendu logiciel d’une série de glyphes dans une image bitmap 32-BPP. L’objet [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsule une image bitmap et un contexte de périphérique de mémoire qui peut être utilisé pour le rendu des glyphes. Cette API est utile si vous souhaitez rester avec GDI, car vous disposez d’une base de code existante qui s’affiche dans GDI.

Si vous disposez d’une application qui possède un code de disposition de texte qui utilise GDI et que vous souhaitez conserver son code de disposition existant mais utiliser [DirectWrite](direct-write-portal.md) uniquement pour l’étape finale du rendu des glyphes, [**IDWriteGdiInterop :: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) fournit le pont entre les deux API. Avant d’appeler cette fonction, l’application utilise la fonction **IDWriteGdiInterop :: CreateFontFaceFromHdc** pour obtenir une référence de type font-face d’un contexte de périphérique (Device Context).

> [!Note]  
> Pour la plupart des scénarios, les applications n’ont peut-être pas besoin d’utiliser ces API de rendu de glyphe. Une fois qu’une application a créé un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , elle peut utiliser la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) pour restituer le texte.

 

## <a name="custom-rendering-modes"></a>Modes de rendu personnalisés

Un certain nombre de paramètres affectent le rendu du texte, tels que gamma, le niveau ClearType, la géométrie des pixels et le contraste amélioré. Les paramètres de rendu sont encapsulés par un objet, qui implémente l’interface [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) publique. L’objet de paramètres de rendu est initialisé automatiquement en fonction des propriétés matérielles et/ou des préférences de l’utilisateur spécifiées par le biais de l’applet du panneau de configuration ClearType dans Windows 7. En règle générale, si un client utilise l’API de disposition [DirectWrite](direct-write-portal.md) , DirectWrite sélectionne automatiquement un mode de rendu qui correspond au mode de mesure spécifié.

Les applications qui souhaitent davantage de contrôle peuvent utiliser [**IDWriteFactory :: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) pour implémenter les différentes options de rendu. Cette fonction peut également être utilisée pour définir la valeur gamma, la géométrie des pixels et le contraste amélioré.

Voici les différentes options de rendu disponibles :

-   Anticrénelage de sous-pixel

    L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ naturel pour spécifier le rendu avec anticrénelage dans la dimension horizontale uniquement.

-   Anticrénelage de sous-pixel dans les dimensions horizontales et verticales.

    L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ Natural \_ symétrique pour spécifier le rendu avec anticrénelage à la fois dans les dimensions horizontales et verticales. Cela rend les courbes et les lignes diagonales plus lisses au détriment d’une certaine douceur, et est généralement utilisée à des tailles supérieures à 16 ppem.

-   Texte avec alias

    L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE avec un \_ \_ alias pour spécifier un alias de texte.

-   Texte en nuances de gris

    L’application définit le paramètre *pixelGeometry* sur DWRITE \_ pixel \_ Geometry \_ Flat pour spécifier un texte en nuances de gris.

-   Compatible GDI-largeur (y compris l’image bitmap incorporée d’Extrême-Orient)

    L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ GDI Classic pour spécifier l’anticrénelage de \_ largeur compatible GDI.

-   GDI-largeur naturelle

    L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ GDI \_ Natural pour spécifier l’anticrénelage compatible GDI en largeur naturelle.

-   Texte du plan

    Pour un rendu de grande taille, un développeur d’applications peut préférer le rendu à l’aide de la structure de police plutôt que de la pixellisation dans une bitmap. L’application définit le paramètre *renderingMode* sur **\_ \_ \_ plan du mode de rendu DWRITE** pour spécifier que le rendu doit contourner le rastériseur et utiliser directement les contours.

## <a name="gdi-interoperability"></a>Interopérabilité GDI

L’interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) fournit une interopérabilité avec GDI. Cela permet aux applications de poursuivre leurs investissements existants dans les bases de code GDI et d’utiliser de manière sélective [DirectWrite](direct-write-portal.md) pour le rendu ou la mise en page.

Voici les API qui permettent à une application de migrer vers ou à partir du système de polices GDI :

-   [**CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    Crée un objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) qui correspond aux propriétés spécifiées par la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

-   [**ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    Initialise une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basée sur les propriétés compatibles GDI du [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)spécifié.

-   [**ConvertFontFaceToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    Initialise une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basée sur les propriétés compatibles GDI du [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)spécifié.

-   [**CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    Crée un objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) qui correspond au **Hfont** actuellement sélectionné.

## <a name="conclusion"></a>Conclusion

L’amélioration de l’expérience de lecture est très intéressante pour les utilisateurs, qu’ils soient sur l’écran ou sur papier. [DirectWrite](direct-write-portal.md) offre la facilité d’utilisation et le modèle de programmation en couches pour les développeurs d’applications afin d’améliorer l’expérience de texte pour leurs applications Windows. Les applications peuvent utiliser DirectWrite pour restituer un texte riche en format pour leur interface utilisateur et leurs documents avec l’API Layout. Pour les scénarios plus complexes, une application peut fonctionner directement avec des glyphes, accéder aux polices, etc. et exploiter la puissance de DirectWrite pour fournir une typographie de haute qualité.

Les fonctionnalités d’interopérabilité de [DirectWrite](direct-write-portal.md) permettent aux développeurs d’applications de transférer leurs codes base Win32 existants et d’adopter DirectWrite de manière sélective au sein de leurs applications.

 

 