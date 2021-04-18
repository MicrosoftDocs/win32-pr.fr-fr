---
description: L’assistance IP peut faciliter la gestion des adresses IP associées aux interfaces sur l’ordinateur local. Utilisez les fonctions décrites dans les paragraphes suivants pour la gestion des adresses IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Gestion des adresses IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519280"
---
# <a name="managing-ip-addresses"></a><span data-ttu-id="5670e-104">Gestion des adresses IP</span><span class="sxs-lookup"><span data-stu-id="5670e-104">Managing IP Addresses</span></span>

<span data-ttu-id="5670e-105">L’assistance IP peut faciliter la gestion des adresses IP associées aux interfaces sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5670e-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="5670e-106">Utilisez les fonctions décrites dans les paragraphes suivants pour la gestion des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="5670e-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="5670e-107">La fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) récupère une table qui contient le mappage d’adresses IP aux interfaces.</span><span class="sxs-lookup"><span data-stu-id="5670e-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="5670e-108">Plusieurs adresses IP peuvent être associées à la même interface.</span><span class="sxs-lookup"><span data-stu-id="5670e-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="5670e-109">Utilisez la fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) pour ajouter une adresse IP à une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="5670e-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="5670e-110">Pour supprimer des adresses IP précédemment ajoutées à l’aide de **AddIpAddress**, utilisez la fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="5670e-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="5670e-111">Les fonctions [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requièrent que l’ordinateur local utilise le protocole DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="5670e-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="5670e-112">La fonction **IpReleaseAddress** libère une adresse IP précédemment obtenue à partir de DHCP.</span><span class="sxs-lookup"><span data-stu-id="5670e-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="5670e-113">La fonction **IpRenewAddress** renouvelle un bail DHCP sur une adresse IP particulière.</span><span class="sxs-lookup"><span data-stu-id="5670e-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="5670e-114">Un bail DHCP permet à un ordinateur d’utiliser une adresse IP pendant un laps de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="5670e-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="5670e-115">Pour obtenir des exemples de code impliquant des [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , consultez [gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="5670e-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="5670e-116">Pour obtenir des exemples de code impliquant [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) et [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), consultez [gestion des adresses IP à l’aide de AddIpAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span><span class="sxs-lookup"><span data-stu-id="5670e-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="5670e-117">Pour obtenir des exemples de code impliquant [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , consultez [gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span><span class="sxs-lookup"><span data-stu-id="5670e-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



