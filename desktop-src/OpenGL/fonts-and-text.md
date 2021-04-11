---
title: Polices et texte (OpenGL)
description: L’implémentation de OpenGL par Microsoft dans Windows prend en charge les graphiques GDI dans une fenêtre OpenGL à mémoire tampon unique.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL sur Windows, polices
- OpenGL sur Windows, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383664"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="fbfad-105">Polices et texte (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="fbfad-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="fbfad-106">L’implémentation de OpenGL par Microsoft dans Windows prend en charge les graphiques GDI dans une fenêtre OpenGL à mémoire tampon unique.</span><span class="sxs-lookup"><span data-stu-id="fbfad-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="fbfad-107">Elle ne prend pas en charge les graphiques GDI dans une fenêtre OpenGL à double mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fbfad-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="fbfad-108">Par conséquent, vous pouvez appeler uniquement les fonctions de texte et de police GDI standard pour dessiner du texte dans une fenêtre OpenGL à une seule mise en mémoire tampon ; vous ne pouvez pas appeler ces fonctions pour dessiner du texte dans une fenêtre OpenGL à deux mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="fbfad-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="fbfad-109">Il existe une solution de contournement pour cette restriction sur du texte dans les fenêtres à deux mémoires tampons : créez des listes d’affichage OpenGL pour les images bitmap de caractères, puis exécutez ces listes d’affichage pour dessiner des caractères.</span><span class="sxs-lookup"><span data-stu-id="fbfad-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="fbfad-110">Ce processus comporte trois étapes principales :</span><span class="sxs-lookup"><span data-stu-id="fbfad-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="fbfad-111">Sélectionnez une police pour un contexte de périphérique, en définissant les propriétés de la police comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="fbfad-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="fbfad-112">Créer un ensemble de listes d’affichage bitmap en fonction des glyphes dans la police du contexte de périphérique, une liste d’affichage pour chaque glyphe que l’application dessinera.</span><span class="sxs-lookup"><span data-stu-id="fbfad-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="fbfad-113">Dessinez chaque glyphe dans une chaîne, à l’aide de ces listes d’affichage bitmap.</span><span class="sxs-lookup"><span data-stu-id="fbfad-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="fbfad-114">Pour créer les listes d’affichage, appelez les fonctions [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) et [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) .</span><span class="sxs-lookup"><span data-stu-id="fbfad-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="fbfad-115">Pour dessiner des caractères dans une chaîne à l’aide de ces listes d’affichage, appelez [**glCallLists**](glcalllists.md).</span><span class="sxs-lookup"><span data-stu-id="fbfad-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="fbfad-116">Pour créer des applications faciles à localiser et utilisant des ressources avec parcimonie, la création et le stockage de ces listes d’affichage d’image de glyphe doivent être gérés avec précaution.</span><span class="sxs-lookup"><span data-stu-id="fbfad-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="fbfad-117">De nombreux langages, contrairement à l’anglais, possèdent des alphabets dont les codes de caractères sont compris dans un ensemble de valeurs relativement volumineux.</span><span class="sxs-lookup"><span data-stu-id="fbfad-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbfad-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fbfad-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbfad-119">Fonctions de police et de texte</span><span class="sxs-lookup"><span data-stu-id="fbfad-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 




