---
description: Notification de suppression de l’appareil
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notification de suppression de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950363"
---
# <a name="device-removal-notification"></a><span data-ttu-id="08751-103">Notification de suppression de l’appareil</span><span class="sxs-lookup"><span data-stu-id="08751-103">Device Removal Notification</span></span>

<span data-ttu-id="08751-104">Si l’utilisateur supprime un appareil Plug-and-Play que le graphique utilisait, le gestionnaire de graphique de filtre publie un événement de [**\_ \_ perte d’appareil ce**](ec-device-lost.md) .</span><span class="sxs-lookup"><span data-stu-id="08751-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="08751-105">Si le périphérique redevient disponible, le gestionnaire de graphique de filtre publie un autre événement de **\_ \_ perte d’appareil EC** .</span><span class="sxs-lookup"><span data-stu-id="08751-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="08751-106">Toutefois, l’état précédent du filtre de capture n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="08751-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="08751-107">L’application doit reconstruire le graphique pour utiliser l’appareil.</span><span class="sxs-lookup"><span data-stu-id="08751-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="08751-108">DirectShow n’envoie aucun événement lorsqu’un nouvel appareil est branché.</span><span class="sxs-lookup"><span data-stu-id="08751-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="08751-109">Pour savoir quand un nouvel appareil est disponible, l’application peut surveiller les \_ messages de fenêtre WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="08751-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="08751-110">Pour plus d’informations, consultez « Gestion des périphériques » dans la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="08751-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08751-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08751-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08751-112">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="08751-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



