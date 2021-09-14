---
description: La fonction GetAdaptersInfo remplit un pointeur vers une structure d’informations d' \_ adaptateur IP \_ avec des informations sur les cartes réseau associées au système.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Gestion des cartes réseau à l’aide de GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094569"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Gestion des cartes réseau à l’aide de GetAdaptersInfo

La fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) remplit un pointeur vers une structure d’informations d' [**\_ adaptateur \_ IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) avec des informations sur les cartes réseau associées au système.

**Pour utiliser GetAdaptersInfo**

1.  Déclarez un pointeur vers une variable d' [**\_ \_ informations d’adaptateur IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) appelée *pAdapterInfo* et une variable **ULong** appelée *ulOutBufLen*. Ces variables sont passées en tant que paramètres à la fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Créez également une variable **DWORD** appelée *dwRetVal* (pour la vérification des erreurs).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Allouez de la mémoire pour les structures.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Effectuez un appel initial à [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) pour connaître la taille nécessaire dans la variable *ulOutBufLen* .
    > [!Note]  
    > Cet appel à la fonction est censé échouer et est utilisé pour s’assurer que la variable *ulOutBufLen* spécifie une taille suffisante pour contenir toutes les informations retournées à *pAdapterInfo*. Il s’agit d’un modèle de programmation commun pour les structures de données et les fonctions de ce type.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Effectuez un deuxième appel à [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), en passant *pAdapterInfo* et *ulOutBufLen* comme paramètres et en procédant à une vérification générale des erreurs. Retournez sa valeur à la  variable DWORD *dwRetVal* (pour une vérification des erreurs plus poussée).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Si l’appel a réussi, accédez à certaines des données de la structure *pAdapterInfo* .
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  Libérez la mémoire allouée pour la structure *pAdapterInfo* .
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Étape suivante : [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

Étape précédente : [récupération d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 



