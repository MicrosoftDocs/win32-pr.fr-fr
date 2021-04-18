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
# <a name="managing-ip-addresses"></a>Gestion des adresses IP

L’assistance IP peut faciliter la gestion des adresses IP associées aux interfaces sur l’ordinateur local. Utilisez les fonctions décrites dans les paragraphes suivants pour la gestion des adresses IP.

La fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) récupère une table qui contient le mappage d’adresses IP aux interfaces. Plusieurs adresses IP peuvent être associées à la même interface.

Utilisez la fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) pour ajouter une adresse IP à une interface particulière. Pour supprimer des adresses IP précédemment ajoutées à l’aide de **AddIpAddress**, utilisez la fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

Les fonctions [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requièrent que l’ordinateur local utilise le protocole DHCP (Dynamic Host Configuration Protocol). La fonction **IpReleaseAddress** libère une adresse IP précédemment obtenue à partir de DHCP. La fonction **IpRenewAddress** renouvelle un bail DHCP sur une adresse IP particulière. Un bail DHCP permet à un ordinateur d’utiliser une adresse IP pendant un laps de temps spécifié.

-   Pour obtenir des exemples de code impliquant des [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , consultez [gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

-   Pour obtenir des exemples de code impliquant [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) et [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), consultez [gestion des adresses IP à l’aide de AddIpAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Pour obtenir des exemples de code impliquant [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , consultez [gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



