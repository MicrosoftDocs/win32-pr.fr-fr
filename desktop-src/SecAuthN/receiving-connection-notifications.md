---
description: Certaines applications doivent recevoir la notification des événements de connexion avant l’événement, juste après qu’elle ait lieu, ou les deux. Vous pouvez créer une DLL pour recevoir la notification d’avance et de fin des événements de connexion.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Réception des notifications de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524874"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="d482c-104">Réception des notifications de connexion</span><span class="sxs-lookup"><span data-stu-id="d482c-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="d482c-105">Certaines applications doivent recevoir la notification des événements de connexion avant l’événement, juste après qu’elle ait lieu, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="d482c-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="d482c-106">Vous pouvez créer une DLL pour recevoir la notification d’avance et de fin des événements de connexion.</span><span class="sxs-lookup"><span data-stu-id="d482c-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="d482c-107">Le service d’accès à distance (RAS) est un exemple d’application qui doit recevoir la notification préalable d’un événement de connexion.</span><span class="sxs-lookup"><span data-stu-id="d482c-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="d482c-108">RAS doit être informé avant qu’une connexion soit établie, car il peut être nécessaire d’établir une connexion de modem avant d’établir la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="d482c-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="d482c-109">De même, les applications devront peut-être nettoyer les ressources une fois la connexion établie, ce qui nécessite une notification après la connexion.</span><span class="sxs-lookup"><span data-stu-id="d482c-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="d482c-110">Les applications qui souhaitent recevoir une notification anticipée et une notification après le fait des événements de connexion doivent fournir une DLL qui exporte deux fonctions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) et [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span><span class="sxs-lookup"><span data-stu-id="d482c-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="d482c-111">Une fois ces fonctions implémentées, vous devez inscrire votre DLL comme décrit dans la rubrique [inscription pour recevoir des notifications de connexion](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d482c-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



