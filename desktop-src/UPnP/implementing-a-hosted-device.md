---
title: Implémentation d’un appareil hébergé
description: L’hôte d’appareil avec la technologie UPnP implémente la détection, la description, le contrôle et les événements des principaux protocoles UPnP.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675250"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="89019-103">Implémentation d’un appareil hébergé</span><span class="sxs-lookup"><span data-stu-id="89019-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="89019-104">L’hôte d’appareil avec la technologie UPnP implémente les principaux protocoles UPnP : découverte, description, contrôle et événement.</span><span class="sxs-lookup"><span data-stu-id="89019-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="89019-105">Le développeur qui implémente un appareil hébergé doit uniquement fournir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="89019-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="89019-106">Description de l’appareil et de ses services.</span><span class="sxs-lookup"><span data-stu-id="89019-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="89019-107">Implémentation de la fonctionnalité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89019-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="89019-108">Par exemple, le développeur d’un appareil horloge doit fournir des descriptions de service et d’appareil UPnP, ainsi qu’une implémentation des fonctions d’horloge (telles que la conservation de l’heure, la définition du temps et la réponse aux requêtes pour l’heure actuelle).</span><span class="sxs-lookup"><span data-stu-id="89019-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="89019-109">L’hôte de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="89019-109">The device host:</span></span>

-   <span data-ttu-id="89019-110">Annonce l’appareil conformément au protocole de découverte UPnP.</span><span class="sxs-lookup"><span data-stu-id="89019-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="89019-111">Répond aux requêtes de la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89019-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="89019-112">Achemine les demandes de contrôle vers la partie du code de l’appareil qui implémente les fonctions d’horloge.</span><span class="sxs-lookup"><span data-stu-id="89019-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="89019-113">Gère les abonnements aux services.</span><span class="sxs-lookup"><span data-stu-id="89019-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="89019-114">Envoie des notifications d’événements aux abonnés lorsque l’état du service change.</span><span class="sxs-lookup"><span data-stu-id="89019-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




