---
title: Comment étiqueter dynamiquement des boutons de barre d’outils
description: Vous pouvez assigner du texte à un bouton existant à l’aide du \_ message to SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104462799"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="9630c-103">Comment étiqueter dynamiquement des boutons de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="9630c-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="9630c-104">Vous pouvez assigner du texte à un bouton existant à l’aide du message [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9630c-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9630c-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="9630c-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9630c-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="9630c-106">Technologies</span></span>

-   [<span data-ttu-id="9630c-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="9630c-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9630c-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="9630c-108">Prerequisites</span></span>

-   <span data-ttu-id="9630c-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="9630c-109">C/C++</span></span>
-   <span data-ttu-id="9630c-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="9630c-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9630c-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="9630c-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="9630c-112">Étiqueter dynamiquement un bouton de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="9630c-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="9630c-113">L’exemple suivant montre comment modifier le texte du troisième bouton dans les exemples précédents de **Save** to **Save As**.</span><span class="sxs-lookup"><span data-stu-id="9630c-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="9630c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9630c-114">Remarks</span></span>

<span data-ttu-id="9630c-115">La modification du texte d’un bouton à l’aide de [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) n’affecte pas la chaîne qui est assignée à ce bouton dans la liste des chaînes internes.</span><span class="sxs-lookup"><span data-stu-id="9630c-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="9630c-116">Si vous ajoutez une chaîne de bouton de barre d’outils à la liste de texte interne, vous ne pouvez pas récupérer l’index de cette chaîne en appelant [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)— vous devez utiliser le message [**to \_ GETBUTTON**](tb-getbutton.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="9630c-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9630c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9630c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9630c-118">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="9630c-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="9630c-119">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9630c-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




