---
title: Authentification, autorisation et gestion des comptes RADIUS
description: NPS prend entièrement en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS). Le protocole RADIUS est la norme de facto pour l’authentification des utilisateurs distants et il est documenté dans le document RFC 2865 et RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382332"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="6c8f7-104">Authentification, autorisation et gestion des comptes RADIUS</span><span class="sxs-lookup"><span data-stu-id="6c8f7-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="6c8f7-105">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="6c8f7-106">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="6c8f7-107">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="6c8f7-108">NPS prend entièrement en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="6c8f7-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="6c8f7-109">Le protocole RADIUS est la norme de facto pour l’authentification des utilisateurs distants et il est documenté dans le document [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) et [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="6c8f7-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="6c8f7-110">Authentification et autorisation RADIUS</span><span class="sxs-lookup"><span data-stu-id="6c8f7-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="6c8f7-111">Le diagramme suivant montre un client d’authentification (« utilisateur ») qui se connecte à un serveur d’accès réseau (NAS) via une connexion d’accès à distance, à l’aide de la protocole PPP (PPP).</span><span class="sxs-lookup"><span data-stu-id="6c8f7-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="6c8f7-112">Pour authentifier l’utilisateur, le NAS contacte un serveur distant exécutant NPS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="6c8f7-113">Le serveur NAS et le serveur NPS communiquent à l’aide du protocole RADIUS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![authentification des utilisateurs distants](images/ias01.png)

<span data-ttu-id="6c8f7-115">Un NAS fonctionne comme un client d’un serveur ou de serveurs qui prennent en charge le protocole RADIUS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="6c8f7-116">Les serveurs qui prennent en charge le protocole RADIUS sont généralement appelés serveurs RADIUS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="6c8f7-117">Le client RADIUS, autrement dit, le NAS, transmet des informations sur l’utilisateur aux serveurs RADIUS désignés, puis agit sur la réponse que les serveurs renvoient.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="6c8f7-118">La demande envoyée par le NAS au serveur RADIUS afin d’authentifier l’utilisateur est généralement appelée « demande d’authentification ».</span><span class="sxs-lookup"><span data-stu-id="6c8f7-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="6c8f7-119">Si un serveur RADIUS authentifie l’utilisateur avec succès, le serveur RADIUS retourne des informations de configuration au NAS afin qu’il puisse fournir un service réseau à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="6c8f7-120">Ces informations de configuration sont composées de « autorisations » et elles contiennent, entre autres, le type de service que le NAS peut fournir à l’utilisateur (par exemple, PPP ou Telnet).</span><span class="sxs-lookup"><span data-stu-id="6c8f7-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="6c8f7-121">Pendant que le serveur RADIUS traite la demande d’authentification, il peut effectuer des fonctions d’autorisation telles que la vérification du numéro de téléphone de l’utilisateur et la vérification de la présence ou non d’une session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="6c8f7-122">Le serveur RADIUS peut déterminer si l’utilisateur a déjà une session en cours en contactant un serveur d’État.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="6c8f7-123">Pour plus d’informations sur l’authentification et l’autorisation RADIUS, consultez [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span><span class="sxs-lookup"><span data-stu-id="6c8f7-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="6c8f7-124">Gestion des comptes RADIUS</span><span class="sxs-lookup"><span data-stu-id="6c8f7-124">RADIUS Accounting</span></span>

<span data-ttu-id="6c8f7-125">Le serveur RADIUS collecte également une variété d’informations envoyées par le NAS qui peuvent être utilisées pour la gestion des comptes et pour la création de rapports sur l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="6c8f7-126">Le client RADIUS envoie des informations aux serveurs RADIUS désignés quand l’utilisateur se connecte et se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="6c8f7-127">Le client RADIUS peut envoyer des informations d’utilisation supplémentaires sur une base périodique pendant que la session est en cours.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="6c8f7-128">Les demandes envoyées par le client au serveur pour enregistrer les informations d’ouverture/de fermeture de session et d’utilisation sont généralement appelées « demandes de gestion ».</span><span class="sxs-lookup"><span data-stu-id="6c8f7-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="6c8f7-129">Pour plus d’informations sur la gestion des comptes RADIUS, consultez [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="6c8f7-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="6c8f7-130">Proxy RADIUS</span><span class="sxs-lookup"><span data-stu-id="6c8f7-130">RADIUS Proxy</span></span>

<span data-ttu-id="6c8f7-131">Un serveur RADIUS peut agir en tant que client proxy pour d’autres serveurs RADIUS.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="6c8f7-132">Dans ce cas, le serveur RADIUS contacté par le NAS transmet la requête d’authentification ou de gestion des comptes à un autre serveur RADIUS qui effectue réellement l’authentification ou la tâche de gestion des comptes.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c8f7-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c8f7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c8f7-134">Service d’authentification Internet et serveur NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="6c8f7-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="6c8f7-135">Paquets de gestion de comptes RADIUS</span><span class="sxs-lookup"><span data-stu-id="6c8f7-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="6c8f7-136">Utilisation d’un serveur d’État</span><span class="sxs-lookup"><span data-stu-id="6c8f7-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 