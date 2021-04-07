---
title: Comment implémenter des info-bulles multilignes
description: Les info-bulles multilignes autorisent l’affichage du texte sur plusieurs lignes.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671974"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="fc24b-103">Comment implémenter des info-bulles multilignes</span><span class="sxs-lookup"><span data-stu-id="fc24b-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="fc24b-104">Les info-bulles multilignes autorisent l’affichage du texte sur plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="fc24b-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="fc24b-105">Ils sont pris en charge par la [version 4,70](common-control-versions.md) et les versions ultérieures des contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="fc24b-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="fc24b-106">Votre application crée une info-bulle multiligne en envoyant un message [**atténuation \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , en spécifiant la largeur du rectangle d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fc24b-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="fc24b-107">Le texte qui dépasse cette largeur est renvoyé à la ligne suivante au lieu d’élargir la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fc24b-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="fc24b-108">La hauteur du rectangle est augmentée autant que nécessaire pour accueillir les lignes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fc24b-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="fc24b-109">Le contrôle ToolTip encapsule les lignes automatiquement, ou vous pouvez utiliser une combinaison retour chariot/saut de ligne, \\ r \\ n, pour forcer les sauts de ligne à des emplacements particuliers.</span><span class="sxs-lookup"><span data-stu-id="fc24b-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="fc24b-110">L’illustration suivante montre l’affichage qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="fc24b-110">The resulting display is shown in the following illustration.</span></span>

![capture d’écran d’une boîte de dialogue avec une info-bulle contenant du texte organisé comme un paragraphe à plusieurs lignes](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="fc24b-112">La mémoire tampon de texte spécifiée par le membre **szText** de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) peut contenir uniquement 80 caractères.</span><span class="sxs-lookup"><span data-stu-id="fc24b-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="fc24b-113">Si vous devez utiliser une chaîne plus longue, pointez le membre **lpszText** de **NMTTDISPINFO** vers une mémoire tampon contenant le texte souhaité.</span><span class="sxs-lookup"><span data-stu-id="fc24b-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="fc24b-114">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="fc24b-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fc24b-115">Technologies</span><span class="sxs-lookup"><span data-stu-id="fc24b-115">Technologies</span></span>

-   [<span data-ttu-id="fc24b-116">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="fc24b-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fc24b-117">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fc24b-117">Prerequisites</span></span>

-   <span data-ttu-id="fc24b-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="fc24b-118">C/C++</span></span>
-   <span data-ttu-id="fc24b-119">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="fc24b-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fc24b-120">Instructions</span><span class="sxs-lookup"><span data-stu-id="fc24b-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="fc24b-121">Implémenter des info-bulles multilignes</span><span class="sxs-lookup"><span data-stu-id="fc24b-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="fc24b-122">Le fragment de code suivant est un exemple de gestionnaire de notification [ \_ GETDISPINFO ttn](ttn-getdispinfo.md) simple.</span><span class="sxs-lookup"><span data-stu-id="fc24b-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="fc24b-123">Il active une info-bulle multiligne en définissant le rectangle d’affichage sur 150 pixels.</span><span class="sxs-lookup"><span data-stu-id="fc24b-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="fc24b-124">Un saut de ligne manuel est inséré après le premier mot pour montrer que les sauts de ligne peuvent être difficiles et souples.</span><span class="sxs-lookup"><span data-stu-id="fc24b-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="fc24b-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc24b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc24b-126">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="fc24b-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




