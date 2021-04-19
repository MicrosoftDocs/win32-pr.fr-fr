---
title: Lecture et positionnement
description: Lecture et positionnement
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510401"
---
# <a name="playback-and-positioning"></a><span data-ttu-id="e5fca-103">Lecture et positionnement</span><span class="sxs-lookup"><span data-stu-id="e5fca-103">Playback and Positioning</span></span>

<span data-ttu-id="e5fca-104">Un certain nombre de commandes MCI, telles que [**lecture**](play.md) ([**\_ lecture MCI**](mci-play.md)), [**arrêt**](stop.md) (MCI), [**Pause**](pause.md) ([**\_ Pause MCI**](mci-pause.md)), [**reprise**](resume.md) ([**\_ reprise MCI**](mci-resume.md)) et [**recherche**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), affectent la lecture ou le positionnement d’un fichier multimédia.[**\_**](mci-stop.md)</span><span class="sxs-lookup"><span data-stu-id="e5fca-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="e5fca-105">Si un périphérique MCI reçoit une commande de lecture alors qu’une autre commande de lecture est en cours, il accepte la commande et arrête ou remplace la commande précédente.</span><span class="sxs-lookup"><span data-stu-id="e5fca-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="e5fca-106">De nombreuses commandes MCI, telles que [**Set**](set.md) ([**MCI \_ Set**](mci-set.md)), n’affectent pas la lecture.</span><span class="sxs-lookup"><span data-stu-id="e5fca-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="e5fca-107">Une notification de l’une de ces commandes n’interfère pas avec les commandes de lecture ou de position en attente tant que les notifications ne sont pas exécutées à partir de la même instance du pilote.</span><span class="sxs-lookup"><span data-stu-id="e5fca-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="e5fca-108">Par exemple, vous pouvez émettre une commande **Set** ou [**Status**](status.md) ([**\_ État MCI**](mci-status.md)) quand un appareil exécute une commande **Seek** sans arrêter ni remplacer la commande **Seek** .</span><span class="sxs-lookup"><span data-stu-id="e5fca-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="e5fca-109">Toutefois, il ne peut y avoir qu’une seule notification en attente.</span><span class="sxs-lookup"><span data-stu-id="e5fca-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="e5fca-110">Par exemple, si une application demande une notification pour la **lecture** et suit la demande avec l' **État** « démarrer la notification de la position », la notification de **lecture** retourne « remplacé » et la notification pour la commande Status est renvoyée lorsqu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="e5fca-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="e5fca-111">Dans ce cas, toutefois, la commande de **lecture** est toujours réussie, même si l’application n’a pas reçu la notification.</span><span class="sxs-lookup"><span data-stu-id="e5fca-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




