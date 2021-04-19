---
description: La fonction GetIpStatistics remplit un pointeur vers une \_ structure IPSTATS MIB avec des informations sur les statistiques IP actuelles associées au système.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Récupération d’informations à l’aide de GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544909"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="0daad-103">Récupération d’informations à l’aide de GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="0daad-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="0daad-104">La fonction [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) remplit un pointeur vers une structure [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) avec des informations sur les statistiques IP actuelles associées au système.</span><span class="sxs-lookup"><span data-stu-id="0daad-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="0daad-105">**Pour utiliser GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="0daad-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="0daad-106">Déclarez les variables nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0daad-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="0daad-107">Déclarez une variable **DWORD** `dwRetval` qui sera utilisée pour les appels de fonction de vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="0daad-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="0daad-108">Déclarez un pointeur vers une variable [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) appelée *pStats* et allouez de la mémoire pour la structure.</span><span class="sxs-lookup"><span data-stu-id="0daad-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="0daad-109">Vérifiez que la mémoire peut être allouée.</span><span class="sxs-lookup"><span data-stu-id="0daad-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="0daad-110">Appelez la fonction [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) avec le paramètre *pStats* pour récupérer les statistiques IP de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0daad-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="0daad-111">Recherchez les erreurs et retournez la valeur d’erreur dans la variable **DWORD** `dwRetval` .</span><span class="sxs-lookup"><span data-stu-id="0daad-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="0daad-112">Si une erreur se produit, la `dwRetval` variable peut être utilisée pour la vérification et la création de rapports d’erreurs plus vastes.</span><span class="sxs-lookup"><span data-stu-id="0daad-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="0daad-113">Si l’appel à [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) a réussi, imprimez une partie des données de la structure [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) vers laquelle pointe le paramètre *pStats* .</span><span class="sxs-lookup"><span data-stu-id="0daad-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="0daad-114">Libérez la mémoire allouée pour la structure [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) vers laquelle pointe le paramètre *pStats* .</span><span class="sxs-lookup"><span data-stu-id="0daad-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="0daad-115">Cette opération doit être effectuée une fois que l’application n’a plus besoin des données retournées par le paramètre *pStats* .</span><span class="sxs-lookup"><span data-stu-id="0daad-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="0daad-116">Étape suivante : [récupération d’informations à l’aide de GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="0daad-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="0daad-117">Étape précédente : [gestion des adresses IP à l’aide de AddIpAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="0daad-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 
