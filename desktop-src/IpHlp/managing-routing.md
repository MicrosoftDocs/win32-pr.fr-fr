---
description: L’assistance IP fournit des fonctionnalités permettant de gérer le routage réseau. Utilisez les fonctions suivantes pour gérer la table de routage IP et pour obtenir d’autres informations de routage.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gestion du routage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862437"
---
# <a name="managing-routing"></a><span data-ttu-id="96a07-104">Gestion du routage</span><span class="sxs-lookup"><span data-stu-id="96a07-104">Managing Routing</span></span>

<span data-ttu-id="96a07-105">L’assistance IP fournit des fonctionnalités permettant de gérer le routage réseau.</span><span class="sxs-lookup"><span data-stu-id="96a07-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="96a07-106">Utilisez les fonctions suivantes pour gérer la table de routage IP et pour obtenir d’autres informations de routage.</span><span class="sxs-lookup"><span data-stu-id="96a07-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="96a07-107">Récupérez le contenu de la table de routage IP en effectuant un appel à la fonction [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) .</span><span class="sxs-lookup"><span data-stu-id="96a07-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="96a07-108">Manipuler des entrées spécifiques dans la table de routage IP à l’aide des fonctions [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)et [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) .</span><span class="sxs-lookup"><span data-stu-id="96a07-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="96a07-109">Utilisez la fonction **CreateIpForwardEntry** pour ajouter une nouvelle entrée de table de routage.</span><span class="sxs-lookup"><span data-stu-id="96a07-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="96a07-110">Utilisez la fonction **DeleteIpForwardEntry** pour supprimer une entrée existante.</span><span class="sxs-lookup"><span data-stu-id="96a07-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="96a07-111">La fonction **SetIpForwardEntry** modifie une entrée existante.</span><span class="sxs-lookup"><span data-stu-id="96a07-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="96a07-112">Les fonctionnalités de gestion de routeur d’assistance IP peuvent être utilisées pour récupérer des informations sur le mode de routage des datagrammes sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="96a07-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="96a07-113">La fonction [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) récupère le meilleur itinéraire vers une adresse de destination spécifiée.</span><span class="sxs-lookup"><span data-stu-id="96a07-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="96a07-114">La fonction [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) récupère l’index de l’interface utilisée par le meilleur itinéraire vers une adresse de destination spécifiée.</span><span class="sxs-lookup"><span data-stu-id="96a07-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="96a07-115">Enfin, la fonction [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) récupère le temps d’aller-retour (RTT) et le nombre de tronçons vers une adresse de destination spécifiée.</span><span class="sxs-lookup"><span data-stu-id="96a07-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



