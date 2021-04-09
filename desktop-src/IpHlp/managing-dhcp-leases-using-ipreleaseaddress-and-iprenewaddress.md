---
title: Gérer les baux DHCP avec IpReleaseAddress, IpRenewAddress
description: Les fonctions IpReleaseAddress et IpRenewAddress sont utilisées pour libérer et renouveler le bail actuel du protocole DHCP (Dynamic Host Configuration Protocol).
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862438"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="a24ee-103">Gérer les baux DHCP avec IpReleaseAddress, IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="a24ee-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="a24ee-104">Les fonctions [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) sont utilisées pour libérer et renouveler le bail actuel du protocole DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="a24ee-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="a24ee-105">La fonction **IpReleaseAddress** libère une adresse IPv4 précédemment obtenue via DHCP.</span><span class="sxs-lookup"><span data-stu-id="a24ee-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="a24ee-106">La fonction **IpRenewAddress** renouvelle un bail sur une adresse IPv4 précédemment obtenue via DHCP.</span><span class="sxs-lookup"><span data-stu-id="a24ee-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="a24ee-107">Il est courant d’utiliser ces deux fonctions ensemble, d’abord de libérer le bail avec un appel à **IpReleaseAddress**, puis de renouveler le bail avec un appel à la fonction **IpRenewAddress** .</span><span class="sxs-lookup"><span data-stu-id="a24ee-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="a24ee-108">Lorsqu’un client DHCP a précédemment obtenu un bail DHCP et que [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) n’est pas appelé avant la fonction [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , la demande du client DHCP est envoyée au serveur DHCP qui a émis le bail DHCP initial.</span><span class="sxs-lookup"><span data-stu-id="a24ee-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="a24ee-109">Ce serveur DHCP peut ne pas être disponible ou la demande DHCP peut échouer.</span><span class="sxs-lookup"><span data-stu-id="a24ee-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="a24ee-110">Lorsqu’un ordinateur hôte a déjà obtenu un bail DHCP et que **IpReleaseAddress** est appelé avant la fonction **IpRenewAddress** , le client DHCP libère d’abord l’adresse IP obtenue et envoie une requête de client DHCP pour une réponse de tout serveur DHCP disponible.</span><span class="sxs-lookup"><span data-stu-id="a24ee-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="a24ee-111">Les fonctions [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) et [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requièrent que DHCP soit activé pour s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="a24ee-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="a24ee-112">La fonction [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) prend un pointeur vers une structure de mappage d' [**\_ \_ index \_ d’adaptateurs IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) comme seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="a24ee-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="a24ee-113">Pour obtenir ce paramètre, appelez d’abord [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span><span class="sxs-lookup"><span data-stu-id="a24ee-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="a24ee-114">Pour obtenir de l’aide sur la fonction **GetInterfaceInfo** , consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a24ee-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="a24ee-115">**Pour utiliser IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="a24ee-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="a24ee-116">Obtenir un pointeur vers une structure de [**mappage d' \_ \_ index \_ d’adaptateurs IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) à l’aide de la fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="a24ee-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="a24ee-117">(Pour obtenir de l’aide sur la fonction GetInterfaceInfo, consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="a24ee-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="a24ee-118">Créez un  objet DWORD `dwRetVal` (utilisé pour la vérification des erreurs).</span><span class="sxs-lookup"><span data-stu-id="a24ee-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="a24ee-119">La variable retournée par **GetInterfaceInfo** est supposée être appelée `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="a24ee-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="a24ee-120">Si le protocole DHCP est activé, appelez la fonction [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , en passant la variable de mappage d’index de la [**\_ carte \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="a24ee-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="a24ee-121">Recherchez les erreurs générales et retournez sa valeur à la  variable DWORD `dwRetVal` (pour une vérification plus poussée des erreurs).</span><span class="sxs-lookup"><span data-stu-id="a24ee-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="a24ee-122">La fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retourne un paramètre qui peut être utilisé pour vérifier si le protocole DHCP est activé avant d’appeler ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="a24ee-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="a24ee-123">Pour obtenir de l’aide sur **GetAdaptersInfo**, consultez [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a24ee-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="a24ee-124">Il est courant d’utiliser ces deux fonctions ensemble, d’appeler la fonction [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , puis d’appeler la fonction [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , en passant la même structure que le paramètre aux deux fonctions.</span><span class="sxs-lookup"><span data-stu-id="a24ee-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="a24ee-125">La procédure suivante suppose que les fonctions ne sont pas utilisées ensemble ; Toutefois, si les fonctions sont utilisées ensemble, ignorez l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a24ee-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="a24ee-126">**Pour utiliser IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="a24ee-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="a24ee-127">Obtenir un pointeur vers une structure de [**mappage d' \_ \_ index \_ d’adaptateurs IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) à l’aide de la fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="a24ee-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="a24ee-128">(Pour obtenir de l’aide sur la fonction **GetInterfaceInfo** , consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="a24ee-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="a24ee-129">Déclarez un objet **DWORD** `dwRetVal` (utilisé pour la vérification des erreurs) si cette variable n’a pas été déclarée.</span><span class="sxs-lookup"><span data-stu-id="a24ee-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="a24ee-130">La variable retournée par **GetInterfaceInfo** est supposée être appelée `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="a24ee-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="a24ee-131">Appelez la fonction [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , en passant la variable de mappage d’index de la [**\_ carte \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="a24ee-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="a24ee-132">Recherchez les erreurs générales et retournez sa valeur à la  variable DWORD `dwRetVal` (pour une vérification plus poussée des erreurs).</span><span class="sxs-lookup"><span data-stu-id="a24ee-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="a24ee-133">Étape suivante : [gestion des adresses IP à l’aide de AddIpAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="a24ee-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="a24ee-134">Étape précédente : [gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="a24ee-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



