---
description: WSPConnect établit une adresse de destination par défaut pour permettre l’utilisation d’un socket avec les opérations Send (WSPSend) et Receive (WSPRecv) suivantes.
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Connexion à un homologue par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540821"
---
# <a name="connecting-to-a-default-peer"></a><span data-ttu-id="081f4-103">Connexion à un homologue par défaut</span><span class="sxs-lookup"><span data-stu-id="081f4-103">Connecting to a Default Peer</span></span>

<span data-ttu-id="081f4-104">Pour un socket lié à un protocole sans connexion, l’opération effectuée par [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) est simplement d’établir une adresse de destination par défaut afin que le socket puisse être utilisé avec les opérations suivantes d’envoi et de réception orientées connexion ([**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="081f4-104">For a socket bound to a connectionless protocol, the operation performed by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) is merely to establish a default destination address so that the socket may be used with subsequent connection-oriented send and receive operations ([**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))).</span></span> <span data-ttu-id="081f4-105">Tous les datagrammes reçus à partir d’une adresse autre que l’adresse de destination spécifiée seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="081f4-105">Any datagrams received from an address other than the destination address specified will be discarded.</span></span>

 

 
