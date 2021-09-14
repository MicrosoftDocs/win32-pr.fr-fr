---
description: Remplit un pointeur vers une structure d' \_ informations fixes avec des données relatives aux paramètres réseau actuels.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Récupération d’informations à l’aide de GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094541"
---
# <a name="retrieving-information-using-getnetworkparams"></a>Récupération d’informations à l’aide de GetNetworkParams

La fonction [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) remplit un pointeur vers une structure [**d' \_ informations fixes**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) avec des données sur les paramètres réseau actuels.

**Pour utiliser GetNetworkParams**

1.  Déclarez un pointeur vers un objet d' [**\_ informations fixes**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) appelé *PFixedInfo* et un objet **ULong** appelé *ulOutBufLen*. Ces variables sont passées en tant que paramètres à la fonction [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Créez également une  variable DWORD *dwRetVal* (utilisée pour la vérification des erreurs).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Allouez de la mémoire pour les structures.
    > [!Note]  
    > La taille de *ulOutBufLen* n’est pas suffisante pour contenir les informations. Consultez l’étape suivante.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Effectuez un appel initial à [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) pour obtenir la taille requise pour la variable *ulOutBufLen* .
    > [!Note]  
    > Cette fonction de fonction échoue et permet de s’assurer que la variable *ulOutBufLen* spécifie une taille suffisante pour contenir toutes les données retournées à *pFixedInfo*. Il s’agit d’un modèle de programmation commun pour les structures de données et les fonctions de ce type.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Effectuez un deuxième appel à [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) à l’aide de la vérification générale des erreurs et en retournant sa valeur à la variable **DWORD** *dwRetVal*; utilisé pour la vérification des erreurs plus avancée.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Si l’appel a réussi, accédez aux données à partir de la structure de données *pFixedInfo* .
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  Libérez la mémoire allouée pour la structure *pFixedInfo* .
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Étape suivante : [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

Étape précédente : [création d’une application d’assistance IP de base](creating-a-basic-ip-helper-application.md)

 

 



