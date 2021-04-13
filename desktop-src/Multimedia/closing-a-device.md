---
title: Fermeture d’un appareil
description: Fermeture d’un appareil
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Commande MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379642"
---
# <a name="closing-a-device"></a><span data-ttu-id="73474-104">Fermeture d’un appareil</span><span class="sxs-lookup"><span data-stu-id="73474-104">Closing a Device</span></span>

<span data-ttu-id="73474-105">La commande [**Fermer**](close.md) ([**MCI \_ Close**](mci-close.md)) libère l’accès à un appareil ou à un fichier.</span><span class="sxs-lookup"><span data-stu-id="73474-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="73474-106">MCI libère un appareil lorsque toutes les tâches utilisant un appareil l’ont fermé.</span><span class="sxs-lookup"><span data-stu-id="73474-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="73474-107">Pour faciliter la gestion des appareils par MCI, votre application doit fermer chaque appareil ou fichier une fois qu’il a fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="73474-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="73474-108">Lorsque vous fermez un périphérique MCI externe qui utilise son propre support au lieu de fichiers (tels qu’un CD audio), le pilote laisse l’appareil dans son mode de fonctionnement actuel.</span><span class="sxs-lookup"><span data-stu-id="73474-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="73474-109">Ainsi, si vous fermez un périphérique CD audio en train de jouer, même si le pilote de périphérique est libéré de la mémoire, le périphérique CD audio continue de fonctionner jusqu’à ce qu’il atteigne la fin de son contenu.</span><span class="sxs-lookup"><span data-stu-id="73474-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="73474-110">La fermeture d’une application avec des appareils MCI ouverts peut empêcher d’autres applications d’utiliser ces appareils jusqu’au redémarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="73474-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




