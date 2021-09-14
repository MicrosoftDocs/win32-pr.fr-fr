---
description: La fonction GetTcpStatistics remplit un pointeur vers une structure MIB \_ TCPSTATS avec des informations sur les statistiques de protocole TCP pour l’ordinateur local.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Récupération d’informations à l’aide de GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094537"
---
# <a name="retrieving-information-using-gettcpstatistics"></a>Récupération d’informations à l’aide de GetTcpStatistics

La fonction [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) remplit un pointeur vers une structure [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) avec des informations sur les statistiques de protocole TCP pour l’ordinateur local.

**Pour utiliser GetTcpStatistics**

1.  Déclarez les variables nécessaires.

    Déclarez une variable **DWORD** `dwRetVal` qui sera utilisée pour les appels de fonction de vérification des erreurs. Déclarez un pointeur vers une variable [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) appelée *pTCPStats* et allouez de la mémoire pour la structure. Vérifiez que la mémoire peut être allouée.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Appelez la fonction [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) avec le paramètre *pTCPStats* pour récupérer les statistiques TCP pour IPv4 sur l’ordinateur local. Recherchez les erreurs et retournez la valeur d’erreur dans la variable **DWORD** `dwRetVal` . Si une erreur se produit, la `dwRetVal` variable peut être utilisée pour la vérification et la création de rapports d’erreurs plus vastes.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Si l’appel a réussi, accédez aux données retournées dans le [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) désigné par le paramètre *pTCPStats* .
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Libérez la mémoire allouée pour la structure [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) vers laquelle pointe le paramètre *pTCPStats* . Cette opération doit être effectuée une fois que l’application n’a plus besoin des données retournées par le paramètre *pTCPStats* .
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Étape suivante : [récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)

Étape précédente : [récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Code source complet

-   [Code source complet de l’application d’assistance IP](complete-ip-helper-application-source-code.md)

 

 
