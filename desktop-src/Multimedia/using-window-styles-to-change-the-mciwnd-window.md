---
title: Utilisation de styles de fenêtre pour modifier la fenêtre MCIWnd
description: Utilisation de styles de fenêtre pour modifier la fenêtre MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106538995"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="4c4b3-104">Utilisation de styles de fenêtre pour modifier la fenêtre MCIWnd</span><span class="sxs-lookup"><span data-stu-id="4c4b3-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="4c4b3-105">Comme pour n’importe quelle fenêtre, vous pouvez modifier l’apparence et le comportement d’une fenêtre MCIWnd en choisissant parmi les styles de fenêtre standard spécifiés avec la fonction [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="4c4b3-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="4c4b3-106">En outre, vous pouvez choisir parmi plusieurs autres styles de fenêtre spécifiques aux fenêtres MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="4c4b3-107">Avec ces styles, votre application peut modifier ces fenêtres MCIWnd des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c4b3-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="4c4b3-108">Modifiez la taille de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-108">Change window size.</span></span>
-   <span data-ttu-id="4c4b3-109">Masquer ou afficher des contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-109">Hide or display controls.</span></span>
-   <span data-ttu-id="4c4b3-110">Émettre des messages de notification.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-110">Issue notification messages.</span></span>
-   <span data-ttu-id="4c4b3-111">Affichez les informations dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-111">Display information in the title bar.</span></span>

<span data-ttu-id="4c4b3-112">Vous pouvez définir des styles de fenêtre en les spécifiant dans la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) , ou vous pouvez utiliser la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) pour modifier le style d’une fenêtre MCIWnd existante.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="4c4b3-113">Vous pouvez également interroger une fenêtre MCIWnd pour ses styles actuels à l’aide de la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="4c4b3-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="4c4b3-114">Pour obtenir la liste des styles de fenêtre spécifiques à MCIWnd, consultez [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="4c4b3-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 