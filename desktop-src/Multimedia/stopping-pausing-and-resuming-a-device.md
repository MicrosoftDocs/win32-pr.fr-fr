---
title: Arrêt, suspension et reprise d’un appareil
description: Arrêt, suspension et reprise d’un appareil
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Commande MCI_STOP
- Commande MCI_PAUSE
- Commande MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673334"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="c5cbd-106">Arrêt, suspension et reprise d’un appareil</span><span class="sxs-lookup"><span data-stu-id="c5cbd-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="c5cbd-107">La commande [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) interrompt la diffusion ou l’enregistrement d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="c5cbd-108">De nombreux appareils prennent également en charge la commande [**Pause**](pause.md) ([**\_ Pause MCI**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="c5cbd-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="c5cbd-109">La différence entre l' **arrêt** et la **Pause** dépend de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="c5cbd-110">En règle générale, **suspendre** l’opération interrompt, mais laisse l’appareil prêt à reprendre la lecture ou l’enregistrement immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="c5cbd-111">L’utilisation de la commande [**lire**](play.md) ([**\_ lecture MCI**](mci-play.md)) ou [**Enregistrer**](record.md) ([**\_ enregistrement MCI**](mci-record.md)) pour redémarrer un appareil réinitialise les emplacements spécifiés avec les indicateurs « to » (MCI \_ à) et « from » (MCI \_ à partir de) avant la suspension ou l’arrêt de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="c5cbd-112">Sans l’indicateur « from », ces commandes réinitialisent l’emplacement de départ à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="c5cbd-113">Sans l’indicateur « to », ils réinitialisent l’emplacement de fin à la fin du support.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="c5cbd-114">Pour poursuivre la lecture ou l’enregistrement sans réinitialiser une position d’arrêt précédemment spécifiée, utilisez l’indicateur « to » de la commande **Play** ou **Record** pour spécifier une position de fin.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="c5cbd-115">Certains appareils prennent en charge la commande de [**reprise**](resume.md) ([**\_ Resume MCI**](mci-resume.md)) pour redémarrer un appareil suspendu.</span><span class="sxs-lookup"><span data-stu-id="c5cbd-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="c5cbd-116">Cette commande ne change pas les emplacements « to » et « from » spécifiés avec la commande **Play** ou **Record** qui a précédé la commande [**Pause**](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="c5cbd-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




