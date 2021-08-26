---
title: Gérer les adresses IP avec AddIPAddress, DeleteIPAddress
description: La fonction AddIPAddress ajoute l’adresse IPv4 spécifiée à l’adaptateur spécifié.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e726a2e5785641532abb739d61143f9fabfdd10c38e4b51fcd529f20d92503d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870089"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Gérer les adresses IP avec AddIPAddress, DeleteIPAddress

La fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) ajoute l’adresse IPv4 spécifiée à l’adaptateur spécifié. La fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) supprime l’adresse IPv4 spécifiée de l’adaptateur spécifié. Ces fonctions peuvent être utilisées pour ajouter et supprimer des adresses IPv4 sur une carte réseau.

Une adresse IPv4 ajoutée par la fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) n’est pas persistante. L’adresse IPv4 existe uniquement tant que l’objet d’adaptateur existe. Le redémarrage de l’ordinateur détruit l’adresse IPv4, tout comme la réinitialisation manuelle de la carte d’interface réseau (NIC).

Une fois que [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) a été appelé avec succès, DHCP est désactivé pour l’adresse IP qui a été ajoutée. Par conséquent, les fonctions telles que [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), qui requièrent l’activation de DHCP, ne seront pas fonctionnelles sur l’adresse IP ajoutée. La fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) peut être utilisée pour supprimer l’adresse IPv4 ajoutée.

> [!Note]  
> Les stratégies de groupe, les stratégies d’entreprise et autres restrictions sur le réseau peuvent empêcher l’exécution correcte de ces fonctions. Assurez-vous que l’application dispose des autorisations réseau nécessaires avant d’essayer d’utiliser ces fonctions.

 

**Pour utiliser AddIPAddress**

1.  Déclarez les variables **ULong** nommées `NTEContext` et `NTEInstance` , toutes deux initialisées à zéro.
    > [!Note]  
    > La `NTEContext` variable est le seul paramètre de la fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) ; pour supprimer l’adresse IP ajoutée, elle `NTEContext` doit être stockée et inchangée.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Déclarez les variables pour les structures IPAddr et IPMask nommées `iaIPAddress` et `iaIPMask` , respectivement. Ces valeurs sont simplement des entiers non signés. Initialisez les `iaIPAddress` `iaIPMask` variables et à l’aide de la fonction [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Appelez la fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) pour ajouter l’adresse IPv4. Recherchez les erreurs et renvoyez la valeur d’erreur à la variable **DWORD** `dwRetVal` (pour une vérification des erreurs plus poussée).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > Le troisième paramètre est l’index de l’adaptateur, qui peut être obtenu en appelant la fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Il est supposé que la variable retournée par cette fonction est nommée `pIPAddrTable` . Pour obtenir de l’aide sur la fonction **GetIpAddrTable** , consultez Gestion de l' [adresse IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Pour utiliser DeleteIpAddress**

-   Appelez la fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , en passant la `NTEContext` variable en tant que paramètre. Recherchez les erreurs et renvoyez la valeur d’erreur à la variable **DWORD** `dwRetVal` (pour une vérification des erreurs plus poussée).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Pour utiliser [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) doit d’abord être appelé pour recevoir le descripteur `NTEContext` . La procédure précédente suppose que **AddIpAddress** a déjà été appelé quelque part dans le code et qu’il `NTEContext` a été enregistré et qu’il n’est pas endommagé.

 

Étape suivante : [récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)

Étape précédente : [gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
