---
title: Utilisation des contrôles ToolTip
description: Cette section contient des exemples qui montrent comment créer différents types d’info-bulles.
ms.assetid: 4486b406-a069-4250-b7ab-671d895b79f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fd4a0cef452be3f9700f8466959043ac8d30b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672882"
---
# <a name="using-tooltip-controls"></a><span data-ttu-id="af514-103">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="af514-103">Using Tooltip Controls</span></span>

<span data-ttu-id="af514-104">Cette section contient des exemples qui montrent comment créer différents types d’info-bulles.</span><span class="sxs-lookup"><span data-stu-id="af514-104">This section contains examples that demonstrate how to create different types of tooltips.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af514-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="af514-105">In this section</span></span>



| <span data-ttu-id="af514-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="af514-106">Topic</span></span>                                                                                                    | <span data-ttu-id="af514-107">Description</span><span class="sxs-lookup"><span data-stu-id="af514-107">Description</span></span>                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af514-108">Comment créer une info-bulle pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="af514-108">How to Create a Tooltip for a Control</span></span>](create-a-tooltip-for-a-control.md)<br/>                   | <span data-ttu-id="af514-109">L’exemple de fonction suivant crée une info-bulle et l’associe au contrôle dont l’ID de ressource est passé.</span><span class="sxs-lookup"><span data-stu-id="af514-109">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span> <br/>                                                                                                                                                  |
| [<span data-ttu-id="af514-110">Comment créer une info-bulle pour une zone rectangulaire</span><span class="sxs-lookup"><span data-stu-id="af514-110">How to Create a Tooltip for a Rectangular Area</span></span>](create-a-tooltip-for-a-rectangular-area.md)<br/> | <span data-ttu-id="af514-111">L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="af514-111">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span> <br/>                                                                                                                                                       |
| [<span data-ttu-id="af514-112">Comment implémenter des info-bulles de suivi</span><span class="sxs-lookup"><span data-stu-id="af514-112">How to Implement Tracking Tooltips</span></span>](implement-tracking-tooltips.md)<br/>                         | <span data-ttu-id="af514-113">Les info-bulles de suivi restent visibles jusqu’à ce qu’elles soient explicitement fermées par l’application et peuvent changer la position sur l’écran dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="af514-113">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="af514-114">Ils sont pris en charge par la [version 4,70](common-control-versions.md) et les versions ultérieures des contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="af514-114">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <br/>                         |
| [<span data-ttu-id="af514-115">Comment implémenter des info-bulles multilignes</span><span class="sxs-lookup"><span data-stu-id="af514-115">How to Implement Multiline Tooltips</span></span>](implement-multiline-tooltips.md)<br/>                       | <span data-ttu-id="af514-116">Les info-bulles multilignes autorisent l’affichage du texte sur plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="af514-116">Multiline tooltips allow text to be displayed on more than one line.</span></span> <br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="af514-117">Comment implémenter des info-bulles</span><span class="sxs-lookup"><span data-stu-id="af514-117">How to Implement Balloon Tooltips</span></span>](implement-balloon-tooltips.md)<br/>                           | <span data-ttu-id="af514-118">Les info-bulles sont similaires aux info-bulles standard, mais elles sont affichées dans un « ballon » de style dessin animé avec une tige pointant sur l’outil.</span><span class="sxs-lookup"><span data-stu-id="af514-118">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="af514-119">Les info-bulles peuvent être à une seule ligne ou multiligne.</span><span class="sxs-lookup"><span data-stu-id="af514-119">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="af514-120">Elles sont créées et gérées à peu près de la même façon que les info-bulles standard.</span><span class="sxs-lookup"><span data-stu-id="af514-120">They are created and handled in much the same way as standard tooltips.</span></span> <br/> |
| [<span data-ttu-id="af514-121">Comment implémenter des info-bulles pour les icônes de barre d’État</span><span class="sxs-lookup"><span data-stu-id="af514-121">How to Implement Tooltips for Status Bar Icons</span></span>](implement-tooltips-for-status-bar-icons.md)<br/> | <span data-ttu-id="af514-122">Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="af514-122">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="af514-123">L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="af514-123">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span> <br/>                                                                                |
| [<span data-ttu-id="af514-124">Comment implémenter des info-bulles In-Place</span><span class="sxs-lookup"><span data-stu-id="af514-124">How to Implement In-Place Tooltips</span></span>](implement-in-place-tooltips.md)<br/>                         | <span data-ttu-id="af514-125">Les info-bulles sur place sont utilisées pour afficher des chaînes de texte pour les objets qui ont été découpés.</span><span class="sxs-lookup"><span data-stu-id="af514-125">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="af514-126">Pour obtenir une illustration, consultez [à propos des contrôles ToolTip](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="af514-126">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span> <br/>                                                                                                      |



 

 

 





