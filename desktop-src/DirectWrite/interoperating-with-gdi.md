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
# <a name="interoperating-with-gdi"></a><span data-ttu-id="37ed7-108">Interopérabilité avec GDI</span><span class="sxs-lookup"><span data-stu-id="37ed7-108">Interoperating with GDI</span></span>

<span data-ttu-id="37ed7-109">[DirectWrite](direct-write-portal.md) fournit un chemin de migration depuis et une certaine interopérabilité avec le modèle de police GDI, ainsi que des interfaces pour le rendu de texte dans une image bitmap qui peut ensuite être dessinée dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="37ed7-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="37ed7-110">Cette vue d’ensemble contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="37ed7-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="37ed7-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="37ed7-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="37ed7-112">Partie 1 : IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="37ed7-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="37ed7-113">Partie 2 : objets de police</span><span class="sxs-lookup"><span data-stu-id="37ed7-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="37ed7-114">Partie 3 : rendu</span><span class="sxs-lookup"><span data-stu-id="37ed7-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="37ed7-115">Introduction</span><span class="sxs-lookup"><span data-stu-id="37ed7-115">Introduction</span></span>

<span data-ttu-id="37ed7-116">[DirectWrite](direct-write-portal.md) fournit des méthodes pour la conversion entre la structure LogFont de GDI et les interfaces de police DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="37ed7-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="37ed7-117">Cela vous permet d’utiliser GDI pour une partie ou la totalité de l’énumération et de la sélection des polices, tout en tirant parti des fonctionnalités et des performances améliorées de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="37ed7-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="37ed7-118">DirectWrite possède également des interfaces pour le rendu sur une image bitmap si vous souhaitez afficher du texte sur une surface GDI.</span><span class="sxs-lookup"><span data-stu-id="37ed7-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="37ed7-119">Partie 1 : IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="37ed7-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="37ed7-120">L’interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) est utilisée pour effectuer une conversion entre les structures de police GDI et les interfaces de police [DirectWrite](direct-write-portal.md) , ainsi que pour créer un objet [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="37ed7-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="37ed7-121">Récupérez un objet **IDWriteGdiInterop** à l’aide de la méthode [**IDWriteFactory :: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="37ed7-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="37ed7-122">Partie 2 : objets de police</span><span class="sxs-lookup"><span data-stu-id="37ed7-122">Part 2: Font Objects</span></span>

<span data-ttu-id="37ed7-123">GDI utilise la structure LOGFONT pour stocker des informations sur la police et le style de texte.</span><span class="sxs-lookup"><span data-stu-id="37ed7-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="37ed7-124">La méthode [**IDWriteGdiInterop :: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) convertit une structure LogFont en objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="37ed7-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="37ed7-125">Toutefois, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) n’encapsule pas toutes les mêmes informations qu’un LogFont.</span><span class="sxs-lookup"><span data-stu-id="37ed7-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="37ed7-126">Une structure LOGFONT contient la taille de la police, le poids, le style, le soulignement, le barré, le nom du type de police et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="37ed7-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="37ed7-127">Les objets **IDWriteFont** contiennent des informations sur une police, son poids et son style, mais pas la taille de police, le soulignement, etc.</span><span class="sxs-lookup"><span data-stu-id="37ed7-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="37ed7-128">Avec [DirectWrite](direct-write-portal.md), les éléments de mise en forme tels que ceux-ci sont encapsulés par un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou, pour des plages de texte spécifiques, un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="37ed7-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="37ed7-129">Vous avez la possibilité de convertir un [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) en LogFont à l’aide de [**IDWriteGdiInterop :: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span><span class="sxs-lookup"><span data-stu-id="37ed7-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="37ed7-130">Partie 3 : rendu</span><span class="sxs-lookup"><span data-stu-id="37ed7-130">Part 3: Rendering</span></span>

<span data-ttu-id="37ed7-131">Pour afficher du texte DirectWrite sur une surface GDI, vous utilisez un convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="37ed7-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="37ed7-132">Consultez la rubrique [rendu dans une surface GDI](render-to-a-gdi-surface.md) .</span><span class="sxs-lookup"><span data-stu-id="37ed7-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 