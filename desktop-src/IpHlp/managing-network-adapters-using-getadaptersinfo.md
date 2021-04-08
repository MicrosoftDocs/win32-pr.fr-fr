---
description: La fonction GetAdaptersInfo remplit un pointeur vers une structure d’informations d' \_ adaptateur IP \_ avec des informations sur les cartes réseau associées au système.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Gestion des cartes réseau à l’aide de GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034866"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="5b2f2-103">Gestion des cartes réseau à l’aide de GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="5b2f2-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="5b2f2-104">La fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) remplit un pointeur vers une structure d’informations d' [**\_ adaptateur \_ IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) avec des informations sur les cartes réseau associées au système.</span><span class="sxs-lookup"><span data-stu-id="5b2f2-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="5b2f2-105">**Pour utiliser GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="5b2f2-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="5b2f2-106">Déclarez un pointeur vers une variable d' [**\_ \_ informations d’adaptateur IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) appelée *pAdapterInfo* et une variable **ULong** appelée *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="5b2f2-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="5b2f2-107">Ces variables sont passées en tant que paramètres à la fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="5b2f2-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="5b2f2-108">Créez également une variable **DWORD** appelée *dwRetVal* (pour la vérification des erreurs).</span><span class="sxs-lookup"><span data-stu-id="5b2f2-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="5b2f2-109">Allouez de la mémoire pour les structures.</span><span class="sxs-lookup"><span data-stu-id="5b2f2-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="5b2f2-110">Effectuez un appel initial à [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) pour connaître la taille nécessaire dans la variable *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="5b2f2-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="5b2f2-111">Cet appel à la fonction est censé échouer et est utilisé pour s’assurer que la variable *ulOutBufLen* spécifie une taille suffisante pour contenir toutes les informations retournées à *pAdapterInfo*.</span><span class="sxs-lookup"><span data-stu-id="5b2f2-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="5b2f2-112">Il s’agit d’un modèle de programmation commun pour les structures de données et les fonctions de ce type.</span><span class="sxs-lookup"><span data-stu-id="5b2f2-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="5b2f2-113">Effectuez un deuxième appel à [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), en passant *pAdapterInfo* et *ulOutBufLen* comme paramètres et en procédant à une vérification générale des erreurs.</span><span class="sxs-lookup"><span data-stu-id="5b2f2-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="5b2f2-114">Retournez sa valeur à la  variable DWORD *dwRetVal* (pour une vérification des erreurs plus poussée).</span><span class="sxs-lookup"><span data-stu-id="5b2f2-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="5b2f2-115">Si l’appel a réussi, accédez à certaines des données de la structure *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="5b2f2-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
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

    

6.  <span data-ttu-id="5b2f2-116">Libérez la mémoire allouée pour la structure *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="5b2f2-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="5b2f2-117">Étape suivante : [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="5b2f2-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="5b2f2-118">Étape précédente : [récupération d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="5b2f2-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 



