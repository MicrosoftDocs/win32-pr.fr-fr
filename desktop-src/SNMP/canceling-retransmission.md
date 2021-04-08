---
title: Annulation de la retransmission
description: S’il n’y a aucune réponse à une demande de communication dans le délai d’attente spécifié pour une entité de destination et si des retransmissions sont spécifiées pour l’entité, l’implémentation de l’WinSNMP de Microsoft retransmet la demande.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029204"
---
# <a name="canceling-retransmission"></a><span data-ttu-id="68f35-103">Annulation de la retransmission</span><span class="sxs-lookup"><span data-stu-id="68f35-103">Canceling Retransmission</span></span>

<span data-ttu-id="68f35-104">S’il n’y a aucune réponse à une demande de communication dans le délai d’attente spécifié pour une entité de destination et si des retransmissions sont spécifiées pour l’entité, l’implémentation de l’WinSNMP de Microsoft retransmet la demande.</span><span class="sxs-lookup"><span data-stu-id="68f35-104">If there is no response to a communication request within the time-out period specified for a destination entity, and if retransmissions are specified for the entity, the Microsoft WinSNMP implementation retransmits the request.</span></span> <span data-ttu-id="68f35-105">Un appel à la fonction [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) peut annuler ce cycle de retransmission et libérer les structures de données internes associées à la demande de message.</span><span class="sxs-lookup"><span data-stu-id="68f35-105">A call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function can cancel this retransmission cycle and release internal data structures associated with the message request.</span></span>

<span data-ttu-id="68f35-106">Notez qu’il est possible pour une entité de destination de recevoir un message SNMP qui a été annulé par un appel à la fonction [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) .</span><span class="sxs-lookup"><span data-stu-id="68f35-106">Note that it is possible for a destination entity to receive an SNMP message that has been canceled by a call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function.</span></span> <span data-ttu-id="68f35-107">Il est également possible qu’une entité de destination puisse répondre à un message SNMP annulé.</span><span class="sxs-lookup"><span data-stu-id="68f35-107">It is also possible that a destination entity can respond to a canceled SNMP message.</span></span> <span data-ttu-id="68f35-108">Cela est dû au fait que la mise en file d’attente des transactions se produit à plusieurs niveaux.</span><span class="sxs-lookup"><span data-stu-id="68f35-108">This is because transaction queuing occurs at multiple levels.</span></span> <span data-ttu-id="68f35-109">Toutefois, une fois qu’un message a été annulé par un appel à [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), l’implémentation de l’WinSNMP de Microsoft ne retransmet pas le message, soumet un PDU de réponse ou envoie une notification d’expiration à l’application pour ce message.</span><span class="sxs-lookup"><span data-stu-id="68f35-109">However, once a message has been canceled by a call to [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), the Microsoft WinSNMP implementation will not retransmit the message, submit a response PDU, or send a time-out notification to the application for that message.</span></span>

 

 




