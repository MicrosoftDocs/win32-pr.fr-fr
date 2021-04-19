---
description: La fonction GetTcpStatistics remplit un pointeur vers une structure MIB \_ TCPSTATS avec des informations sur les statistiques de protocole TCP pour l’ordinateur local.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Récupération d’informations à l’aide de GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544908"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="970b1-103">Récupération d’informations à l’aide de GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="970b1-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="970b1-104">La fonction [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) remplit un pointeur vers une structure [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) avec des informations sur les statistiques de protocole TCP pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="970b1-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="970b1-105">**Pour utiliser GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="970b1-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="970b1-106">Déclarez les variables nécessaires.</span><span class="sxs-lookup"><span data-stu-id="970b1-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="970b1-107">Déclarez une variable **DWORD** `dwRetVal` qui sera utilisée pour les appels de fonction de vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="970b1-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="970b1-108">Déclarez un pointeur vers une variable [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) appelée *pTCPStats* et allouez de la mémoire pour la structure.</span><span class="sxs-lookup"><span data-stu-id="970b1-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="970b1-109">Vérifiez que la mémoire peut être allouée.</span><span class="sxs-lookup"><span data-stu-id="970b1-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="970b1-110">Appelez la fonction [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) avec le paramètre *pTCPStats* pour récupérer les statistiques TCP pour IPv4 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="970b1-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="970b1-111">Recherchez les erreurs et retournez la valeur d’erreur dans la variable **DWORD** `dwRetVal` .</span><span class="sxs-lookup"><span data-stu-id="970b1-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="970b1-112">Si une erreur se produit, la `dwRetVal` variable peut être utilisée pour la vérification et la création de rapports d’erreurs plus vastes.</span><span class="sxs-lookup"><span data-stu-id="970b1-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="970b1-113">Si l’appel a réussi, accédez aux données retournées dans le [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) désigné par le paramètre *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="970b1-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="970b1-114">Libérez la mémoire allouée pour la structure [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) vers laquelle pointe le paramètre *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="970b1-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="970b1-115">Cette opération doit être effectuée une fois que l’application n’a plus besoin des données retournées par le paramètre *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="970b1-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="970b1-116">Étape suivante : [récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="970b1-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="970b1-117">Étape précédente : [récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="970b1-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="970b1-118">Code source complet</span><span class="sxs-lookup"><span data-stu-id="970b1-118">Complete Source Code</span></span>

-   [<span data-ttu-id="970b1-119">Code source complet de l’application d’assistance IP</span><span class="sxs-lookup"><span data-stu-id="970b1-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 
