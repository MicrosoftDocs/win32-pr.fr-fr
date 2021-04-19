---
title: Authentification mutuelle à l'aide de Kerberos
description: L’authentification mutuelle est une fonctionnalité de sécurité dans laquelle un processus client doit prouver son identité à un service, et le service doit prouver son identité au client, avant qu’un trafic d’application ne soit transmis via la connexion client/service.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, authentification mutuelle
- Active Directory, utilisation de, sécurité, authentification mutuelle
- sécurité AD
- sécurité AD, authentification mutuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "106518000"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="1f4e5-107">Authentification mutuelle à l'aide de Kerberos</span><span class="sxs-lookup"><span data-stu-id="1f4e5-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="1f4e5-108">L’authentification mutuelle est une fonctionnalité de sécurité dans laquelle un processus client doit prouver son identité à un service, et le service doit prouver son identité au client, avant qu’un trafic d’application ne soit transmis via la connexion client/service.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="1f4e5-109">Active Directory Domain Services et Windows assurent la prise en charge des noms de principal du service (SPN), qui sont un composant clé du mécanisme Kerberos par lequel un client authentifie un service.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="1f4e5-110">Un SPN est un nom unique qui identifie une instance d’un service et qui est associé au compte d’ouverture de session sous lequel l’instance de service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="1f4e5-111">Les composants d’un SPN sont tels qu’un client peut composer un SPN pour un service sans le compte d’ouverture de session du service.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="1f4e5-112">Cela permet au client de demander au service d’authentifier son compte même si le client n’a pas le nom du compte.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="1f4e5-113">Cette section comprend une vue d’ensemble des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1f4e5-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="1f4e5-114">Authentification mutuelle à l’aide de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="1f4e5-115">Composition d’un nom principal de service unique.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="1f4e5-116">Comment un programme d’installation de service inscrit des noms de principal du service sur l’objet de compte associé à une instance de service.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="1f4e5-117">Comment une application cliente utilise l’objet point de connexion de service (SCP) d’une instance de service dans Active Directory Domain Services pour récupérer des données à partir desquelles composer un SPN pour le service.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="1f4e5-118">Comment une application cliente utilise un SPN de service conjointement avec l’interface SSPI (Security Support Provider Interface) pour authentifier le service.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="1f4e5-119">Exemple de code pour une application cliente/service Windows Sockets qui utilise un SCP et un SSPI pour effectuer une authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="1f4e5-120">Exemple de code pour un client/service RPC qui effectue une authentification mutuelle à l’aide du service de noms RPC et de l’authentification RPC.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="1f4e5-121">Comment un service d’inscription et de résolution Windows Sockets (RnR) utilise des noms de principal du service (SPN) pour effectuer une authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="1f4e5-122">Cette section décrit l’utilisation de domaine Active Directory Service pour l’authentification mutuelle, en particulier l’objectif des points de connexion de service et des noms de principal du service dans l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="1f4e5-123">Il ne s’agit pas d’une description complète de l’utilisation de SSPI pour l’authentification mutuelle ou du support d’authentification et de sécurité disponible pour les applications RPC et Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="1f4e5-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="1f4e5-124">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="1f4e5-124">For more information, see:</span></span>

-   [<span data-ttu-id="1f4e5-125">Publication avec des points de connexion de service</span><span class="sxs-lookup"><span data-stu-id="1f4e5-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="1f4e5-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="1f4e5-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="1f4e5-127">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="1f4e5-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="1f4e5-128">RPC</span><span class="sxs-lookup"><span data-stu-id="1f4e5-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 