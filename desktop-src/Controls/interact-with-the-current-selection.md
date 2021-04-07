---
title: Comment interagir avec la sélection actuelle
description: L’utilisateur peut sélectionner du texte dans un contrôle RichEdit à l’aide de la souris ou du clavier.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724279"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="df4a5-103">Comment interagir avec la sélection actuelle</span><span class="sxs-lookup"><span data-stu-id="df4a5-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="df4a5-104">L’utilisateur peut sélectionner du texte dans un contrôle RichEdit à l’aide de la souris ou du clavier.</span><span class="sxs-lookup"><span data-stu-id="df4a5-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="df4a5-105">La *sélection actuelle* correspond à la plage de caractères sélectionnés ou à la position du point d’insertion si aucun caractère n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="df4a5-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="df4a5-106">Une application peut obtenir des informations sur la sélection actuelle, la définir, déterminer quand elle change et afficher ou masquer la mise en surbrillance de la sélection.</span><span class="sxs-lookup"><span data-stu-id="df4a5-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="df4a5-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="df4a5-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="df4a5-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="df4a5-108">Technologies</span></span>

-   [<span data-ttu-id="df4a5-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="df4a5-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="df4a5-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="df4a5-110">Prerequisites</span></span>

-   <span data-ttu-id="df4a5-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="df4a5-111">C/C++</span></span>
-   <span data-ttu-id="df4a5-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="df4a5-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="df4a5-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="df4a5-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="df4a5-114">Interagir avec la sélection actuelle</span><span class="sxs-lookup"><span data-stu-id="df4a5-114">Interact with the Current Selection</span></span>

<span data-ttu-id="df4a5-115">Pour déterminer la sélection actuelle dans un contrôle RichEdit, utilisez le message [**em \_ EXGETSEL**](em-exgetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="df4a5-116">Pour définir la sélection actuelle, utilisez le message [**em \_ EXSETSEL**](em-exsetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="df4a5-117">La structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) est utilisée avec les deux messages et spécifie une plage de caractères.</span><span class="sxs-lookup"><span data-stu-id="df4a5-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="df4a5-118">Pour récupérer des informations sur le contenu de la sélection actuelle, vous pouvez utiliser le message [**em \_ SELECTIONTYPE**](em-selectiontype.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="df4a5-119">Une application peut détecter à quel moment la sélection actuelle change en traitant le code de notification en [ \_ selChange](en-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="df4a5-120">Le code de notification spécifie une structure [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) qui contient des informations sur la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="df4a5-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="df4a5-121">Un contrôle RichEdit envoie ce code de notification uniquement si vous l’activez à l’aide du message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="df4a5-122">Par défaut, un contrôle RichEdit affiche et masque la mise en surbrillance de la sélection quand elle gagne et perd le focus.</span><span class="sxs-lookup"><span data-stu-id="df4a5-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="df4a5-123">Vous pouvez afficher ou masquer la sélection à tout moment en utilisant le message [**em \_ HIDESELECTION**](em-hideselection.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="df4a5-124">Par exemple, une application peut fournir une boîte de dialogue de recherche pour rechercher du texte dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="df4a5-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="df4a5-125">L’application peut sélectionner du texte correspondant sans fermer la boîte de dialogue. dans ce cas, elle doit utiliser le message de **em \_ HIDESELECTION** pour mettre en surbrillance la sélection.</span><span class="sxs-lookup"><span data-stu-id="df4a5-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="df4a5-126">Comme avec les contrôles d’édition, vous pouvez spécifier le style de fenêtre [**es \_ NOHIDESEL**](edit-control-styles.md) pour empêcher un contrôle RichEdit de masquer la mise en surbrillance de la sélection lorsqu’elle perd le focus.</span><span class="sxs-lookup"><span data-stu-id="df4a5-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="df4a5-127">En guise d’alternative à l’utilisation des messages [**em \_ EXGETSEL**](em-exgetsel.md) et [**em \_ EXSETSEL**](em-exsetsel.md) , vous pouvez récupérer et définir la sélection actuelle à l’aide des messages de contrôle d’édition em [**\_ GETSEL**](em-getsel.md) et [**em \_ SETSEL**](em-setsel.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="df4a5-128">Le **\_ GETSEL** message packs de caractères 2 16 bits indexe dans sa valeur de retour de 32 bits et, par conséquent, fonctionne uniquement pour les sélections qui se trouvent entièrement dans le premier 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="df4a5-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="df4a5-129">Toutefois, un contrôle RichEdit ne contiendra jamais plus de 32 Ko de texte, sauf si vous étendez cette limite à l’aide du message [**em \_ LIMITTEXT**](em-limittext.md) ou [**em \_ EXLIMITTEXT**](em-exlimittext.md) .</span><span class="sxs-lookup"><span data-stu-id="df4a5-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="df4a5-130">Pour les sélections qui s’étendent au-delà du premier 64 Ko de texte, le message **em \_ GETSEL** retourne-1.</span><span class="sxs-lookup"><span data-stu-id="df4a5-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="df4a5-131">Dans ce cas, vous pouvez toujours utiliser les valeurs retournées dans *wParam* et *lParam* pour rechercher les caractères de début et de fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="df4a5-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df4a5-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df4a5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df4a5-133">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="df4a5-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="df4a5-134">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="df4a5-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




