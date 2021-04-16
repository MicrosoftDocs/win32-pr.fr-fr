---
title: Contrôle de capture précis
description: Contrôle de capture précis
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Fonctions de rappel AVICap, contrôle de capture précis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507190"
---
# <a name="precise-capture-control"></a><span data-ttu-id="d2ff8-104">Contrôle de capture précis</span><span class="sxs-lookup"><span data-stu-id="d2ff8-104">Precise Capture Control</span></span>

<span data-ttu-id="d2ff8-105">Une fenêtre de capture peut fournir la fonction de rappel de contrôle de capture avec un contrôle précis sur les moments de début et de fin de la capture de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="d2ff8-106">Le premier message envoyé à partir du pilote de capture à la procédure de rappel définit le paramètre *nState* sur le \_ préroll CONTROLCALLBACK après avoir alloué toutes les mémoires tampons et toutes les autres préparations de capture sont terminées.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="d2ff8-107">Ce message donne à l’application la possibilité de Prérouler les sources vidéo.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="d2ff8-108">(La fonction de rappel spécifie *nState* comme deuxième paramètre.) La fonction de rappel retourne alors à l’enregistrement exact du moment.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="d2ff8-109">La valeur de retour **true** à partir de la fonction de rappel continue la capture.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="d2ff8-110">La valeur de retour **false** abandonne la capture.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="d2ff8-111">Une fois la capture lancée, la fonction de rappel est appelée fréquemment avec *nState* défini sur la \_ capture CONTROLCALLBACK pour permettre à l’application de terminer la capture en renvoyant la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="d2ff8-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




