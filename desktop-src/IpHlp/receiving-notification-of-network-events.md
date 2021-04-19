---
description: Utilisez les fonctions suivantes pour vous assurer qu’une application reçoit une notification de certains événements réseau.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Réception des notifications d’événements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514001"
---
# <a name="receiving-notification-of-network-events"></a><span data-ttu-id="2c8b3-103">Réception des notifications d’événements réseau</span><span class="sxs-lookup"><span data-stu-id="2c8b3-103">Receiving Notification of Network Events</span></span>

<span data-ttu-id="2c8b3-104">Utilisez les fonctions suivantes pour vous assurer qu’une application reçoit une notification de certains événements réseau.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-104">Use the following functions to ensure that an application receives notification of certain network events.</span></span>

<span data-ttu-id="2c8b3-105">Utilisez la fonction [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) pour demander une notification des modifications qui se produisent dans le mappage entre les adresses IP et les interfaces sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-105">Use the [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) function to request notification of any change that occurs in the mapping between IP addresses and interfaces on the local computer.</span></span>

<span data-ttu-id="2c8b3-106">De même, la fonction [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permet à une application de demander la notification de toute modification qui se produit dans la table de routage IP.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-106">Similarly, the [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) function enables an application to request notification of any change that occurs in the IP routing table.</span></span>

<span data-ttu-id="2c8b3-107">Les notifications fournies par ces fonctions ne spécifient pas ce qui a changé ; ils spécifient simplement qu’un événement a changé.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-107">The notifications provided by these functions do not specify what changed; they simply specify that something changed.</span></span> <span data-ttu-id="2c8b3-108">Utilisez d’autres fonctions d’assistance IP, telles que [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) et [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), pour déterminer la nature exacte de la modification.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-108">Use other IP Helper functions, such as [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) and [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), to determine the exact nature of the change.</span></span>

 

 



