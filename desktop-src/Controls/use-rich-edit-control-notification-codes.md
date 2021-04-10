---
title: Comment utiliser les codes de notification de contrôle RichEdit
description: La fenêtre parente d’un contrôle RichEdit peut traiter les codes de notification pour surveiller les événements qui affectent le contrôle. Les contrôles RichEdit prennent en charge tous les codes de notification utilisés avec les contrôles d’édition, ainsi que plusieurs autres.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103940781"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="15400-104">Comment utiliser les codes de notification de contrôle RichEdit</span><span class="sxs-lookup"><span data-stu-id="15400-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="15400-105">La fenêtre parente d’un contrôle RichEdit peut traiter les codes de notification pour surveiller les événements qui affectent le contrôle.</span><span class="sxs-lookup"><span data-stu-id="15400-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="15400-106">Les contrôles RichEdit prennent en charge tous les codes de notification utilisés avec les contrôles d’édition, ainsi que plusieurs autres.</span><span class="sxs-lookup"><span data-stu-id="15400-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="15400-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="15400-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="15400-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="15400-108">Technologies</span></span>

-   [<span data-ttu-id="15400-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="15400-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="15400-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="15400-110">Prerequisites</span></span>

-   <span data-ttu-id="15400-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="15400-111">C/C++</span></span>
-   <span data-ttu-id="15400-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="15400-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="15400-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="15400-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="15400-114">Utiliser un code de notification Rich Edit Control</span><span class="sxs-lookup"><span data-stu-id="15400-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="15400-115">Vous pouvez déterminer les codes de notification qu’un contrôle RichEdit envoie à sa fenêtre parente en définissant son masque d’événement.</span><span class="sxs-lookup"><span data-stu-id="15400-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="15400-116">Pour définir le masque d’événement pour un contrôle RichEdit, utilisez le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="15400-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="15400-117">Vous pouvez récupérer le masque d’événement actuel d’un contrôle RichEdit à l’aide du message [**em \_ GETEVENTMASK**](em-geteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="15400-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="15400-118">Pour obtenir la liste des indicateurs de masque d’événement, consultez [indicateurs de masque d’événement de contrôle RichEdit](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="15400-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="15400-119">La fenêtre parente d’un contrôle RichEdit peut filtrer toutes les entrées du clavier et de la souris dans le contrôle en traitant le code de notification en [ \_ msgfilter](en-msgfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="15400-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="15400-120">La fenêtre parente peut empêcher le traitement du message clavier ou de la souris, ou peut modifier le message en modifiant la structure [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="15400-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="15400-121">Une application peut traiter le code de notification en [ \_ protégé](en-protected.md) pour détecter quand l’utilisateur tente de modifier du texte protégé.</span><span class="sxs-lookup"><span data-stu-id="15400-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="15400-122">Pour marquer une plage de texte comme protégée, vous pouvez définir l’effet de caractère protégé.</span><span class="sxs-lookup"><span data-stu-id="15400-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="15400-123">Vous pouvez autoriser l’utilisateur à déposer des fichiers dans un contrôle Rich Edit en traitant le code de notification en [ \_ DROPFILES](en-dropfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="15400-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="15400-124">La structure [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) spécifiée contient des informations sur les fichiers en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="15400-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15400-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15400-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15400-126">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="15400-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="15400-127">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="15400-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




