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
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="e3578-103">Gestion des adresses IP à l’aide de GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="e3578-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="e3578-104">La fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) remplit un pointeur vers une structure [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) avec des informations sur les adresses IP actuelles associées au système.</span><span class="sxs-lookup"><span data-stu-id="e3578-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="e3578-105">**Pour utiliser GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="e3578-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="e3578-106">Déclarez un pointeur vers un objet [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) appelé *PIPAddrTable* et un objet **DWORD** appelé *dwSize nul*.</span><span class="sxs-lookup"><span data-stu-id="e3578-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="e3578-107">Ces variables sont passées en tant que paramètres à la fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="e3578-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="e3578-108">Créez également une variable **DWORD** appelée *dwRetVal* (utilisée pour la vérification des erreurs).</span><span class="sxs-lookup"><span data-stu-id="e3578-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="e3578-109">Allouez de la mémoire pour la structure.</span><span class="sxs-lookup"><span data-stu-id="e3578-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="e3578-110">La taille de *dwSize nul* n’est pas suffisante pour contenir les informations.</span><span class="sxs-lookup"><span data-stu-id="e3578-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="e3578-111">Consultez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="e3578-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="e3578-112">Effectuez un appel initial à [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) pour connaître la taille nécessaire dans la variable *dwSize nul* .</span><span class="sxs-lookup"><span data-stu-id="e3578-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="e3578-113">Cet appel à la fonction est censé échouer et est utilisé pour s’assurer que la variable *dwSize nul* spécifie une taille suffisante pour contenir toutes les informations retournées à *pIPAddrTable*.</span><span class="sxs-lookup"><span data-stu-id="e3578-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="e3578-114">Il s’agit d’un modèle de programmation commun pour les structures de données et les fonctions de ce type.</span><span class="sxs-lookup"><span data-stu-id="e3578-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="e3578-115">Effectuez un deuxième appel à [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) avec une vérification générale des erreurs et retournez sa valeur à la variable **DWORD** *dwRetVal* (pour une vérification des erreurs plus avancée).</span><span class="sxs-lookup"><span data-stu-id="e3578-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="e3578-116">Si l’appel a réussi, accédez aux données à partir de la structure de données *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="e3578-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="e3578-117">Libérez la mémoire allouée pour la structure *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="e3578-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="e3578-118">Les  objets DWORD *dwAddr* et *dwMask* sont retournés en tant que valeurs numériques dans l’ordre d’octet de l’hôte, et non dans l’ordre des octets du réseau.</span><span class="sxs-lookup"><span data-stu-id="e3578-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="e3578-119">Ces valeurs ne sont pas des adresses IP en pointillés.</span><span class="sxs-lookup"><span data-stu-id="e3578-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="e3578-120">Étape suivante : [gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="e3578-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="e3578-121">Étape précédente : [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="e3578-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
