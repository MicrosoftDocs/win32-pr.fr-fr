---
description: 'Les fonctions de résolution de noms peuvent être regroupées en trois catégories : installation de service, requêtes client et application auxiliaire (avec macros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Résumé des fonctions de résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751397"
---
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="dd66b-103">Résumé des fonctions de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="dd66b-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="dd66b-104">Les fonctions de résolution de noms peuvent être regroupées en trois catégories : installation de service, requêtes client et application auxiliaire (avec macros).</span><span class="sxs-lookup"><span data-stu-id="dd66b-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="dd66b-105">Les sections qui suivent identifient les fonctions de chaque catégorie et décrivent brièvement leur utilisation prévue.</span><span class="sxs-lookup"><span data-stu-id="dd66b-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="dd66b-106">Les structures de données clés sont également décrites.</span><span class="sxs-lookup"><span data-stu-id="dd66b-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="dd66b-107">Installation du service</span><span class="sxs-lookup"><span data-stu-id="dd66b-107">Service Installation</span></span>

-   [<span data-ttu-id="dd66b-108">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="dd66b-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="dd66b-109">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="dd66b-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="dd66b-110">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="dd66b-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="dd66b-111">Quand la classe de service requise n’existe pas encore, une application utilise [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) pour installer une nouvelle classe de service en fournissant un nom de classe de service, un GUID pour l’identificateur de classe de service et une série de structures [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="dd66b-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="dd66b-112">Ces structures sont spécifiques à un espace de noms particulier et fournissent des valeurs communes telles que des numéros de port TCP recommandés ou des identificateurs SAP SAP.</span><span class="sxs-lookup"><span data-stu-id="dd66b-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="dd66b-113">Une classe de service peut être supprimée en appelant [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) et en fournissant le GUID correspondant à l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="dd66b-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="dd66b-114">Une fois qu’une classe de service existe, les instances spécifiques d’un service peuvent être installées ou supprimées par le biais de [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span><span class="sxs-lookup"><span data-stu-id="dd66b-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="dd66b-115">Cette fonction prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme paramètre d’entrée avec un code d’opération et des indicateurs d’opération.</span><span class="sxs-lookup"><span data-stu-id="dd66b-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="dd66b-116">Le code d’opération indique si le service est en cours d’installation ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="dd66b-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="dd66b-117">La structure **WSAQUERYSET** fournit toutes les informations pertinentes relatives au service, notamment l’identificateur de classe de service, le nom de service (pour cette instance), l’identificateur d’espace de noms applicable et les informations de protocole, ainsi qu’un ensemble d’adresses de transport sur lequel le service écoute.</span><span class="sxs-lookup"><span data-stu-id="dd66b-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="dd66b-118">Les services doivent appeler **WSASetService** lorsqu’ils s’initialisent pour annoncer leur présence dans les espaces de noms dynamiques.</span><span class="sxs-lookup"><span data-stu-id="dd66b-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="dd66b-119">Requête cliente</span><span class="sxs-lookup"><span data-stu-id="dd66b-119">Client Query</span></span>

-   [<span data-ttu-id="dd66b-120">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="dd66b-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="dd66b-121">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="dd66b-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="dd66b-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="dd66b-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="dd66b-123">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="dd66b-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="dd66b-124">La fonction [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) permet à une application de découvrir quels espaces de noms sont accessibles par le biais de fonctions de résolution de noms Winsock.</span><span class="sxs-lookup"><span data-stu-id="dd66b-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="dd66b-125">Elle permet également à une application de déterminer si un espace de noms donné est pris en charge par plusieurs fournisseurs d’espaces de noms, et de découvrir l’identificateur de fournisseur pour n’importe quel fournisseur d’espace de noms particulier.</span><span class="sxs-lookup"><span data-stu-id="dd66b-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="dd66b-126">À l’aide d’un identificateur de fournisseur, l’application peut limiter une opération de requête à un fournisseur d’espaces de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd66b-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="dd66b-127">Espace de noms Winsock : les opérations de requête impliquent une série d’appels : [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), suivis d’un ou plusieurs appels à [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) et se terminant par un appel à [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="dd66b-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="dd66b-128">**WSALookupServiceBegin** prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme entrée pour définir les paramètres de requête avec un jeu d’indicateurs pour fournir un contrôle supplémentaire sur l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="dd66b-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="dd66b-129">Elle retourne un handle de requête qui est utilisé dans les appels suivants à **WSALookupServiceNext** et **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="dd66b-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="dd66b-130">L’application appelle [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) pour obtenir les résultats de la requête, avec les résultats fournis dans une mémoire tampon [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="dd66b-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="dd66b-131">L’application continue d’appeler **WSALookupServiceNext** jusqu’à ce que le code d’erreur « wsa \_ E » \_ \_ soit retourné, indiquant que tous les résultats ont été récupérés.</span><span class="sxs-lookup"><span data-stu-id="dd66b-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="dd66b-132">La recherche est ensuite terminée par un appel à [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="dd66b-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="dd66b-133">La fonction **WSALookupServiceEnd** peut également être utilisée pour annuler un **WSALookupServiceNext** actuellement en attente en cas d’appel à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="dd66b-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="dd66b-134">Dans Windows Sockets 2, les codes d’erreur en conflit sont définis pour WSAENOMORE (10102) et WSA \_ E \_ \_ (10110).</span><span class="sxs-lookup"><span data-stu-id="dd66b-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="dd66b-135">Le code d’erreur WSAENOMORE sera supprimé dans une version ultérieure et seul le WSA \_ E ne \_ \_ sera pas conservé.</span><span class="sxs-lookup"><span data-stu-id="dd66b-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="dd66b-136">Pour Windows Sockets 2, toutefois, les applications doivent vérifier à la fois WSAENOMORE et WSA \_ E pour \_ \_ la compatibilité la plus étendue possible avec les fournisseurs d’espaces de noms qui utilisent l’un ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="dd66b-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="dd66b-137">Fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="dd66b-137">Helper Functions</span></span>

-   [<span data-ttu-id="dd66b-138">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="dd66b-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="dd66b-139">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="dd66b-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="dd66b-140">**WSAStringToAddress n'**</span><span class="sxs-lookup"><span data-stu-id="dd66b-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="dd66b-141">**WSAGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="dd66b-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="dd66b-142">Les fonctions d’assistance de résolution de noms incluent une fonction permettant de récupérer un nom de classe de service en fonction d’un identificateur de classe de service, une paire de fonctions utilisées pour traduire une adresse de transport entre une structure [**sockaddr**](sockaddr-2.md) et une représentation sous forme de chaîne ASCII, une fonction pour récupérer les informations de schéma de la classe de service pour une classe de service donnée et un ensemble de macros pour</span><span class="sxs-lookup"><span data-stu-id="dd66b-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="dd66b-143">Les macros suivantes de Winsock2. h facilitent le mappage entre les classes de service connues et les espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="dd66b-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="dd66b-144">Macro</span><span class="sxs-lookup"><span data-stu-id="dd66b-144">Macro</span></span>                                                                                                            | <span data-ttu-id="dd66b-145">Description</span><span class="sxs-lookup"><span data-stu-id="dd66b-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd66b-146">SVCID \_ TCP (port) SVCID \_ UDP (port)</span><span class="sxs-lookup"><span data-stu-id="dd66b-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="dd66b-147">SVCID \_ NetWare (type d’objet)</span><span class="sxs-lookup"><span data-stu-id="dd66b-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="dd66b-148">Avec un port pour TCP/IP ou UDP/IP ou le type d’objet dans le cas de NetWare, retourne le GUID (numéro de port dans l’ordre de l’ordinateur hôte).</span><span class="sxs-lookup"><span data-stu-id="dd66b-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="dd66b-149">\_SVCID \_ TCP (Guid) est-il \_ SVCID \_ UDP (Guid)</span><span class="sxs-lookup"><span data-stu-id="dd66b-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="dd66b-150">IS \_ SVCID \_ NetWare (Guid)</span><span class="sxs-lookup"><span data-stu-id="dd66b-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="dd66b-151">Retourne la **valeur true** si le GUID est dans la plage autorisée.</span><span class="sxs-lookup"><span data-stu-id="dd66b-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="dd66b-152">DÉFINIR \_ TCP \_ SVCID (Guid, port) définir \_ UDP \_ SVCID (Guid, port)</span><span class="sxs-lookup"><span data-stu-id="dd66b-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="dd66b-153">Initialise une structure GUID avec le GUID équivalent pour un numéro de port TCP ou UDP (le numéro de port doit être dans l’ordre de l’ordinateur hôte).</span><span class="sxs-lookup"><span data-stu-id="dd66b-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="dd66b-154">PORT \_ à partir du \_ \_ port SVCID TCP (Guid) \_ à partir de \_ SVCID \_ UDP (Guid)</span><span class="sxs-lookup"><span data-stu-id="dd66b-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="dd66b-155">SAPId \_ à partir de \_ SVCID \_ NetWare (Guid)</span><span class="sxs-lookup"><span data-stu-id="dd66b-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="dd66b-156">Retourne le port ou le type d’objet associé au GUID (numéro de port dans l’ordre de l’ordinateur hôte).</span><span class="sxs-lookup"><span data-stu-id="dd66b-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="dd66b-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd66b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd66b-158">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="dd66b-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="dd66b-159">**API getaddrinfoex**</span><span class="sxs-lookup"><span data-stu-id="dd66b-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="dd66b-160">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="dd66b-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="dd66b-161">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="dd66b-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="dd66b-162">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="dd66b-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="dd66b-163">Structures de données de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="dd66b-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="dd66b-164">Modèle de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="dd66b-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="dd66b-165">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="dd66b-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="dd66b-166">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="dd66b-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="dd66b-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="dd66b-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="dd66b-168">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="dd66b-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="dd66b-169">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="dd66b-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="dd66b-170">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="dd66b-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="dd66b-171">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="dd66b-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="dd66b-172">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="dd66b-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="dd66b-173">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="dd66b-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="dd66b-174">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="dd66b-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="dd66b-175">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="dd66b-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="dd66b-176">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="dd66b-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="dd66b-177">**WSANSCLASSINFO**</span><span class="sxs-lookup"><span data-stu-id="dd66b-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




