---
description: Bien que les fonctions présentées dans le précédent fonctionnent bien pour de nombreuses langues, elles peuvent ne pas répondre aux besoins des scripts complexes.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Scripts complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863682"
---
# <a name="complex-scripts"></a><span data-ttu-id="28c77-103">Scripts complexes</span><span class="sxs-lookup"><span data-stu-id="28c77-103">Complex Scripts</span></span>

<span data-ttu-id="28c77-104">Bien que les fonctions présentées dans le précédent fonctionnent bien pour de nombreuses langues, elles peuvent ne pas répondre aux besoins des scripts complexes.</span><span class="sxs-lookup"><span data-stu-id="28c77-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="28c77-105">Les *scripts complexes* sont des langues dont le formulaire imprimé n’est pas rendu de manière simple.</span><span class="sxs-lookup"><span data-stu-id="28c77-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="28c77-106">Par exemple, un script complexe peut permettre un rendu bidirectionnel, une mise en forme contextuelle de glyphes ou une combinaison de caractères.</span><span class="sxs-lookup"><span data-stu-id="28c77-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="28c77-107">En raison de ces exigences spéciales, le contrôle de la sortie de texte doit être très flexible.</span><span class="sxs-lookup"><span data-stu-id="28c77-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="28c77-108">Les fonctions qui affichent du texte [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)et [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) ont été étendues pour prendre en charge des scripts complexes.</span><span class="sxs-lookup"><span data-stu-id="28c77-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="28c77-109">En général, cette prise en charge est transparente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="28c77-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="28c77-110">Toutefois, les applications doivent enregistrer des caractères dans une mémoire tampon et afficher une ligne entière de texte à la fois, afin que les modules de mise en forme de script complexes puissent utiliser le contexte pour réorganiser et générer correctement les glyphes.</span><span class="sxs-lookup"><span data-stu-id="28c77-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="28c77-111">En outre, étant donné que la largeur d’un glyphe peut varier en fonction du contexte, les applications doivent utiliser [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) pour déterminer la longueur de ligne au lieu d’utiliser des largeurs de caractères mises en cache.</span><span class="sxs-lookup"><span data-stu-id="28c77-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="28c77-112">En outre, les applications complexes prenant en charge les scripts doivent envisager l’ajout de la prise en charge de l’ordre de lecture de droite à gauche à leurs applications.</span><span class="sxs-lookup"><span data-stu-id="28c77-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="28c77-113">Vous pouvez basculer l’ordre de lecture ou l’alignement entre gauche et droite avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="28c77-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



<span data-ttu-id="28c77-114">Pour basculer les deux attributs en même temps, exécutez l’instruction suivante, puis appelez [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) et [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), comme indiqué précédemment :</span><span class="sxs-lookup"><span data-stu-id="28c77-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="28c77-115">Vous pouvez également traiter des scripts complexes avec Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="28c77-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="28c77-116">Uniscribe est un ensemble de fonctions qui permettent un degré de contrôle précis des scripts complexes.</span><span class="sxs-lookup"><span data-stu-id="28c77-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="28c77-117">Pour plus d’informations, consultez [Uniscribe](../intl/uniscribe.md) et [traitement de scripts complexes](../intl/processing-complex-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="28c77-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 
