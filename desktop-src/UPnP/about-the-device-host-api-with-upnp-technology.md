---
title: À propos de l’API d’hôte d’appareil
description: L’API d’hôte d’appareil avec la technologie UPnP est une infrastructure permettant d’implémenter les fonctionnalités d’appareil UPnP sur la plateforme Windows.
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380278"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="0b66f-103">À propos de l’API d’hôte d’appareil</span><span class="sxs-lookup"><span data-stu-id="0b66f-103">About the Device Host API</span></span>

<span data-ttu-id="0b66f-104">L’API d’hôte d’appareil avec la technologie UPnP est une infrastructure permettant d’implémenter les fonctionnalités d’appareil UPnP sur la plateforme Windows.</span><span class="sxs-lookup"><span data-stu-id="0b66f-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="0b66f-105">Les développeurs qui créent des appareils à l’aide de l’API d’hôte d’appareil avec la technologie UPnP (appelés [*appareils hébergés*](h-gly.md)) ont besoin d’implémenter uniquement les fonctionnalités principales de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0b66f-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="0b66f-106">Les développeurs peuvent s’appuyer sur l’hôte de l’appareil pour gérer les détails propres à UPnP en matière de découverte, de description, de contrôle, d’événement et de présentation.</span><span class="sxs-lookup"><span data-stu-id="0b66f-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="0b66f-107">L’hôte d’appareil valide les données entrantes à partir de clients UPnP et met en forme toutes les données sortantes à partir d’appareils hébergés en fonction de l’architecture de périphérique UPnP.</span><span class="sxs-lookup"><span data-stu-id="0b66f-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="0b66f-108">Les sections suivantes expliquent en général comment fonctionne l’hôte de périphérique UPnP :</span><span class="sxs-lookup"><span data-stu-id="0b66f-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="0b66f-109">Implémentation d’un appareil hébergé</span><span class="sxs-lookup"><span data-stu-id="0b66f-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="0b66f-110">Inscription d’un appareil hébergé auprès de l’hôte de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0b66f-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="0b66f-111">Fournisseurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="0b66f-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="0b66f-112">Événements</span><span class="sxs-lookup"><span data-stu-id="0b66f-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="0b66f-113">Présentation</span><span class="sxs-lookup"><span data-stu-id="0b66f-113">Presentation</span></span>](presentation.md)

 

 




