---
title: Gérer les adresses IP avec AddIPAddress, DeleteIPAddress
description: La fonction AddIPAddress ajoute l’adresse IPv4 spécifiée à l’adaptateur spécifié.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543701"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="4f255-103">Gérer les adresses IP avec AddIPAddress, DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="4f255-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="4f255-104">La fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) ajoute l’adresse IPv4 spécifiée à l’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f255-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="4f255-105">La fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) supprime l’adresse IPv4 spécifiée de l’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f255-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="4f255-106">Ces fonctions peuvent être utilisées pour ajouter et supprimer des adresses IPv4 sur une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="4f255-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="4f255-107">Une adresse IPv4 ajoutée par la fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) n’est pas persistante.</span><span class="sxs-lookup"><span data-stu-id="4f255-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="4f255-108">L’adresse IPv4 existe uniquement tant que l’objet d’adaptateur existe.</span><span class="sxs-lookup"><span data-stu-id="4f255-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="4f255-109">Le redémarrage de l’ordinateur détruit l’adresse IPv4, tout comme la réinitialisation manuelle de la carte d’interface réseau (NIC).</span><span class="sxs-lookup"><span data-stu-id="4f255-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="4f255-110">Une fois que [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) a été appelé avec succès, DHCP est désactivé pour l’adresse IP qui a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4f255-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="4f255-111">Par conséquent, les fonctions telles que [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), qui requièrent l’activation de DHCP, ne seront pas fonctionnelles sur l’adresse IP ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4f255-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="4f255-112">La fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) peut être utilisée pour supprimer l’adresse IPv4 ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4f255-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="4f255-113">Les stratégies de groupe, les stratégies d’entreprise et autres restrictions sur le réseau peuvent empêcher l’exécution correcte de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="4f255-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="4f255-114">Assurez-vous que l’application dispose des autorisations réseau nécessaires avant d’essayer d’utiliser ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="4f255-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="4f255-115">**Pour utiliser AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="4f255-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="4f255-116">Déclarez les variables **ULong** nommées `NTEContext` et `NTEInstance` , toutes deux initialisées à zéro.</span><span class="sxs-lookup"><span data-stu-id="4f255-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="4f255-117">La `NTEContext` variable est le seul paramètre de la fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) ; pour supprimer l’adresse IP ajoutée, elle `NTEContext` doit être stockée et inchangée.</span><span class="sxs-lookup"><span data-stu-id="4f255-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="4f255-118">Déclarez les variables pour les structures IPAddr et IPMask nommées `iaIPAddress` et `iaIPMask` , respectivement.</span><span class="sxs-lookup"><span data-stu-id="4f255-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="4f255-119">Ces valeurs sont simplement des entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="4f255-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="4f255-120">Initialisez les `iaIPAddress` `iaIPMask` variables et à l’aide de la fonction [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .</span><span class="sxs-lookup"><span data-stu-id="4f255-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="4f255-121">Appelez la fonction [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) pour ajouter l’adresse IPv4.</span><span class="sxs-lookup"><span data-stu-id="4f255-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="4f255-122">Recherchez les erreurs et renvoyez la valeur d’erreur à la variable **DWORD** `dwRetVal` (pour une vérification des erreurs plus poussée).</span><span class="sxs-lookup"><span data-stu-id="4f255-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="4f255-123">Le troisième paramètre est l’index de l’adaptateur, qui peut être obtenu en appelant la fonction [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="4f255-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="4f255-124">Il est supposé que la variable retournée par cette fonction est nommée `pIPAddrTable` .</span><span class="sxs-lookup"><span data-stu-id="4f255-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="4f255-125">Pour obtenir de l’aide sur la fonction **GetIpAddrTable** , consultez Gestion de l' [adresse IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="4f255-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="4f255-126">**Pour utiliser DeleteIpAddress**</span><span class="sxs-lookup"><span data-stu-id="4f255-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="4f255-127">Appelez la fonction [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , en passant la `NTEContext` variable en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="4f255-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="4f255-128">Recherchez les erreurs et renvoyez la valeur d’erreur à la variable **DWORD** `dwRetVal` (pour une vérification des erreurs plus poussée).</span><span class="sxs-lookup"><span data-stu-id="4f255-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="4f255-129">Pour utiliser [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) doit d’abord être appelé pour recevoir le descripteur `NTEContext` .</span><span class="sxs-lookup"><span data-stu-id="4f255-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="4f255-130">La procédure précédente suppose que **AddIpAddress** a déjà été appelé quelque part dans le code et qu’il `NTEContext` a été enregistré et qu’il n’est pas endommagé.</span><span class="sxs-lookup"><span data-stu-id="4f255-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="4f255-131">Étape suivante : [récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="4f255-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="4f255-132">Étape précédente : [gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="4f255-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
