---
description: Dans le texte unidirectionnel, la position du signe insertion n’a aucune ambiguïté, car le bord de tête d’un caractère se trouve au même endroit que le bord de fin du caractère précédent.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Affichage du signe insertion dans les chaînes bidirectionnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528311"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="04430-103">Affichage du signe insertion dans les chaînes bidirectionnelles</span><span class="sxs-lookup"><span data-stu-id="04430-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="04430-104">Dans le texte unidirectionnel, la position du signe insertion n’a aucune ambiguïté, car le bord de tête d’un caractère se trouve au même endroit que le bord de fin du caractère précédent.</span><span class="sxs-lookup"><span data-stu-id="04430-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="04430-105">Toutefois, dans le texte bidirectionnel, la position du signe insertion entre les exécutions de la direction opposée est ambiguë.</span><span class="sxs-lookup"><span data-stu-id="04430-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="04430-106">Par exemple, dans le paragraphe de gauche à droite « hellosalaam », la dernière lettre de « Hello » précède immédiatement la première lettre de « Salaam ».</span><span class="sxs-lookup"><span data-stu-id="04430-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="04430-107">La meilleure position pour afficher le signe insertion varie selon qu’il est considéré comme suivi du « o » de « Hello » ou qu’il doit précéder le « s » de « Salaam ».</span><span class="sxs-lookup"><span data-stu-id="04430-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="04430-108">Uniscribe utilise les conventions de positionnement du signe insertion indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="04430-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="04430-109">Situation</span><span class="sxs-lookup"><span data-stu-id="04430-109">Situation</span></span>       | <span data-ttu-id="04430-110">Positionnement du signe insertion visuel</span><span class="sxs-lookup"><span data-stu-id="04430-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="04430-111">Saisie</span><span class="sxs-lookup"><span data-stu-id="04430-111">Typing</span></span>          | <span data-ttu-id="04430-112">Bord de fin du dernier caractère tapé.</span><span class="sxs-lookup"><span data-stu-id="04430-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="04430-113">Collage</span><span class="sxs-lookup"><span data-stu-id="04430-113">Pasting</span></span>         | <span data-ttu-id="04430-114">Bord de fin du dernier caractère collé.</span><span class="sxs-lookup"><span data-stu-id="04430-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="04430-115">Avancer le signe insertion</span><span class="sxs-lookup"><span data-stu-id="04430-115">Caret advancing</span></span> | <span data-ttu-id="04430-116">Bord de fin du dernier caractère passé.</span><span class="sxs-lookup"><span data-stu-id="04430-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="04430-117">Retrait du signe insertion</span><span class="sxs-lookup"><span data-stu-id="04430-117">Caret retiring</span></span>  | <span data-ttu-id="04430-118">Bord de tête du dernier caractère passé.</span><span class="sxs-lookup"><span data-stu-id="04430-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="04430-119">Accueil</span><span class="sxs-lookup"><span data-stu-id="04430-119">Home</span></span>            | <span data-ttu-id="04430-120">Bord de tête de la ligne.</span><span class="sxs-lookup"><span data-stu-id="04430-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="04430-121">End</span><span class="sxs-lookup"><span data-stu-id="04430-121">End</span></span>             | <span data-ttu-id="04430-122">Bord de fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="04430-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="04430-123">Le signe insertion peut être positionné comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="04430-123">The caret can be positioned as shown in the following example:</span></span>


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



<span data-ttu-id="04430-124">Le positionnement du signe insertion peut être plus simple, comme indiqué ci-dessous, en fonction d’une valeur *fAdvancing* limitée à **true** ou **false**:</span><span class="sxs-lookup"><span data-stu-id="04430-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="04430-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) gère logiquement les positions hors limites.</span><span class="sxs-lookup"><span data-stu-id="04430-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="04430-126">Elle retourne le bord de tête de la série pour *iCharPos* <0, et le bord de fin de la série pour *iCharPos* >= length.</span><span class="sxs-lookup"><span data-stu-id="04430-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="04430-127">Pour plus d’informations, consultez [gestion du placement du signe insertion et test de positionnement](managing-caret-placement-and-hit-testing.md) .</span><span class="sxs-lookup"><span data-stu-id="04430-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="04430-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04430-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04430-129">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="04430-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



