---
title: Comment limiter le mouvement d’un curseur
description: Comme décrit dans à propos des contrôles TrackBar, il est possible de définir une partie off de la plage TrackBar en tant que plage de sélection. L’une des finalités d’une plage de sélection consiste à limiter le déplacement du curseur, en faisant en sorte que certaines parties de la plage complète soient délimitées.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839590"
---
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="c4866-104">Comment limiter le mouvement d’un curseur</span><span class="sxs-lookup"><span data-stu-id="c4866-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="c4866-105">Comme décrit dans [à propos des contrôles TrackBar](trackbar-controls.md), il est possible de définir une partie off de la plage TrackBar en tant que plage de sélection.</span><span class="sxs-lookup"><span data-stu-id="c4866-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="c4866-106">L’une des finalités d’une plage de sélection consiste à limiter le déplacement du curseur, en faisant en sorte que certaines parties de la plage complète soient délimitées.</span><span class="sxs-lookup"><span data-stu-id="c4866-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c4866-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c4866-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c4866-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="c4866-108">Technologies</span></span>

-   [<span data-ttu-id="c4866-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="c4866-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c4866-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c4866-110">Prerequisites</span></span>

-   <span data-ttu-id="c4866-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c4866-111">C/C++</span></span>
-   <span data-ttu-id="c4866-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="c4866-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c4866-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="c4866-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="c4866-114">Limiter le déplacement du curseur</span><span class="sxs-lookup"><span data-stu-id="c4866-114">Limit Slider Movement</span></span>

<span data-ttu-id="c4866-115">L’exemple de code suivant limite le déplacement du curseur en réinitialisant la position du curseur à chaque fois qu’il est déplacé en dehors de la plage de sélection.</span><span class="sxs-lookup"><span data-stu-id="c4866-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a><span data-ttu-id="c4866-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c4866-116">Remarks</span></span>

<span data-ttu-id="c4866-117">Cet extrait de code fait partie de la procédure de fenêtre d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c4866-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4866-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4866-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4866-119">Utilisation des contrôles TrackBar</span><span class="sxs-lookup"><span data-stu-id="c4866-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




