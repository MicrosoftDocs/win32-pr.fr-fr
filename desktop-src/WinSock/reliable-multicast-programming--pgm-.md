---
description: Cette section décrit l’implémentation du protocole de multidiffusion PGM (Pragmatic General Multicast) dans Windows, souvent appelée diffusion fiable. La multidiffusion fiable est implémentée via Windows Sockets dans Windows Server 2003 et versions ultérieures.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programmation de la multidiffusion fiable (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540847"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="80a3b-104">Programmation de la multidiffusion fiable (PGM)</span><span class="sxs-lookup"><span data-stu-id="80a3b-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="80a3b-105">Cette section décrit l’implémentation du protocole de multidiffusion PGM (Pragmatic General Multicast) dans Windows, souvent appelée diffusion fiable.</span><span class="sxs-lookup"><span data-stu-id="80a3b-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="80a3b-106">La multidiffusion fiable est implémentée via Windows Sockets dans Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="80a3b-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="80a3b-107">**Windows XP :** Le PGM est pris en charge uniquement lorsque Microsoft Message Queuing (MSMQ) 3,0 est installé.</span><span class="sxs-lookup"><span data-stu-id="80a3b-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="80a3b-108">Le protocole PGM est un protocole de multidiffusion fiable et évolutif qui permet aux destinataires de détecter la perte, de demander la retransmission des données perdues ou de notifier une application de perte irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="80a3b-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="80a3b-109">Le protocole PGM est un protocole fiable pour le récepteur, ce qui signifie que le récepteur est chargé de vérifier que toutes les données sont reçues, absolving l’expéditeur de la responsabilité de la réception.</span><span class="sxs-lookup"><span data-stu-id="80a3b-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="80a3b-110">Le PGM est approprié pour les applications qui nécessitent la remise de données en multidiffusion sans doublon de plusieurs sources à plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="80a3b-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="80a3b-111">Le PGM ne prend pas en charge la livraison reconnue et ne garantit pas le classement des paquets à partir de plusieurs expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="80a3b-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="80a3b-112">Pour plus d’informations sur le PGM, reportez-vous à la RFC 3208 disponible sur [www.ietf.org](https://www.ietf.org/).</span><span class="sxs-lookup"><span data-stu-id="80a3b-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="80a3b-113">Cette section décrit comment utiliser la multidiffusion fiable sur Windows.</span><span class="sxs-lookup"><span data-stu-id="80a3b-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="80a3b-114">Les rubriques suivantes expliquent les différents aspects de la création d’une application de multidiffusion fiable à l’aide de Windows Sockets :</span><span class="sxs-lookup"><span data-stu-id="80a3b-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="80a3b-115">Expéditeurs et destinataires PGM</span><span class="sxs-lookup"><span data-stu-id="80a3b-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="80a3b-116">Options de l’expéditeur PGM</span><span class="sxs-lookup"><span data-stu-id="80a3b-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="80a3b-117">Envoi et réception de données PGM</span><span class="sxs-lookup"><span data-stu-id="80a3b-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="80a3b-118">Hébergement multiple et PGM</span><span class="sxs-lookup"><span data-stu-id="80a3b-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="80a3b-119">Options de socket PGM</span><span class="sxs-lookup"><span data-stu-id="80a3b-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



