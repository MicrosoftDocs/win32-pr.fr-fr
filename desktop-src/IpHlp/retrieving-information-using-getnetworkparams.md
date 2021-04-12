---
description: Remplit un pointeur vers une structure d' \_ informations fixes avec des données relatives aux paramètres réseau actuels.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Récupération d’informations à l’aide de GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203222"
---
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="6813d-103">Récupération d’informations à l’aide de GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="6813d-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="6813d-104">La fonction [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) remplit un pointeur vers une structure [**d' \_ informations fixes**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) avec des données sur les paramètres réseau actuels.</span><span class="sxs-lookup"><span data-stu-id="6813d-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="6813d-105">**Pour utiliser GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="6813d-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="6813d-106">Déclarez un pointeur vers un objet d' [**\_ informations fixes**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) appelé *PFixedInfo* et un objet **ULong** appelé *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="6813d-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="6813d-107">Ces variables sont passées en tant que paramètres à la fonction [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="6813d-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="6813d-108">Créez également une  variable DWORD *dwRetVal* (utilisée pour la vérification des erreurs).</span><span class="sxs-lookup"><span data-stu-id="6813d-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="6813d-109">Allouez de la mémoire pour les structures.</span><span class="sxs-lookup"><span data-stu-id="6813d-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="6813d-110">La taille de *ulOutBufLen* n’est pas suffisante pour contenir les informations.</span><span class="sxs-lookup"><span data-stu-id="6813d-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="6813d-111">Consultez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="6813d-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="6813d-112">Effectuez un appel initial à [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) pour obtenir la taille requise pour la variable *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="6813d-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="6813d-113">Cette fonction de fonction échoue et permet de s’assurer que la variable *ulOutBufLen* spécifie une taille suffisante pour contenir toutes les données retournées à *pFixedInfo*.</span><span class="sxs-lookup"><span data-stu-id="6813d-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="6813d-114">Il s’agit d’un modèle de programmation commun pour les structures de données et les fonctions de ce type.</span><span class="sxs-lookup"><span data-stu-id="6813d-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="6813d-115">Effectuez un deuxième appel à [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) à l’aide de la vérification générale des erreurs et en retournant sa valeur à la variable **DWORD** *dwRetVal*; utilisé pour la vérification des erreurs plus avancée.</span><span class="sxs-lookup"><span data-stu-id="6813d-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="6813d-116">Si l’appel a réussi, accédez aux données à partir de la structure de données *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="6813d-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
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

    

6.  <span data-ttu-id="6813d-117">Libérez la mémoire allouée pour la structure *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="6813d-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="6813d-118">Étape suivante : [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="6813d-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="6813d-119">Étape précédente : [création d’une application d’assistance IP de base](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="6813d-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 



