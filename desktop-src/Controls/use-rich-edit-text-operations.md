---
title: Utilisation des opérations de modification de texte enrichi
description: Une application peut envoyer des messages pour récupérer ou Rechercher du texte dans un contrôle RichEdit. Vous pouvez récupérer le texte sélectionné ou une plage de texte spécifiée.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941412"
---
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="bdb0f-104">Utilisation des opérations de modification de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="bdb0f-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="bdb0f-105">Une application peut envoyer des messages pour récupérer ou Rechercher du texte dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="bdb0f-106">Vous pouvez récupérer le texte sélectionné ou une plage de texte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="bdb0f-107">Pour obtenir le texte sélectionné dans un contrôle Rich Edit, utilisez le message [**em \_ GETSELTEXT**](em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="bdb0f-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="bdb0f-108">Le texte est copié dans le tableau de caractères spécifié.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="bdb0f-109">Vous devez vous assurer que le tableau est suffisamment grand pour contenir le texte sélectionné, plus un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="bdb0f-110">Pour récupérer une plage de texte spécifiée, utilisez le message [**em \_ GETTEXTRANGE**](em-gettextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="bdb0f-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="bdb0f-111">La structure [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) utilisée avec ce message spécifie la plage de texte à récupérer et pointe vers un tableau de caractères qui reçoit le texte.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="bdb0f-112">Là encore, l’application doit s’assurer que le tableau est suffisamment grand pour le texte spécifié, plus un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="bdb0f-113">Vous pouvez rechercher une chaîne dans un contrôle Rich Edit à l’aide des [**messages \_ em TexteCherché**](em-findtext.md) ou [**em \_ FINDTEXTEX**](em-findtextex.md) , ou de leurs équivalents Unicode, [**em \_ FINDTEXTW**](em-findtextw.md) et [**em \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="bdb0f-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="bdb0f-114">La structure [**TexteCherché**](/windows/win32/api/richedit/ns-richedit-findtexta) utilisée avec les versions non étendues spécifie la plage de texte à rechercher et la chaîne à rechercher.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="bdb0f-115">Les versions étendues utilisent une structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , qui spécifie les mêmes informations et reçoit également les points de début et de fin de la plage de caractères du texte trouvé.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="bdb0f-116">Vous pouvez également spécifier des options comme si la recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bdb0f-117">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="bdb0f-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bdb0f-118">Technologies</span><span class="sxs-lookup"><span data-stu-id="bdb0f-118">Technologies</span></span>

-   [<span data-ttu-id="bdb0f-119">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="bdb0f-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bdb0f-120">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bdb0f-120">Prerequisites</span></span>

-   <span data-ttu-id="bdb0f-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="bdb0f-121">C/C++</span></span>
-   <span data-ttu-id="bdb0f-122">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="bdb0f-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bdb0f-123">Instructions</span><span class="sxs-lookup"><span data-stu-id="bdb0f-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="bdb0f-124">Utiliser une opération Rich Text Edit</span><span class="sxs-lookup"><span data-stu-id="bdb0f-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="bdb0f-125">L’exemple de fonction suivant recherche le texte spécifié dans le texte sélectionné dans un contrôle Rich Edit qui prend en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="bdb0f-126">Si la cible est trouvée, elle devient la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-126">If the target is found, it becomes the new selection.</span></span>


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a><span data-ttu-id="bdb0f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bdb0f-127">Remarks</span></span>

<span data-ttu-id="bdb0f-128">Microsoft Rich Edit 3,0 prend également en charge la fonction de l’éditeur de méthode d’entrée (IME) HexToUnicode, qui permet à un utilisateur d’effectuer une conversion entre des valeurs hexadécimales et Unicode à l’aide de touches d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="bdb0f-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="bdb0f-129">Pour plus d’informations, consultez [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).</span><span class="sxs-lookup"><span data-stu-id="bdb0f-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdb0f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdb0f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdb0f-131">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="bdb0f-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="bdb0f-132">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bdb0f-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 