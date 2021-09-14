---
description: La fonction GetIpStatistics remplit un pointeur vers une \_ structure IPSTATS MIB avec des informations sur les statistiques IP actuelles associées au système.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Récupération d’informations à l’aide de GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094542"
---
# <a name="retrieving-information-using-getipstatistics"></a>Récupération d’informations à l’aide de GetIpStatistics

La fonction [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) remplit un pointeur vers une structure [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) avec des informations sur les statistiques IP actuelles associées au système.

**Pour utiliser GetIpStatistics**

1.  Déclarez les variables nécessaires.

    Déclarez une variable **DWORD** `dwRetval` qui sera utilisée pour les appels de fonction de vérification des erreurs. Déclarez un pointeur vers une variable [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) appelée *pStats* et allouez de la mémoire pour la structure. Vérifiez que la mémoire peut être allouée.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Appelez la fonction [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) avec le paramètre *pStats* pour récupérer les statistiques IP de l’ordinateur local. Recherchez les erreurs et retournez la valeur d’erreur dans la variable **DWORD** `dwRetval` . Si une erreur se produit, la `dwRetval` variable peut être utilisée pour la vérification et la création de rapports d’erreurs plus vastes.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Si l’appel à [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) a réussi, imprimez une partie des données de la structure [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) vers laquelle pointe le paramètre *pStats* .
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Libérez la mémoire allouée pour la structure [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) vers laquelle pointe le paramètre *pStats* . Cette opération doit être effectuée une fois que l’application n’a plus besoin des données retournées par le paramètre *pStats* .
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Étape suivante : [récupération d’informations à l’aide de GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Étape précédente : [gestion des adresses IP à l’aide de AddIpAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
