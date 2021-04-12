---
description: Le protocole Kerberos est composé de trois sous-protocoles.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Sous-protocoles Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203179"
---
# <a name="kerberos-subprotocols"></a><span data-ttu-id="80eae-103">Sous-protocoles Kerberos</span><span class="sxs-lookup"><span data-stu-id="80eae-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="80eae-104">Le [*protocole Kerberos*](../secgloss/k-gly.md) est composé de trois sous-protocoles.</span><span class="sxs-lookup"><span data-stu-id="80eae-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="80eae-105">Sous-protocole</span><span class="sxs-lookup"><span data-stu-id="80eae-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="80eae-106">Signification</span><span class="sxs-lookup"><span data-stu-id="80eae-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80eae-107">Échange de service d'authentification</span><span class="sxs-lookup"><span data-stu-id="80eae-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="80eae-108">Dans ce sous-protocole, le [*Centre de distribution de clés*](../secgloss/k-gly.md) (KDC) donne au client une [*clé de session*](../secgloss/s-gly.md) de connexion et un ticket TGT (Ticket-Granting Ticket).</span><span class="sxs-lookup"><span data-stu-id="80eae-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="80eae-109">Échange de service TG (ticket-granting)</span><span class="sxs-lookup"><span data-stu-id="80eae-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="80eae-110">Dans ce sous-protocole, le centre de distribution de clés distribue une clé de session de service et un ticket pour le service.</span><span class="sxs-lookup"><span data-stu-id="80eae-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="80eae-111">Échange client/serveur</span><span class="sxs-lookup"><span data-stu-id="80eae-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="80eae-112">Dans ce sous-protocole, le client présente le ticket d’admission à un service.</span><span class="sxs-lookup"><span data-stu-id="80eae-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
