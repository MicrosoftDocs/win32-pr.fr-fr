---
description: Le service de notification d’événements système permet aux applications mobiles de recevoir des notifications d’événements système qui effectuent des analyses. Lorsque l’événement demandé se produit, SENS notifie l’application.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notifications (service de notification d’événements système)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535527"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="521ae-104">Notifications (service de notification d’événements système)</span><span class="sxs-lookup"><span data-stu-id="521ae-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="521ae-105">Le service de notification d’événements système permet aux applications mobiles de recevoir des notifications d’événements système qui effectuent des analyses.</span><span class="sxs-lookup"><span data-stu-id="521ae-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="521ae-106">Lorsque l’événement demandé se produit, SENS notifie l’application.</span><span class="sxs-lookup"><span data-stu-id="521ae-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="521ae-107">SENS peut notifier les applications de trois classes d’événements système :</span><span class="sxs-lookup"><span data-stu-id="521ae-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="521ae-108">Événements de réseau TCP/IP, tels que l’état d’une connexion réseau TCP/IP ou la qualité de la connexion.</span><span class="sxs-lookup"><span data-stu-id="521ae-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="521ae-109">Événements d’ouverture de session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="521ae-109">User logon events.</span></span>
-   <span data-ttu-id="521ae-110">Les événements de batterie et d’alimentation secteur.</span><span class="sxs-lookup"><span data-stu-id="521ae-110">Battery and AC power events.</span></span>

<span data-ttu-id="521ae-111">Par exemple, une application peut s’abonner à l’un des événements système suivants :</span><span class="sxs-lookup"><span data-stu-id="521ae-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="521ae-112">Établissement de la connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="521ae-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="521ae-113">Notification quand une destination spécifiée peut être atteinte dans les paramètres QOC (Quality of Connection) spécifiés</span><span class="sxs-lookup"><span data-stu-id="521ae-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="521ae-114">L’ordinateur a basculé sur la batterie</span><span class="sxs-lookup"><span data-stu-id="521ae-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="521ae-115">Le pourcentage de la puissance de la batterie restante est compris dans un paramètre spécifié</span><span class="sxs-lookup"><span data-stu-id="521ae-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="521ae-116">Les événements planifiés à l’aide du gestionnaire de synchronisation se produisent</span><span class="sxs-lookup"><span data-stu-id="521ae-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="521ae-117">**Windows Server 2008 R2 et Windows 7 :** L’abonné a un maximum de 3 minutes pour répondre à une notification sur les interfaces [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) et [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) .</span><span class="sxs-lookup"><span data-stu-id="521ae-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="521ae-118">Au bout de 3 minutes, SENS annule l’appel aux abonnés et débloque le thread de notification.</span><span class="sxs-lookup"><span data-stu-id="521ae-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="521ae-119">Si une longue opération est nécessaire pour répondre à la notification, retournez à partir de **ISensLogon** ou de **ISensLogon2** aussi rapidement que possible et ouvrez un autre thread pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="521ae-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



