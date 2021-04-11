---
title: Fonctions de police et de texte (OpenGL)
description: Les fonctions suivantes peuvent être utilisées pour gérer des polices et du texte.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL, fonctions, texte
- WGL, police
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383667"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="591c8-105">Fonctions de police et de texte (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="591c8-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="591c8-106">Les fonctions suivantes peuvent être utilisées pour gérer des polices et du texte.</span><span class="sxs-lookup"><span data-stu-id="591c8-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="591c8-107">Fonction Windows</span><span class="sxs-lookup"><span data-stu-id="591c8-107">Windows Function</span></span>                                 | <span data-ttu-id="591c8-108">Description</span><span class="sxs-lookup"><span data-stu-id="591c8-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="591c8-109">**wglUseFontBitmaps**</span><span class="sxs-lookup"><span data-stu-id="591c8-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="591c8-110">Crée un jeu de listes d’affichage de bitmaps de caractères.</span><span class="sxs-lookup"><span data-stu-id="591c8-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="591c8-111">Les caractères proviennent de la police actuelle d’un contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="591c8-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="591c8-112">Les caractères sont spécifiés en tant qu’exécution consécutive dans le jeu de glyphes de la police.</span><span class="sxs-lookup"><span data-stu-id="591c8-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="591c8-113">**wglUseFontOutlines**</span><span class="sxs-lookup"><span data-stu-id="591c8-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="591c8-114">Crée un ensemble de listes d’affichage, en fonction des glyphes de la police de contour actuellement sélectionnée d’un contexte de périphérique, à utiliser avec le contexte de rendu actuel.</span><span class="sxs-lookup"><span data-stu-id="591c8-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="591c8-115">Les listes d’affichage permettent de dessiner des caractères 3D de polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="591c8-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="591c8-116">Les fonctions **wglUseFontBitmaps** et **wglUseFontOutlines** prennent un handle vers un contexte de périphérique et utilisent la police actuelle de ce contexte de périphérique comme source pour les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="591c8-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="591c8-117">Par conséquent, il est nécessaire de définir la police du contexte de périphérique et les propriétés de la police avant d’appeler **wglUseFontBitmaps** ou **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="591c8-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="591c8-118">Les fonctions [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) et [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) prennent également un paramètre qui transforme le premier glyphe de la police en une liste d’affichage bitmap, et un paramètre qui spécifie le nombre de glyphes à convertir en listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="591c8-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="591c8-119">La fonction crée ensuite des listes d’affichage pour l’exécution consécutive de glyphes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="591c8-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="591c8-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="591c8-120">For example:</span></span>

-   <span data-ttu-id="591c8-121">Pour créer un ensemble de listes d’affichage bitmap 224 pour tous les glyphes de jeu de caractères Windows, définissez ces deux paramètres sur 32 et 224, respectivement.</span><span class="sxs-lookup"><span data-stu-id="591c8-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="591c8-122">Pour créer un ensemble de listes d’affichage bitmap 256 pour tous les glyphes de jeu de caractères OEM, définissez ces deux paramètres sur 0 et 256, respectivement.</span><span class="sxs-lookup"><span data-stu-id="591c8-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="591c8-123">Pour créer une liste d’affichage à bitmap unique pour tout glyphe de jeu de caractères unique, définissez la seconde de ces paramètres sur 1.</span><span class="sxs-lookup"><span data-stu-id="591c8-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="591c8-124">Les fonctions **wglUseFontBitmaps** et **wglUseFontOutlines** représentent un glyphe null dans une police avec une liste d’affichage vide.</span><span class="sxs-lookup"><span data-stu-id="591c8-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="591c8-125">Les listes d’affichage créées par un appel à **wglUseFontBitmaps** ou **wglUseFontOutlines** sont numérotées automatiquement de façon consécutive.</span><span class="sxs-lookup"><span data-stu-id="591c8-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="591c8-126">Après avoir appelé la fonction [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) ou [**WglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , appelez [**glCallLists**](glcalllists.md) pour dessiner une chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="591c8-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="591c8-127">Pour obtenir un exemple de code [, consultez dessin de texte dans une fenêtre Double-Buffered OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) .</span><span class="sxs-lookup"><span data-stu-id="591c8-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="591c8-128">Dans ce contexte, **glCallLists** utilise chaque caractère dans une chaîne en tant qu’index dans le tableau des listes d’affichage numérotées consécutivement créées par **wglUseFontBitmaps** ou **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="591c8-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="591c8-129">Lorsque vous avez terminé de dessiner du texte, appelez la fonction [**glDeleteLists**](gldeletelists.md) pour libérer l’ensemble des listes d’affichage contiguës créées par **wglUseFontBitmaps** et **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="591c8-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 




