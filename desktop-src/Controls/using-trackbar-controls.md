---
title: Utilisation des contrôles TrackBar
description: Cette section fournit des détails d’implémentation et des exemples pour les contrôles TrackBar.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672881"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="783cb-103">Utilisation des contrôles TrackBar</span><span class="sxs-lookup"><span data-stu-id="783cb-103">Using Trackbar Controls</span></span>

<span data-ttu-id="783cb-104">Cette section fournit des détails d’implémentation et des exemples pour les contrôles TrackBar.</span><span class="sxs-lookup"><span data-stu-id="783cb-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="783cb-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="783cb-105">In this section</span></span>



| <span data-ttu-id="783cb-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="783cb-106">Topic</span></span>                                                                                                  | <span data-ttu-id="783cb-107">Description</span><span class="sxs-lookup"><span data-stu-id="783cb-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="783cb-108">Comment créer un TrackBar</span><span class="sxs-lookup"><span data-stu-id="783cb-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="783cb-109">Lorsque le TrackBar est créé, sa plage et sa plage de sélection sont initialisées.</span><span class="sxs-lookup"><span data-stu-id="783cb-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="783cb-110">La taille de la page est également définie à ce stade.</span><span class="sxs-lookup"><span data-stu-id="783cb-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="783cb-111">Comment traiter des messages de notification TrackBar</span><span class="sxs-lookup"><span data-stu-id="783cb-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="783cb-112">Trackbars notifier la fenêtre parente des actions de l’utilisateur en lui envoyant un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="783cb-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="783cb-113">Comment limiter le mouvement d’un curseur</span><span class="sxs-lookup"><span data-stu-id="783cb-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="783cb-114">Comme décrit dans [à propos des contrôles TrackBar](trackbar-controls.md), il est possible de définir une partie off de la plage TrackBar en tant que plage de sélection.</span><span class="sxs-lookup"><span data-stu-id="783cb-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="783cb-115">L’une des finalités d’une plage de sélection consiste à limiter le déplacement du curseur, en faisant en sorte que certaines parties de la plage complète soient délimitées.</span><span class="sxs-lookup"><span data-stu-id="783cb-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="783cb-116">Utilisation des fenêtres d’amis</span><span class="sxs-lookup"><span data-stu-id="783cb-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="783cb-117">En définissant d’autres contrôles en tant que fenêtres d’amis pour un TrackBar, vous pouvez positionner automatiquement ces contrôles aux extrémités du TrackBar en tant qu’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="783cb-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





