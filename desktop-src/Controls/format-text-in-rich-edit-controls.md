---
title: Comment mettre en forme du texte dans les contrôles RichEdit
description: Une application peut envoyer des messages à un contrôle Rich Edit afin de mettre en forme des caractères et des paragraphes et de récupérer des informations de mise en forme.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724286"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="1d70c-103">Comment mettre en forme du texte dans les contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="1d70c-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="1d70c-104">Une application peut envoyer des messages à un contrôle Rich Edit afin de mettre en forme des caractères et des paragraphes et de récupérer des informations de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="1d70c-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="1d70c-105">Les attributs de mise en forme des paragraphes incluent l’alignement, les tabulations, les retraits, la numérotation et les tables simples.</span><span class="sxs-lookup"><span data-stu-id="1d70c-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="1d70c-106">Pour les caractères, vous pouvez spécifier le nom de la police, la taille, la couleur et les effets tels que gras, italique et protégé.</span><span class="sxs-lookup"><span data-stu-id="1d70c-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1d70c-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="1d70c-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1d70c-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="1d70c-108">Technologies</span></span>

-   [<span data-ttu-id="1d70c-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="1d70c-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1d70c-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="1d70c-110">Prerequisites</span></span>

-   <span data-ttu-id="1d70c-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="1d70c-111">C/C++</span></span>
-   <span data-ttu-id="1d70c-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="1d70c-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1d70c-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="1d70c-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="1d70c-114">Mettre en forme du texte dans un contrôle RichEdit</span><span class="sxs-lookup"><span data-stu-id="1d70c-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="1d70c-115">Vous pouvez appliquer la mise en forme des paragraphes à l’aide du message [**em \_ SETPARAFORMAT**](em-setparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="1d70c-116">Pour déterminer la mise en forme de paragraphe actuelle pour le texte sélectionné, utilisez le message [**em \_ GETPARAFORMAT**](em-getparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="1d70c-117">La structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) ou [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) est utilisée avec les deux messages pour spécifier les attributs de mise en forme des paragraphes.</span><span class="sxs-lookup"><span data-stu-id="1d70c-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="1d70c-118">Vous pouvez appliquer la mise en forme des caractères à l’aide du message [**em \_ SETCHARFORMAT**](em-setcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="1d70c-119">Pour déterminer la mise en forme de caractères actuelle pour le texte sélectionné, vous pouvez utiliser le message [**em \_ GETCHARFORMAT**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="1d70c-120">La structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) ou [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) est utilisée avec les deux messages pour spécifier des attributs de caractères.</span><span class="sxs-lookup"><span data-stu-id="1d70c-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="1d70c-121">Vous pouvez également utiliser des messages [**em \_ SETCHARFORMAT**](em-setcharformat.md) et [**em \_ GETCHARFORMAT**](em-getcharformat.md) pour définir et récupérer la mise en forme des caractères du point d’insertion, qui est la mise en forme appliquée à tous les caractères insérés par la suite.</span><span class="sxs-lookup"><span data-stu-id="1d70c-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="1d70c-122">Par exemple, si une application définit la mise en forme de caractère par défaut sur gras et que l’utilisateur tape ensuite un caractère, ce caractère est gras.</span><span class="sxs-lookup"><span data-stu-id="1d70c-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="1d70c-123">La mise en forme des caractères du point d’insertion est appliquée au texte nouvellement inséré uniquement si la sélection actuelle est vide (si la sélection actuelle est un point d’insertion).</span><span class="sxs-lookup"><span data-stu-id="1d70c-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="1d70c-124">Dans le cas contraire, le nouveau texte prend la mise en forme des caractères du texte qu’il remplace.</span><span class="sxs-lookup"><span data-stu-id="1d70c-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="1d70c-125">Si la sélection change, la mise en forme des caractères par défaut change pour correspondre au premier caractère de la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="1d70c-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="1d70c-126">L’effet de caractère protégé est unique en ce qu’il ne modifie pas l’apparence du texte.</span><span class="sxs-lookup"><span data-stu-id="1d70c-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="1d70c-127">Si l’utilisateur tente de modifier du texte protégé, un contrôle RichEdit envoie à sa fenêtre parente un code de notification en [ \_ protection](en-protected.md) , ce qui permet à la fenêtre parente d’autoriser ou d’empêcher la modification.</span><span class="sxs-lookup"><span data-stu-id="1d70c-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="1d70c-128">Pour recevoir ce code de notification, vous devez l’activer à l’aide du message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="1d70c-129">La couleur de premier plan est toujours un attribut de caractère.</span><span class="sxs-lookup"><span data-stu-id="1d70c-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="1d70c-130">Dans Microsoft Rich Edit 1,0, la couleur d’arrière-plan n’est qu’une propriété du contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1d70c-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="1d70c-131">Pour définir la couleur d’arrière-plan par défaut, utilisez le message [**em \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="1d70c-132">Notez que Rich Edit ne prend pas en charge le message [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="1d70c-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d70c-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d70c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d70c-134">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="1d70c-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="1d70c-135">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1d70c-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




