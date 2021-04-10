---
description: Les clouds sont utilisés par les infrastructures de regroupement et de représentation graphique des homologues.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Clouds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115579"
---
# <a name="clouds"></a><span data-ttu-id="1754f-103">Clouds</span><span class="sxs-lookup"><span data-stu-id="1754f-103">Clouds</span></span>

<span data-ttu-id="1754f-104">Les clouds sont utilisés par les infrastructures de [regroupement](grouping-api.md) et de [représentation graphique](graphing-api.md) des homologues.</span><span class="sxs-lookup"><span data-stu-id="1754f-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="1754f-105">Le [protocole PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) identifie un Cloud comme un ensemble d’homologues qui peuvent communiquer au sein de la même étendue IPv6.</span><span class="sxs-lookup"><span data-stu-id="1754f-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="1754f-106">Les clouds sont étroitement liés aux étendues IPv6.</span><span class="sxs-lookup"><span data-stu-id="1754f-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="1754f-107">La liste suivante répertorie certaines des fonctionnalités de Cloud uniques :</span><span class="sxs-lookup"><span data-stu-id="1754f-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="1754f-108">Un Cloud est identifié par un nom, et les clouds disponibles peuvent être énumérés à l’aide de [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="1754f-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="1754f-109">Si un ordinateur est connecté à Internet, il fait partie d’un Cloud global, qui est identifié par la chaîne « global \_ ».</span><span class="sxs-lookup"><span data-stu-id="1754f-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="1754f-110">Si un ordinateur est connecté à un ou plusieurs réseaux locaux (LAN), des clouds individuels sont disponibles pour chaque lien.</span><span class="sxs-lookup"><span data-stu-id="1754f-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="1754f-111">Un ordinateur peut être connecté à plusieurs réseaux à l’aide de plusieurs cartes réseau ou à l’aide d’un réseau privé virtuel (VPN), ce qui signifie qu’un ordinateur avec une interface peut être visible dans de nombreux Clouds.</span><span class="sxs-lookup"><span data-stu-id="1754f-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="1754f-112">Vous pouvez utiliser PNRP pour inscrire et résoudre des noms d’homologue dans un Cloud spécifique.</span><span class="sxs-lookup"><span data-stu-id="1754f-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 



