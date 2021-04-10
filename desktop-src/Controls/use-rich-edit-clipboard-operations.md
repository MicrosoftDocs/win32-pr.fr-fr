---
title: Comment utiliser les opérations du presse-papiers RichEdit
description: Une application peut coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le format de presse-papiers le mieux disponible ou un format de presse-papiers spécifique.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941413"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="43f9e-103">Comment utiliser les opérations du presse-papiers RichEdit</span><span class="sxs-lookup"><span data-stu-id="43f9e-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="43f9e-104">Une application peut coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le format de presse-papiers le mieux disponible ou un format de presse-papiers spécifique.</span><span class="sxs-lookup"><span data-stu-id="43f9e-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="43f9e-105">Vous pouvez également déterminer si un contrôle RichEdit peut coller un format de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="43f9e-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="43f9e-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="43f9e-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="43f9e-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="43f9e-107">Technologies</span></span>

-   [<span data-ttu-id="43f9e-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="43f9e-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="43f9e-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="43f9e-109">Prerequisites</span></span>

-   <span data-ttu-id="43f9e-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="43f9e-110">C/C++</span></span>
-   <span data-ttu-id="43f9e-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="43f9e-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="43f9e-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="43f9e-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="43f9e-113">Utilisation d’une opération RichEdit dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="43f9e-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="43f9e-114">Comme avec un contrôle d’édition, vous pouvez copier ou couper le contenu de la sélection actuelle à l’aide du message de [**\_ copie WM**](/windows/desktop/dataxchg/wm-copy) ou de [**\_ Cut**](/windows/desktop/dataxchg/wm-cut) .</span><span class="sxs-lookup"><span data-stu-id="43f9e-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="43f9e-115">De même, vous pouvez coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le message [**WM \_ Paste**](/windows/desktop/dataxchg/wm-paste) .</span><span class="sxs-lookup"><span data-stu-id="43f9e-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="43f9e-116">Le contrôle colle le premier format disponible qu’il reconnaît, ce qui est vraisemblablement le format le plus descriptif.</span><span class="sxs-lookup"><span data-stu-id="43f9e-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="43f9e-117">Pour coller un format de presse-papiers spécifique, vous pouvez utiliser le message [**\_ PASTESPECIAL em**](em-pastespecial.md) .</span><span class="sxs-lookup"><span data-stu-id="43f9e-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="43f9e-118">Ce message est utile pour les applications avec une commande **Collage spécial** qui permet à l’utilisateur de sélectionner le format du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="43f9e-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="43f9e-119">Vous pouvez utiliser le message de la [**\_ CANPASTE em**](em-canpaste.md) pour déterminer si un format donné est reconnu par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="43f9e-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="43f9e-120">Vous pouvez également utiliser le message de la [**\_ CANPASTE em**](em-canpaste.md) pour déterminer si un format de presse-papiers disponible est reconnu par un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="43f9e-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="43f9e-121">Ce message est utile lors du traitement du message [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) .</span><span class="sxs-lookup"><span data-stu-id="43f9e-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="43f9e-122">Une application peut activer ou griser sa commande de **Collage** , selon que le contrôle peut coller n’importe quel format disponible.</span><span class="sxs-lookup"><span data-stu-id="43f9e-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="43f9e-123">Les contrôles RichEdit inscrivent deux formats de presse-papiers :</span><span class="sxs-lookup"><span data-stu-id="43f9e-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="43f9e-124">Format de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="43f9e-124">Rich Text Format</span></span>
-   <span data-ttu-id="43f9e-125">Format de texte enrichi sans objets</span><span class="sxs-lookup"><span data-stu-id="43f9e-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="43f9e-126">Texte et objets RichEdit</span><span class="sxs-lookup"><span data-stu-id="43f9e-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="43f9e-127">Une application peut inscrire ces formats à l’aide de la fonction [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , en spécifiant les \_ valeurs CF RTF, CF \_ RTFNOOBJS et CF \_ RETEXTOBJ.</span><span class="sxs-lookup"><span data-stu-id="43f9e-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43f9e-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43f9e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43f9e-129">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="43f9e-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="43f9e-130">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="43f9e-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 