---
title: Utiliser la variation naturelle
description: Utiliser la variation naturelle
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100641"
---
# <a name="use-natural-variation"></a><span data-ttu-id="61e74-103">Utiliser la variation naturelle</span><span class="sxs-lookup"><span data-stu-id="61e74-103">Use Natural Variation</span></span>

<span data-ttu-id="61e74-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61e74-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="61e74-105">Bien que la cohérence de présentation dans l’interface conventionnelle de votre application, telle que les menus et les boîtes de dialogue, rend l’interface plus prévisible, fait varier l’animation et la sortie parlée dans l’interface du caractère.</span><span class="sxs-lookup"><span data-stu-id="61e74-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="61e74-106">Le fait de faire varier les réponses du caractère de manière appropriée fournit une interface plus naturelle.</span><span class="sxs-lookup"><span data-stu-id="61e74-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="61e74-107">Si un caractère adresse toujours l’utilisateur exactement de la même façon ; par exemple, en prononçant toujours les mêmes mots, l’utilisateur est susceptible de prendre en compte l’alésage de caractères, le désintérêt ou même le caractère impropre.</span><span class="sxs-lookup"><span data-stu-id="61e74-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="61e74-108">La communication humaine implique rarement des répétitions précises.</span><span class="sxs-lookup"><span data-stu-id="61e74-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="61e74-109">Même si vous répétez une opération dans une situation similaire, nous pouvons modifier le libellé, les gestes ou l’expression faciale.</span><span class="sxs-lookup"><span data-stu-id="61e74-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="61e74-110">Microsoft agent vous permet de créer des variantes d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="61e74-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="61e74-111">Lorsque vous définissez les animations d’un caractère, vous pouvez utiliser les probabilités de branchement sur n’importe quelle image d’animation pour modifier une animation quand elle est lue.</span><span class="sxs-lookup"><span data-stu-id="61e74-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="61e74-112">Vous pouvez également assigner plusieurs animations à chaque État.</span><span class="sxs-lookup"><span data-stu-id="61e74-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="61e74-113">Microsoft Agent choisit de façon aléatoire l’une des animations affectées chaque fois qu’il lance un État.</span><span class="sxs-lookup"><span data-stu-id="61e74-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="61e74-114">Pour la sortie vocale, vous pouvez également inclure des barres verticales dans le texte de sortie pour faire varier automatiquement le texte prononcé.</span><span class="sxs-lookup"><span data-stu-id="61e74-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="61e74-115">Par exemple, Microsoft Agent sélectionne aléatoirement l’une des instructions suivantes lors du traitement de ce texte dans le cadre de la méthode [**Speak**](speak-method.md) :</span><span class="sxs-lookup"><span data-stu-id="61e74-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="61e74-116">«Je peux affirmer cela. \| Je peux le prononcer. \| Je peux faire autre chose.»</span><span class="sxs-lookup"><span data-stu-id="61e74-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 




