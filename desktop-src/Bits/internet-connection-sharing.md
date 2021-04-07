---
title: Partage de connexion Internet
description: BITS peut forcer une connexion d’accès à distance pour les réseaux familiaux qui utilisent le partage de connexion Internet de Microsoft si le partage de connexion est configuré pour effectuer des appels sortants lorsque les ordinateurs sur le réseau accèdent à Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671426"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="0585a-103">Partage de connexion Internet</span><span class="sxs-lookup"><span data-stu-id="0585a-103">Internet Connection Sharing</span></span>

<span data-ttu-id="0585a-104">BITS peut forcer une connexion d’accès à distance pour les réseaux familiaux qui utilisent le partage de connexion Internet de Microsoft si le partage de connexion est configuré pour effectuer des appels sortants lorsque les ordinateurs sur le réseau accèdent à Internet.</span><span class="sxs-lookup"><span data-stu-id="0585a-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="0585a-105">Pour empêcher une connexion d’accès à distance forcée, désactivez l’option **établir une connexion d’accès à distance chaque fois qu’un ordinateur de mon réseau tente d’accéder à Internet** sur l’ordinateur hôte de partage de connexion qui partage sa connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="0585a-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="0585a-106">Les ordinateurs connectés à l’ordinateur hôte de partage de connexion partent du principe qu’ils disposent d’une connexion réseau, de sorte que le service BITS essaie de transférer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="0585a-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="0585a-107">Si l’option d’accès à distance est désactivée sur l’ordinateur hôte et que l’ordinateur hôte n’a pas de connexion active, les transferts échouent avec une erreur temporaire.</span><span class="sxs-lookup"><span data-stu-id="0585a-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="0585a-108">Le service BITS réessaiera périodiquement les transferts.</span><span class="sxs-lookup"><span data-stu-id="0585a-108">BITS will retry the transfers periodically.</span></span>

 

 




