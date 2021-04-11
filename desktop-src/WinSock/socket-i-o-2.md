---
description: Utilisation des e/s bloquantes, des e/s non bloquantes avec notification asynchrone des événements réseau et des e/s avec chevauchement avec indication d’achèvement dans Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: E/s de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113002"
---
# <a name="socket-io"></a><span data-ttu-id="64c45-103">E/s de socket</span><span class="sxs-lookup"><span data-stu-id="64c45-103">Socket I/O</span></span>

<span data-ttu-id="64c45-104">Il existe trois façons principales d’exécuter des e/s dans Windows Sockets 2 :</span><span class="sxs-lookup"><span data-stu-id="64c45-104">There are three primary ways of doing I/O in Windows Sockets 2:</span></span>

-   <span data-ttu-id="64c45-105">Blocage des e/s.</span><span class="sxs-lookup"><span data-stu-id="64c45-105">Blocking I/O.</span></span>
-   <span data-ttu-id="64c45-106">Des e/s non bloquantes, ainsi que des notifications asynchrones d’événements réseau.</span><span class="sxs-lookup"><span data-stu-id="64c45-106">Nonblocking I/O along with asynchronous notification of network events.</span></span>
-   <span data-ttu-id="64c45-107">E/s avec chevauchement avec indication d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="64c45-107">Overlapped I/O with completion indication.</span></span>

<span data-ttu-id="64c45-108">Nous décrivons chaque méthode dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="64c45-108">We describe each method in the following sections.</span></span> <span data-ttu-id="64c45-109">Le blocage des e/s est le comportement par défaut, le mode non bloquant peut être utilisé sur n’importe quel Socket placé en mode non bloquant, et les e/s avec chevauchement peuvent se produire uniquement sur les sockets créés avec l’attribut Overlapped.</span><span class="sxs-lookup"><span data-stu-id="64c45-109">Blocking I/O is the default behavior, nonblocking mode can be used on any socket that is placed into nonblocking mode, and overlapped I/O can only occur on sockets that are created with the overlapped attribute.</span></span> <span data-ttu-id="64c45-110">Il est également intéressant de noter que les deux appels pour l’envoi de : [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) et les deux appels pour la réception : [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) et [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implémentent chacun les trois méthodes d’e/s.</span><span class="sxs-lookup"><span data-stu-id="64c45-110">It is also interesting to note that the two calls for sending: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and the two calls for receiving: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) each implement all three methods of I/O.</span></span> <span data-ttu-id="64c45-111">Les fournisseurs de services déterminent comment effectuer l’opération d’e/s en fonction des modes de socket, des attributs et des valeurs de paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="64c45-111">Service providers determine how to perform the I/O operation based on socket modes, attributes, and the input parameter values.</span></span>

 

 
