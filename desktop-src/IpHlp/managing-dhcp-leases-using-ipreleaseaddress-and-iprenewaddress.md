---
title: Gérer les baux DHCP avec IpReleaseAddress, IpRenewAddress
description: Les fonctions IpReleaseAddress et IpRenewAddress sont utilisées pour libérer et renouveler le bail actuel du protocole DHCP (Dynamic Host Configuration Protocol).
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862438"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>Gérer les baux DHCP avec IpReleaseAddress, IpRenewAddress

Les fonctions [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) sont utilisées pour libérer et renouveler le bail actuel du protocole DHCP (Dynamic Host Configuration Protocol). La fonction **IpReleaseAddress** libère une adresse IPv4 précédemment obtenue via DHCP. La fonction **IpRenewAddress** renouvelle un bail sur une adresse IPv4 précédemment obtenue via DHCP. Il est courant d’utiliser ces deux fonctions ensemble, d’abord de libérer le bail avec un appel à **IpReleaseAddress**, puis de renouveler le bail avec un appel à la fonction **IpRenewAddress** .

Lorsqu’un client DHCP a précédemment obtenu un bail DHCP et que [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) n’est pas appelé avant la fonction [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , la demande du client DHCP est envoyée au serveur DHCP qui a émis le bail DHCP initial. Ce serveur DHCP peut ne pas être disponible ou la demande DHCP peut échouer. Lorsqu’un ordinateur hôte a déjà obtenu un bail DHCP et que **IpReleaseAddress** est appelé avant la fonction **IpRenewAddress** , le client DHCP libère d’abord l’adresse IP obtenue et envoie une requête de client DHCP pour une réponse de tout serveur DHCP disponible.

> [!Note]  
> Les fonctions [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requièrent que DHCP soit activé pour s’exécuter correctement.

 

La fonction [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) prend un pointeur vers une structure de mappage d' [**\_ \_ index \_ d’adaptateurs IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) comme seul paramètre. Pour obtenir ce paramètre, appelez d’abord [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo). Pour obtenir de l’aide sur la fonction **GetInterfaceInfo** , consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

**Pour utiliser IpReleaseAddress**

1.  Obtenir un pointeur vers une structure de [**mappage d' \_ \_ index \_ d’adaptateurs IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) à l’aide de la fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . (Pour obtenir de l’aide sur la fonction GetInterfaceInfo, consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)). Créez un  objet DWORD `dwRetVal` (utilisé pour la vérification des erreurs). La variable retournée par **GetInterfaceInfo** est supposée être appelée `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Si le protocole DHCP est activé, appelez la fonction [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , en passant la variable de mappage d’index de la [**\_ carte \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` comme paramètre. Recherchez les erreurs générales et retournez sa valeur à la  variable DWORD `dwRetVal` (pour une vérification plus poussée des erreurs).
    > [!Note]  
    > La fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retourne un paramètre qui peut être utilisé pour vérifier si le protocole DHCP est activé avant d’appeler ces fonctions. Pour obtenir de l’aide sur **GetAdaptersInfo**, consultez [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> Il est courant d’utiliser ces deux fonctions ensemble, d’appeler la fonction [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , puis d’appeler la fonction [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , en passant la même structure que le paramètre aux deux fonctions. La procédure suivante suppose que les fonctions ne sont pas utilisées ensemble ; Toutefois, si les fonctions sont utilisées ensemble, ignorez l’étape 1.

 

**Pour utiliser IpRenewAddress**

1.  Obtenir un pointeur vers une structure de [**mappage d' \_ \_ index \_ d’adaptateurs IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) à l’aide de la fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . (Pour obtenir de l’aide sur la fonction **GetInterfaceInfo** , consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)). Déclarez un objet **DWORD** `dwRetVal` (utilisé pour la vérification des erreurs) si cette variable n’a pas été déclarée. La variable retournée par **GetInterfaceInfo** est supposée être appelée `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Appelez la fonction [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , en passant la variable de mappage d’index de la [**\_ carte \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` comme paramètre. Recherchez les erreurs générales et retournez sa valeur à la  variable DWORD `dwRetVal` (pour une vérification plus poussée des erreurs).
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

Étape suivante : [gestion des adresses IP à l’aide de AddIpAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

Étape précédente : [gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

 

 



