---
description: La fonction GetIpAddrTable remplit un pointeur vers une \_ structure IPADDRTABLE MIB avec des informations sur les adresses IP actuelles associées au système.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Gestion des adresses IP à l’aide de GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864874"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Gestion des adresses IP à l’aide de GetIpAddrTable

La fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) remplit un pointeur vers une structure [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) avec des informations sur les adresses IP actuelles associées au système.

**Pour utiliser GetIpAddrTable**

1.  Déclarez un pointeur vers un objet [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) appelé *PIPAddrTable* et un objet **DWORD** appelé *dwSize nul*. Ces variables sont passées en tant que paramètres à la fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Créez également une variable **DWORD** appelée *dwRetVal* (utilisée pour la vérification des erreurs).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Allouez de la mémoire pour la structure.
    > [!Note]  
    > La taille de *dwSize nul* n’est pas suffisante pour contenir les informations. Consultez l’étape suivante.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Effectuez un appel initial à [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) pour connaître la taille nécessaire dans la variable *dwSize nul* .
    > [!Note]  
    > Cet appel à la fonction est censé échouer et est utilisé pour s’assurer que la variable *dwSize nul* spécifie une taille suffisante pour contenir toutes les informations retournées à *pIPAddrTable*. Il s’agit d’un modèle de programmation commun pour les structures de données et les fonctions de ce type.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Effectuez un deuxième appel à [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) avec une vérification générale des erreurs et retournez sa valeur à la variable **DWORD** *dwRetVal* (pour une vérification des erreurs plus avancée).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Si l’appel a réussi, accédez aux données à partir de la structure de données *pIPAddrTable* .
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Libérez la mémoire allouée pour la structure *pIPAddrTable* .
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Les  objets DWORD *dwAddr* et *dwMask* sont retournés en tant que valeurs numériques dans l’ordre d’octet de l’hôte, et non dans l’ordre des octets du réseau. Ces valeurs ne sont pas des adresses IP en pointillés.

 

Étape suivante : [gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Étape précédente : [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
