---
title: Comment redimensionner automatiquement les contrôles RichEdit
description: Une application peut redimensionner un contrôle RichEdit en fonction des besoins afin qu’elle ait toujours la même taille que son contenu.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031948"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="83341-103">Comment redimensionner automatiquement les contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="83341-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="83341-104">Une application peut redimensionner un contrôle RichEdit en fonction des besoins afin qu’elle ait toujours la même taille que son contenu.</span><span class="sxs-lookup"><span data-stu-id="83341-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="83341-105">Un contrôle Rich Edit prend en charge cette fonctionnalité dite « sans *bas* » en envoyant à sa fenêtre parente un code de notification en [ \_ REQUESTRESIZE](en-requestresize.md) chaque fois que la taille du contenu du contrôle change.</span><span class="sxs-lookup"><span data-stu-id="83341-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="83341-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="83341-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="83341-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="83341-107">Technologies</span></span>

-   [<span data-ttu-id="83341-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="83341-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="83341-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="83341-109">Prerequisites</span></span>

-   <span data-ttu-id="83341-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="83341-110">C/C++</span></span>
-   <span data-ttu-id="83341-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="83341-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="83341-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="83341-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="83341-113">Redimensionner automatiquement un contrôle RichEdit</span><span class="sxs-lookup"><span data-stu-id="83341-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="83341-114">Lors du traitement du code de notification en [ \_ REQUESTRESIZE](en-requestresize.md) , une application doit redimensionner le contrôle avec les dimensions de la structure [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="83341-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="83341-115">Une application peut également déplacer toutes les informations qui se trouvent près du contrôle afin de s’adapter aux changements de hauteur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="83341-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="83341-116">Pour redimensionner le contrôle, vous pouvez utiliser la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="83341-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="83341-117">Vous pouvez forcer un contrôle RichEdit sans fin pour envoyer un code de notification en [ \_ REQUESTRESIZE](en-requestresize.md) à l’aide du message [**em \_ REQUESTRESIZE**](em-requestresize.md) .</span><span class="sxs-lookup"><span data-stu-id="83341-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="83341-118">Ce message peut être utile lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="83341-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="83341-119">Notes</span><span class="sxs-lookup"><span data-stu-id="83341-119">Remarks</span></span>

<span data-ttu-id="83341-120">Pour recevoir les codes de notification en [ \_ REQUESTRESIZE](en-requestresize.md) , vous devez activer la notification à l’aide du message [em \_ SETEVENTMASK](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="83341-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83341-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83341-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83341-122">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="83341-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="83341-123">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="83341-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 