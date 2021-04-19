---
description: La fonction GetInterfaceInfo remplit un pointeur vers une structure d’informations d' \_ interface IP \_ avec des informations sur les interfaces associées au système.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gestion des interfaces à l’aide de GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514419"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="7665f-103">Gestion des interfaces à l’aide de GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="7665f-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="7665f-104">La fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) remplit un pointeur vers une structure d’informations d' [**\_ interface \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) avec des informations sur les interfaces associées au système.</span><span class="sxs-lookup"><span data-stu-id="7665f-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="7665f-105">**Pour utiliser GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="7665f-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="7665f-106">Déclarez un pointeur vers un objet d' [**\_ \_ informations d’interface IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) appelé `pInfo` , et un objet **ULong** appelé `ulOutBufLen` .</span><span class="sxs-lookup"><span data-stu-id="7665f-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="7665f-107">Déclarez également un objet **DWORD** appelé `dwRetVal` (utilisé pour la vérification des erreurs).</span><span class="sxs-lookup"><span data-stu-id="7665f-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="7665f-108">Allouez de la mémoire pour les structures.</span><span class="sxs-lookup"><span data-stu-id="7665f-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="7665f-109">La taille de `ulOutBufLen` n’est pas suffisante pour contenir les informations.</span><span class="sxs-lookup"><span data-stu-id="7665f-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="7665f-110">Consultez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="7665f-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="7665f-111">Effectuez un appel initial à [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) pour connaître la taille nécessaire à la `ulOutBufLen` variable.</span><span class="sxs-lookup"><span data-stu-id="7665f-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="7665f-112">Cet appel à la fonction est censé échouer et est utilisé pour s’assurer que la `ulOutBufLen` variable spécifie une taille suffisante pour contenir toutes les informations retournées à `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="7665f-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="7665f-113">Il s’agit d’un modèle de programmation commun dans le programme d’assistance IP pour les structures de données et les fonctions de ce type.</span><span class="sxs-lookup"><span data-stu-id="7665f-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="7665f-114">Effectuez un deuxième appel à [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) avec une vérification d’erreur générale et retournez sa valeur à la variable **DWORD** `dwRetVal` (pour une vérification des erreurs plus avancée).</span><span class="sxs-lookup"><span data-stu-id="7665f-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="7665f-115">Si l’appel a réussi, accédez aux données de la `pInfo` structure de données.</span><span class="sxs-lookup"><span data-stu-id="7665f-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="7665f-116">Le% WS de la première ligne indique une chaîne étendue.</span><span class="sxs-lookup"><span data-stu-id="7665f-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="7665f-117">Cela est utilisé, car l’attribut **Name** de la structure de mappage d’index de la [**\_ carte \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` est **WCHAR**, qui est une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="7665f-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="7665f-118">Libérez la mémoire allouée pour la structure *pinfo* .</span><span class="sxs-lookup"><span data-stu-id="7665f-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="7665f-119">Étape suivante : [gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="7665f-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="7665f-120">Étape précédente : [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="7665f-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



