---
description: Vous pouvez utiliser l’assistance IP pour effectuer des opérations ARP (Address Resolution Protocol) pour l’ordinateur local. Utilisez les fonctions suivantes pour récupérer et modifier la table ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Utilisation du protocole de résolution d’adresses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530913"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="f412a-104">Utilisation du protocole de résolution d’adresses</span><span class="sxs-lookup"><span data-stu-id="f412a-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="f412a-105">Vous pouvez utiliser l’assistance IP pour effectuer des opérations ARP (Address Resolution Protocol) pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f412a-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="f412a-106">Utilisez les fonctions suivantes pour récupérer et modifier la table ARP.</span><span class="sxs-lookup"><span data-stu-id="f412a-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="f412a-107">Le [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) récupère la table ARP.</span><span class="sxs-lookup"><span data-stu-id="f412a-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="f412a-108">La table ARP contient le mappage d’adresses IP à des adresses physiques.</span><span class="sxs-lookup"><span data-stu-id="f412a-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="f412a-109">Les adresses physiques sont parfois appelées adresses MAC (Media Access Controller).</span><span class="sxs-lookup"><span data-stu-id="f412a-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="f412a-110">Utilisez les fonctions [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) et [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) pour ajouter ou supprimer des entrées ARP particulières vers ou à partir de la table.</span><span class="sxs-lookup"><span data-stu-id="f412a-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="f412a-111">La fonction [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) supprime toutes les entrées de la table.</span><span class="sxs-lookup"><span data-stu-id="f412a-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="f412a-112">Pour créer ou supprimer des entrées de proxy ARP, utilisez les fonctions [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) et [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .</span><span class="sxs-lookup"><span data-stu-id="f412a-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="f412a-113">La fonction [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envoie une requête ARP au réseau local.</span><span class="sxs-lookup"><span data-stu-id="f412a-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



