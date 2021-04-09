---
title: Fonctions (entrée tactile Windows)
description: Cette section contient des fonctions pour les entrées tactiles Windows.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Tactile Windows, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032270"
---
# <a name="functions-windows-touch-input"></a><span data-ttu-id="24fd9-104">Fonctions (entrée tactile Windows)</span><span class="sxs-lookup"><span data-stu-id="24fd9-104">Functions (Windows Touch Input)</span></span>

<span data-ttu-id="24fd9-105">Cette section contient des fonctions pour les entrées tactiles Windows.</span><span class="sxs-lookup"><span data-stu-id="24fd9-105">This section contains functions for Windows Touch input.</span></span>

<span data-ttu-id="24fd9-106">Les fonctions suivantes sont utilisées pour l’entrée tactile Windows.</span><span class="sxs-lookup"><span data-stu-id="24fd9-106">The following functions are used for Windows Touch input.</span></span>



| <span data-ttu-id="24fd9-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="24fd9-107">Function</span></span>                                                                                               | <span data-ttu-id="24fd9-108">Description</span><span class="sxs-lookup"><span data-stu-id="24fd9-108">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24fd9-109">**CloseTouchInputHandle**</span><span class="sxs-lookup"><span data-stu-id="24fd9-109">**CloseTouchInputHandle**</span></span>](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | <span data-ttu-id="24fd9-110">Ferme un handle d’entrée tactile, libère la mémoire de processus qui lui est associée et invalide le descripteur.</span><span class="sxs-lookup"><span data-stu-id="24fd9-110">Closes a touch input handle, frees process memory associated with it, and invalidates the handle.</span></span>                                       |
| [<span data-ttu-id="24fd9-111">**GetTouchInputInfo**</span><span class="sxs-lookup"><span data-stu-id="24fd9-111">**GetTouchInputInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | <span data-ttu-id="24fd9-112">Récupère des informations détaillées sur les entrées tactiles associées à une poignée d’entrée tactile spécifique.</span><span class="sxs-lookup"><span data-stu-id="24fd9-112">Retrieves detailed information about touch inputs associated with a specific touch input handle.</span></span>                                        |
| [<span data-ttu-id="24fd9-113">**IsTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="24fd9-113">**IsTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | <span data-ttu-id="24fd9-114">Vérifie si une fenêtre spécifiée est compatible tactile et, éventuellement, récupère les indicateurs de modificateur définis pour la fonctionnalité tactile de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="24fd9-114">Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.</span></span> |
| [<span data-ttu-id="24fd9-115">**RegisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="24fd9-115">**RegisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | <span data-ttu-id="24fd9-116">Inscrit une fenêtre comme étant en mesure de toucher.</span><span class="sxs-lookup"><span data-stu-id="24fd9-116">Registers a window as being touch-capable.</span></span>                                                                                              |
| [<span data-ttu-id="24fd9-117">**UnregisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="24fd9-117">**UnregisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | <span data-ttu-id="24fd9-118">Inscrit une fenêtre comme n’étant plus en mesure de toucher.</span><span class="sxs-lookup"><span data-stu-id="24fd9-118">Registers a window as no longer being touch-capable.</span></span>                                                                                    |
| [<span data-ttu-id="24fd9-119">SendMessage, PostMessage et fonctions connexes</span><span class="sxs-lookup"><span data-stu-id="24fd9-119">SendMessage, PostMessage, and Related Functions</span></span>](sendmessage--postmessage--and-related-functions.md) | <span data-ttu-id="24fd9-120">Contient des considérations relatives au transfert des messages.</span><span class="sxs-lookup"><span data-stu-id="24fd9-120">Contains considerations about forwarding messages.</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="24fd9-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24fd9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24fd9-122">Entrée tactile Windows</span><span class="sxs-lookup"><span data-stu-id="24fd9-122">Windows Touch Input</span></span>](multi-touch-input.md)
</dt> <dt>

[<span data-ttu-id="24fd9-123">Guide de programmation des entrées tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="24fd9-123">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 




