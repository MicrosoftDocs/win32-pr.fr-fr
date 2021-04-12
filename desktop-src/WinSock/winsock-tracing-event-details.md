---
description: Détails du suivi d’événements réseau Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Détails du suivi d’événements réseau Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204123"
---
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="b1769-103">Détails du suivi d’événements réseau Winsock</span><span class="sxs-lookup"><span data-stu-id="b1769-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="b1769-104">Les informations suivantes décrivent chacun des événements réseau Winsock qui peuvent être suivis et détaillent les paramètres et les informations qui sont journalisés.</span><span class="sxs-lookup"><span data-stu-id="b1769-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="b1769-105">Création de socket</span><span class="sxs-lookup"><span data-stu-id="b1769-105">Socket Creation</span></span>

<span data-ttu-id="b1769-106">ID d’événement = 1</span><span class="sxs-lookup"><span data-stu-id="b1769-106">Event ID = 1</span></span>

<span data-ttu-id="b1769-107">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-107">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-108">Les événements Winsock suivants sont suivis pour la création de Sockets :</span><span class="sxs-lookup"><span data-stu-id="b1769-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="b1769-109">Handles de socket créés par des appels aux fonctions [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="b1769-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="b1769-110">Handles de socket acceptés sur les sockets d’écoute.</span><span class="sxs-lookup"><span data-stu-id="b1769-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="b1769-111">Handles de socket créés par des appels à la fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="b1769-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="b1769-112">Les handles de socket réutilisés par les appels aux fonctions [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) ou [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .</span><span class="sxs-lookup"><span data-stu-id="b1769-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="b1769-113">Les paramètres suivants sont enregistrés pour un événement de création de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="b1769-114">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="b1769-115">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="b1769-117">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="b1769-119">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span><span class="sxs-lookup"><span data-stu-id="b1769-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="b1769-121">Type du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="b1769-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>No</span><span class="sxs-lookup"><span data-stu-id="b1769-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="b1769-123">Protocole du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="b1769-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span><span class="sxs-lookup"><span data-stu-id="b1769-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="b1769-125">ID de processus en mode utilisateur qui a créé le Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="b1769-126">Liaison de socket</span><span class="sxs-lookup"><span data-stu-id="b1769-126">Socket Bind</span></span>

<span data-ttu-id="b1769-127">ID d’événement = 2 (IPv4), ID d’événement = 3 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="b1769-128">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-128">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-129">Les événements Winsock suivants sont suivis pour une opération de liaison :</span><span class="sxs-lookup"><span data-stu-id="b1769-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="b1769-130">Liaison implicite ou explicite d’un handle de Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="b1769-131">Les paramètres suivants sont enregistrés pour un événement de liaison :</span><span class="sxs-lookup"><span data-stu-id="b1769-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="b1769-132">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-132">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-133">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-135">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-137">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="b1769-139">Adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="b1769-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="b1769-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="b1769-141">Numéro de port de l’adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="b1769-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="b1769-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Statu</span><span class="sxs-lookup"><span data-stu-id="b1769-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="b1769-143">État ou code d’erreur retourné pour l’opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="b1769-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="b1769-144">Échec de la liaison</span><span class="sxs-lookup"><span data-stu-id="b1769-144">Failed Bind</span></span>

<span data-ttu-id="b1769-145">ID d’événement = 40</span><span class="sxs-lookup"><span data-stu-id="b1769-145">Event ID = 40</span></span>

<span data-ttu-id="b1769-146">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-146">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-147">Les événements Winsock suivants sont suivis pour une opération de liaison qui a échoué :</span><span class="sxs-lookup"><span data-stu-id="b1769-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="b1769-148">Liaison implicite ou explicite d’un handle de socket qui échoue.</span><span class="sxs-lookup"><span data-stu-id="b1769-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="b1769-149">Les paramètres suivants sont enregistrés pour un événement de liaison qui a échoué :</span><span class="sxs-lookup"><span data-stu-id="b1769-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="b1769-150">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-150">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-151">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-153">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-155">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-157">Code d’erreur retourné pour l’opération de liaison qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="b1769-158">Connexion de socket</span><span class="sxs-lookup"><span data-stu-id="b1769-158">Socket Connect</span></span>

<span data-ttu-id="b1769-159">ID d’événement = 4 (IPv4), ID d’événement = 5 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="b1769-160">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-160">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-161">Les événements Winsock suivants sont suivis pour une demande d’opération de connexion (appel à la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ) :</span><span class="sxs-lookup"><span data-stu-id="b1769-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="b1769-162">Connexion d’un socket à une destination pour un socket orienté connexion ou sans connexion.</span><span class="sxs-lookup"><span data-stu-id="b1769-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="b1769-163">Les paramètres suivants sont enregistrés pour un événement de connexion :</span><span class="sxs-lookup"><span data-stu-id="b1769-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="b1769-164">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-164">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-165">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-167">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-169">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="b1769-171">Adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="b1769-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="b1769-173">Numéro de port de l’adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="b1769-174">Connexion terminée</span><span class="sxs-lookup"><span data-stu-id="b1769-174">Connect Completed</span></span>

<span data-ttu-id="b1769-175">ID d’événement = 6</span><span class="sxs-lookup"><span data-stu-id="b1769-175">Event ID = 6</span></span>

<span data-ttu-id="b1769-176">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-176">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-177">Les événements Winsock suivants sont suivis pour une connexion terminée :</span><span class="sxs-lookup"><span data-stu-id="b1769-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="b1769-178">L’opération de connexion est terminée.</span><span class="sxs-lookup"><span data-stu-id="b1769-178">The connect operation is completed.</span></span>

<span data-ttu-id="b1769-179">Les paramètres suivants sont enregistrés pour un événement Connect terminé :</span><span class="sxs-lookup"><span data-stu-id="b1769-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="b1769-180">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-180">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-181">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-183">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-185">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-187">Code d’erreur retourné pour l’opération de connexion.</span><span class="sxs-lookup"><span data-stu-id="b1769-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="b1769-188">Abandon AFD-Initiated</span><span class="sxs-lookup"><span data-stu-id="b1769-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="b1769-189">ID d’événement = 7</span><span class="sxs-lookup"><span data-stu-id="b1769-189">Event ID = 7</span></span>

<span data-ttu-id="b1769-190">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-190">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-191">Les événements Winsock suivants sont suivis pour les abandons initiés par Winsock ou les opérations d’annulation :</span><span class="sxs-lookup"><span data-stu-id="b1769-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="b1769-192">Abandon en raison de données de réception non lues mises en mémoire tampon après la fermeture.</span><span class="sxs-lookup"><span data-stu-id="b1769-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="b1769-193">Abandon après un appel à la fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) avec le paramètre *How* défini sur Receive SD \_ et un appel à la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) avec received Data Pending.</span><span class="sxs-lookup"><span data-stu-id="b1769-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="b1769-194">Abandon après l’échec d’une tentative de vidage du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b1769-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="b1769-195">Une instruction Abort après une erreur Winsock interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b1769-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="b1769-196">Abandon en raison d’une connexion avec des erreurs et que l’application a précédemment demandé que la connexion soit abandonnée dans certaines circonstances.</span><span class="sxs-lookup"><span data-stu-id="b1769-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="b1769-197">Il peut s’agir, par exemple, d’une application qui a défini \_ un délai d’expiration égal à zéro et dont les données ne sont toujours pas acquittées sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="b1769-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="b1769-198">Abandon sur une connexion qui n’est pas entièrement associée au point de terminaison acceptant.</span><span class="sxs-lookup"><span data-stu-id="b1769-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="b1769-199">Abandon d’un appel à la fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ou [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .</span><span class="sxs-lookup"><span data-stu-id="b1769-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="b1769-200">Abandon en raison d’une opération de réception ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="b1769-201">Abandon en raison d’un événement de Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="b1769-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="b1769-202">Abandon en raison d’une demande de vidage ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="b1769-203">Abandon en raison d’une demande de réception de données expédiées ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="b1769-204">Abandon en raison d’un échec de demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="b1769-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="b1769-205">Abandon suite à l’annulation de la demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="b1769-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="b1769-206">Abandon en raison d’un annulé appelé à la fonction [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .</span><span class="sxs-lookup"><span data-stu-id="b1769-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="b1769-207">Les paramètres suivants sont journalisés pour une opération d’annulation ou d’annulation initiée par Winsock :</span><span class="sxs-lookup"><span data-stu-id="b1769-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="b1769-208">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-208">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-209">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-211">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-213">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Donc</span><span class="sxs-lookup"><span data-stu-id="b1769-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="b1769-215">Raison de l’opération d’abandon ou d’annulation.</span><span class="sxs-lookup"><span data-stu-id="b1769-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="b1769-216">Abandon Transport-Initiated</span><span class="sxs-lookup"><span data-stu-id="b1769-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="b1769-217">ID d’événement = 8</span><span class="sxs-lookup"><span data-stu-id="b1769-217">Event ID = 8</span></span>

<span data-ttu-id="b1769-218">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-218">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-219">Les événements Winsock suivants sont suivis pour les opérations d’annulation ou d’annulation initiées par le transport :</span><span class="sxs-lookup"><span data-stu-id="b1769-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="b1769-220">Réinitialisation indiquée par le transport.</span><span class="sxs-lookup"><span data-stu-id="b1769-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="b1769-221">Les paramètres suivants sont journalisés pour une opération d’annulation ou d’annulation initiée par Winsock :</span><span class="sxs-lookup"><span data-stu-id="b1769-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="b1769-222">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-222">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-223">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-225">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-227">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Donc</span><span class="sxs-lookup"><span data-stu-id="b1769-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="b1769-229">Raison de l’opération d’abandon ou d’annulation.</span><span class="sxs-lookup"><span data-stu-id="b1769-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="b1769-230">Échec de la demande d’envoi</span><span class="sxs-lookup"><span data-stu-id="b1769-230">Failed Send Request</span></span>

<span data-ttu-id="b1769-231">ID d’événement = 9</span><span class="sxs-lookup"><span data-stu-id="b1769-231">Event ID = 9</span></span>

<span data-ttu-id="b1769-232">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-232">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-233">Les événements Winsock suivants sont suivis pour détecter des erreurs lors des demandes [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :</span><span class="sxs-lookup"><span data-stu-id="b1769-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="b1769-234">Erreurs retournées en cas d’échec d' [**envoi**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou de demandes [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) .</span><span class="sxs-lookup"><span data-stu-id="b1769-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="b1769-235">Les paramètres suivants sont enregistrés pour les demandes d’envoi qui génèrent une erreur :</span><span class="sxs-lookup"><span data-stu-id="b1769-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="b1769-236">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-236">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-237">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-239">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-241">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-243">Code d’erreur retourné pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1769-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="b1769-244">Échec de la requête WsaSendMsg</span><span class="sxs-lookup"><span data-stu-id="b1769-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="b1769-245">ID d’événement = 10</span><span class="sxs-lookup"><span data-stu-id="b1769-245">Event ID = 10</span></span>

<span data-ttu-id="b1769-246">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-246">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-247">Les événements Winsock suivants sont suivis pour détecter les erreurs sur les demandes [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="b1769-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="b1769-248">Erreurs renvoyées lors des demandes [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="b1769-249">Les paramètres suivants sont enregistrés pour les demandes d’envoi qui génèrent une erreur :</span><span class="sxs-lookup"><span data-stu-id="b1769-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="b1769-250">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-250">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-251">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-253">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-255">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-257">Code d’erreur retourné pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1769-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="b1769-258">Échec de la demande de réception</span><span class="sxs-lookup"><span data-stu-id="b1769-258">Failed Recv Request</span></span>

<span data-ttu-id="b1769-259">ID d’événement = 11</span><span class="sxs-lookup"><span data-stu-id="b1769-259">Event ID = 11</span></span>

<span data-ttu-id="b1769-260">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-260">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-261">Les événements Winsock suivants sont suivis pour détecter les erreurs sur les demandes [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)ou [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :</span><span class="sxs-lookup"><span data-stu-id="b1769-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="b1769-262">Erreurs renvoyées lors des demandes de réception ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="b1769-263">Les paramètres suivants sont enregistrés pour les demandes d’envoi qui génèrent une erreur :</span><span class="sxs-lookup"><span data-stu-id="b1769-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="b1769-264">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-264">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-265">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-267">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-269">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-271">Code d’erreur retourné pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1769-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="b1769-272">Échec de la demande recvfrom</span><span class="sxs-lookup"><span data-stu-id="b1769-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="b1769-273">ID d’événement = 12</span><span class="sxs-lookup"><span data-stu-id="b1769-273">Event ID = 12</span></span>

<span data-ttu-id="b1769-274">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-274">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-275">Les événements Winsock suivants sont suivis pour détecter les erreurs sur les demandes [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :</span><span class="sxs-lookup"><span data-stu-id="b1769-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="b1769-276">Erreurs retournées en cas d’échec de demandes [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="b1769-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="b1769-277">Les paramètres suivants sont journalisés pour une demande [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) qui génère une erreur :</span><span class="sxs-lookup"><span data-stu-id="b1769-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="b1769-278">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-278">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-279">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-281">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-283">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-285">Code d’erreur retourné pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1769-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="b1769-286">Fermeture du socket</span><span class="sxs-lookup"><span data-stu-id="b1769-286">Socket Close</span></span>

<span data-ttu-id="b1769-287">ID d’événement = 13</span><span class="sxs-lookup"><span data-stu-id="b1769-287">Event ID = 13</span></span>

<span data-ttu-id="b1769-288">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-288">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-289">Les événements Winsock suivants sont suivis pour les opérations de fermeture de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="b1769-290">Un handle de socket est fermé.</span><span class="sxs-lookup"><span data-stu-id="b1769-290">A socket handle is closed.</span></span>

<span data-ttu-id="b1769-291">Les paramètres suivants sont enregistrés pour un événement de fermeture de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="b1769-292">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-292">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-293">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-295">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-297">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-299">Valeur de retour de l’opération de fermeture du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="b1769-300">Nettoyage de socket</span><span class="sxs-lookup"><span data-stu-id="b1769-300">Socket Cleanup</span></span>

<span data-ttu-id="b1769-301">ID d’événement = 14</span><span class="sxs-lookup"><span data-stu-id="b1769-301">Event ID = 14</span></span>

<span data-ttu-id="b1769-302">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-302">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-303">Les événements Winsock suivants sont suivis pour les opérations de nettoyage de socket (arrêt) :</span><span class="sxs-lookup"><span data-stu-id="b1769-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="b1769-304">La fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) est appelée sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="b1769-305">Le transport indique une déconnexion normale qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="b1769-306">Les paramètres suivants sont enregistrés pour un événement de nettoyage de socket (arrêt) ou de fermeture de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="b1769-307">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-307">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-308">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-310">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-312">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-314">Valeur de retour pour l’opération de nettoyage de socket (arrêt).</span><span class="sxs-lookup"><span data-stu-id="b1769-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="b1769-315">Accepter le socket</span><span class="sxs-lookup"><span data-stu-id="b1769-315">Socket Accept</span></span>

<span data-ttu-id="b1769-316">ID d’événement = 15 (IPv4), ID d’événement = 16 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="b1769-317">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-317">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-318">Les événements Winsock suivants sont suivis pour une demande [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) de la fonction :</span><span class="sxs-lookup"><span data-stu-id="b1769-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="b1769-319">Demande de fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) sur un handle de Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="b1769-320">Les paramètres suivants sont enregistrés pour un événement Accept :</span><span class="sxs-lookup"><span data-stu-id="b1769-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="b1769-321">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-321">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-322">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-324">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-326">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="b1769-328">Adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="b1769-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="b1769-330">Numéro de port de l’adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="b1769-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Statu</span><span class="sxs-lookup"><span data-stu-id="b1769-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="b1769-332">État ou code d’erreur retourné pour l’opération d’acceptation.</span><span class="sxs-lookup"><span data-stu-id="b1769-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="b1769-333">Échec de l’acceptation</span><span class="sxs-lookup"><span data-stu-id="b1769-333">Accept Failed</span></span>

<span data-ttu-id="b1769-334">ID d’événement = 17</span><span class="sxs-lookup"><span data-stu-id="b1769-334">Event ID = 17</span></span>

<span data-ttu-id="b1769-335">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="b1769-335">Level = 4 (Information)</span></span>

<span data-ttu-id="b1769-336">Les événements Winsock suivants sont suivis pour une opération d’acceptation ayant échoué :</span><span class="sxs-lookup"><span data-stu-id="b1769-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="b1769-337">Une demande [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) sur un handle de socket qui échoue.</span><span class="sxs-lookup"><span data-stu-id="b1769-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="b1769-338">Les paramètres suivants sont enregistrés pour un événement d’acceptation ayant échoué :</span><span class="sxs-lookup"><span data-stu-id="b1769-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="b1769-339">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-339">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-340">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-342">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-344">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-346">Code d’erreur retourné pour l’opération d’acceptation ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b1769-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="b1769-347">Envoi publié</span><span class="sxs-lookup"><span data-stu-id="b1769-347">Send Posted</span></span>

<span data-ttu-id="b1769-348">ID d’événement = 18</span><span class="sxs-lookup"><span data-stu-id="b1769-348">Event ID = 18</span></span>

<span data-ttu-id="b1769-349">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-350">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-351">Les événements Winsock suivants sont suivis pour les opérations de publication de tampons d’envoi et de réception de Sockets :</span><span class="sxs-lookup"><span data-stu-id="b1769-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="b1769-352">Une application publie un envoi.</span><span class="sxs-lookup"><span data-stu-id="b1769-352">An application posts a send.</span></span>
-   <span data-ttu-id="b1769-353">Une opération d’envoi se termine par Winsock.</span><span class="sxs-lookup"><span data-stu-id="b1769-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="b1769-354">Les paramètres suivants sont journalisés pour les opérations d’envoi de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="b1769-355">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-356">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-358">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="b1769-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-360">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="b1769-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="b1769-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="b1769-362">Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="b1769-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="b1769-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-364">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="b1769-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-366">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-366">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-367">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-369">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-369">The length of the buffer.</span></span> <span data-ttu-id="b1769-370">Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="b1769-371">Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="b1769-372">Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="b1769-373">Réception publiée</span><span class="sxs-lookup"><span data-stu-id="b1769-373">Receive Posted</span></span>

<span data-ttu-id="b1769-374">ID d’événement = 19</span><span class="sxs-lookup"><span data-stu-id="b1769-374">Event ID = 19</span></span>

<span data-ttu-id="b1769-375">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-376">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-377">Les événements Winsock suivants sont suivis pour les opérations de publication de tampon de réception de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="b1769-378">Une application publie une réception.</span><span class="sxs-lookup"><span data-stu-id="b1769-378">An application posts a receive.</span></span>
-   <span data-ttu-id="b1769-379">Une opération de réception se termine par Winsock.</span><span class="sxs-lookup"><span data-stu-id="b1769-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="b1769-380">Les paramètres suivants sont journalisés pour les opérations de réception de socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="b1769-381">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-382">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-384">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="b1769-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-386">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="b1769-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="b1769-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="b1769-388">Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="b1769-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="b1769-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-390">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="b1769-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-392">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-392">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-393">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-395">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-395">The length of the buffer.</span></span> <span data-ttu-id="b1769-396">Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="b1769-397">Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="b1769-398">Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="b1769-399">RecvFrom Posté</span><span class="sxs-lookup"><span data-stu-id="b1769-399">RecvFrom Posted</span></span>

<span data-ttu-id="b1769-400">ID d’événement = 20</span><span class="sxs-lookup"><span data-stu-id="b1769-400">Event ID = 20</span></span>

<span data-ttu-id="b1769-401">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-402">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-403">Les événements Winsock suivants sont suivis pour une opération de publication de tampon [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) sur un socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="b1769-404">Une application publie une opération recevoir à partir de.</span><span class="sxs-lookup"><span data-stu-id="b1769-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="b1769-405">Les paramètres suivants sont journalisés pour l’opération recvfrom :</span><span class="sxs-lookup"><span data-stu-id="b1769-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="b1769-406">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-407">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-409">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="b1769-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-411">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="b1769-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="b1769-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="b1769-413">Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="b1769-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="b1769-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-415">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="b1769-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-417">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-417">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-418">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-420">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-420">The length of the buffer.</span></span> <span data-ttu-id="b1769-421">Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="b1769-422">Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="b1769-423">Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="b1769-424">SendTo envoyé</span><span class="sxs-lookup"><span data-stu-id="b1769-424">SendTo Posted</span></span>

<span data-ttu-id="b1769-425">ID d’événement = 21 (IPv4), ID d’événement = 22 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="b1769-426">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-427">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-428">Les événements Winsock suivants sont suivis pour une opération de publication de mémoire tampon [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) sur un socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="b1769-429">Une application publie un envoi à partir de.</span><span class="sxs-lookup"><span data-stu-id="b1769-429">An application posts a send from.</span></span>

<span data-ttu-id="b1769-430">Les paramètres suivants sont enregistrés pour l’opération [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) :</span><span class="sxs-lookup"><span data-stu-id="b1769-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="b1769-431">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-432">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-434">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="b1769-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-436">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="b1769-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="b1769-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="b1769-438">Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="b1769-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="b1769-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-440">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="b1769-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-442">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-442">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-443">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-445">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-445">The length of the buffer.</span></span> <span data-ttu-id="b1769-446">Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="b1769-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="b1769-448">Adresse IP distante du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="b1769-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="b1769-450">Numéro de port IP distant du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="b1769-451">Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="b1769-452">Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="b1769-453">Réception terminée</span><span class="sxs-lookup"><span data-stu-id="b1769-453">Recv Completed</span></span>

<span data-ttu-id="b1769-454">ID d’événement = 23</span><span class="sxs-lookup"><span data-stu-id="b1769-454">Event ID = 23</span></span>

<span data-ttu-id="b1769-455">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-456">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-457">Les événements Winsock suivants sont suivis pour les opérations de réception de socket terminées :</span><span class="sxs-lookup"><span data-stu-id="b1769-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="b1769-458">Une opération d’envoi se termine au transport.</span><span class="sxs-lookup"><span data-stu-id="b1769-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="b1769-459">Une opération de réception se termine au transport.</span><span class="sxs-lookup"><span data-stu-id="b1769-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="b1769-460">Les paramètres suivants sont enregistrés pour une opération d’envoi terminée ou de réception terminée :</span><span class="sxs-lookup"><span data-stu-id="b1769-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="b1769-461">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-462">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-464">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="b1769-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-466">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="b1769-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-468">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-468">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-469">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="b1769-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-471">Longueur de la mémoire tampon d’octets reçus.</span><span class="sxs-lookup"><span data-stu-id="b1769-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="b1769-472">Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets reçus dans toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="b1769-473">Envoi terminé</span><span class="sxs-lookup"><span data-stu-id="b1769-473">Send Completed</span></span>

<span data-ttu-id="b1769-474">ID d’événement = 24</span><span class="sxs-lookup"><span data-stu-id="b1769-474">Event ID = 24</span></span>

<span data-ttu-id="b1769-475">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-476">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-477">Les événements Winsock suivants sont suivis pour les opérations d’envoi de socket terminées :</span><span class="sxs-lookup"><span data-stu-id="b1769-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="b1769-478">Une opération d’envoi se termine au transport.</span><span class="sxs-lookup"><span data-stu-id="b1769-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="b1769-479">Les paramètres suivants sont enregistrés pour une opération d’envoi terminée :</span><span class="sxs-lookup"><span data-stu-id="b1769-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="b1769-480">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-481">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-483">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="b1769-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-485">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="b1769-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-487">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-487">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-488">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="b1769-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-490">Longueur de la mémoire tampon d’octets envoyés.</span><span class="sxs-lookup"><span data-stu-id="b1769-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="b1769-491">Pour les mémoires tampons chaînées, ce paramètre représente le nombre total d’octets envoyés de toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="b1769-492">SendMsg terminé</span><span class="sxs-lookup"><span data-stu-id="b1769-492">SendMsg Completed</span></span>

<span data-ttu-id="b1769-493">ID d’événement = 25</span><span class="sxs-lookup"><span data-stu-id="b1769-493">Event ID = 25</span></span>

<span data-ttu-id="b1769-494">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-495">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-496">Les événements Winsock suivants sont suivis lorsqu’une opération de publication de tampon [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) se termine sur un socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="b1769-497">Une application effectue une opération [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="b1769-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="b1769-498">Les paramètres suivants sont enregistrés pour la fin du [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="b1769-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="b1769-499">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-500">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-502">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="b1769-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-504">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="b1769-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-506">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="b1769-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-508">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-508">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-509">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="b1769-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-511">Longueur de la mémoire tampon d’octets envoyés.</span><span class="sxs-lookup"><span data-stu-id="b1769-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="b1769-512">Pour les mémoires tampons chaînées, ce paramètre représente le nombre total d’octets envoyés de toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="b1769-514">Adresse IP distante du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="b1769-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="b1769-516">Numéro de port IP distant du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="b1769-517">RecvFrom terminé</span><span class="sxs-lookup"><span data-stu-id="b1769-517">RecvFrom Completed</span></span>

<span data-ttu-id="b1769-518">ID d’événement = 26 (IPv4), ID d’événement = 27 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="b1769-519">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-520">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-521">Les événements Winsock suivants sont suivis lorsqu’une opération de publication de mémoire tampon [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) se termine sur un socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="b1769-522">Une application effectue une opération [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .</span><span class="sxs-lookup"><span data-stu-id="b1769-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="b1769-523">Les paramètres suivants sont enregistrés pour la fin du [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) :</span><span class="sxs-lookup"><span data-stu-id="b1769-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="b1769-524">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-525">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-527">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="b1769-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-529">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="b1769-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-531">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="b1769-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-533">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-533">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-534">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="b1769-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-536">Longueur de la mémoire tampon d’octets reçus.</span><span class="sxs-lookup"><span data-stu-id="b1769-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="b1769-537">Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets reçus dans toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="b1769-539">Adresse IP distante du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="b1769-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="b1769-541">Numéro de port IP distant du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="b1769-542">SendTo terminé</span><span class="sxs-lookup"><span data-stu-id="b1769-542">SendTo Completed</span></span>

<span data-ttu-id="b1769-543">ID d’événement = 28</span><span class="sxs-lookup"><span data-stu-id="b1769-543">Event ID = 28</span></span>

<span data-ttu-id="b1769-544">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-545">Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b1769-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="b1769-546">Les événements Winsock suivants sont suivis lorsqu’une opération de publication de mémoire tampon [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) se termine sur un socket :</span><span class="sxs-lookup"><span data-stu-id="b1769-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="b1769-547">Une application effectue une opération [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) .</span><span class="sxs-lookup"><span data-stu-id="b1769-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="b1769-548">Les paramètres suivants sont enregistrés pour la fin de l’exécution de l’opération [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) :</span><span class="sxs-lookup"><span data-stu-id="b1769-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="b1769-549">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="b1769-550">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="b1769-552">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="b1769-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="b1769-554">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="b1769-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="b1769-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="b1769-556">Nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1769-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="b1769-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b1769-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="b1769-558">Adresse virtuelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b1769-558">The virtual address of the buffer.</span></span> <span data-ttu-id="b1769-559">Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="b1769-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="b1769-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="b1769-561">Longueur de la mémoire tampon d’octets envoyés.</span><span class="sxs-lookup"><span data-stu-id="b1769-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="b1769-562">Pour les mémoires tampons chaînées, ce paramètre représente le nombre total d’octets envoyés de toutes les mémoires tampons de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b1769-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="b1769-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="b1769-564">Adresse IP distante du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="b1769-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="b1769-566">Numéro de port IP distant du Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="b1769-567">Ensemble d’options de socket</span><span class="sxs-lookup"><span data-stu-id="b1769-567">Socket Option Set</span></span>

<span data-ttu-id="b1769-568">ID d’événement = 29</span><span class="sxs-lookup"><span data-stu-id="b1769-568">Event ID = 29</span></span>

<span data-ttu-id="b1769-569">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-570">Chaque fois qu’une application modifie certaines valeurs d’option de socket et les IOCTL, les nouvelles valeurs sont consignées.</span><span class="sxs-lookup"><span data-stu-id="b1769-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="b1769-571">Les options journalisées peuvent être utilisées pour diagnostiquer des performances médiocres ou un comportement étrange dans les applications.</span><span class="sxs-lookup"><span data-stu-id="b1769-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="b1769-572">Les événements Winsock suivants sont suivis pour certaines options de socket et IOCTL :</span><span class="sxs-lookup"><span data-stu-id="b1769-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="b1769-573">\_SNDBUF change donc.</span><span class="sxs-lookup"><span data-stu-id="b1769-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="b1769-574">\_RCVBUF change donc.</span><span class="sxs-lookup"><span data-stu-id="b1769-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="b1769-575">FIONBIO</span><span class="sxs-lookup"><span data-stu-id="b1769-575">FIONBIO</span></span>
-   <span data-ttu-id="b1769-576">SIO \_ activer \_ la \_ file d’attente circulaire</span><span class="sxs-lookup"><span data-stu-id="b1769-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="b1769-577">SIO \_ UDP \_ CONNRESET</span><span class="sxs-lookup"><span data-stu-id="b1769-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="b1769-578">\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="b1769-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="b1769-579">Les paramètres suivants sont consignés pour les appels de fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) et [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) qui modifient les valeurs ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="b1769-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="b1769-580">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-580">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-581">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-583">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-585">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span><span class="sxs-lookup"><span data-stu-id="b1769-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="b1769-587">Option de socket ou IOCTL modifiée.</span><span class="sxs-lookup"><span data-stu-id="b1769-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="b1769-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="b1769-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="b1769-589">Nouvelle valeur pour l’option de socket ou ioctl.</span><span class="sxs-lookup"><span data-stu-id="b1769-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="b1769-590">Sélection/interrogation publiée</span><span class="sxs-lookup"><span data-stu-id="b1769-590">Select/Poll Posted</span></span>

<span data-ttu-id="b1769-591">ID d’événement = 30</span><span class="sxs-lookup"><span data-stu-id="b1769-591">Event ID = 30</span></span>

<span data-ttu-id="b1769-592">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-593">Les événements Winsock suivants sont suivis lorsqu’une application appelle la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="b1769-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="b1769-594">L’application publie une requête [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="b1769-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="b1769-595">Les paramètres suivants sont enregistrés pour les événements [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="b1769-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="b1769-596">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="b1769-597">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="b1769-599">ID du processus propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b1769-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="b1769-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="b1769-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="b1769-601">Nombre de handles passés par l’application (valide uniquement sur l’événement de lancement).</span><span class="sxs-lookup"><span data-stu-id="b1769-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="b1769-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Expiré</span><span class="sxs-lookup"><span data-stu-id="b1769-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="b1769-603">Durée d’attente maximale de la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="b1769-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="b1769-604">Sélection/interrogation terminée</span><span class="sxs-lookup"><span data-stu-id="b1769-604">Select/Poll Completed</span></span>

<span data-ttu-id="b1769-605">ID d’événement = 31</span><span class="sxs-lookup"><span data-stu-id="b1769-605">Event ID = 31</span></span>

<span data-ttu-id="b1769-606">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-607">Les événements Winsock suivants sont suivis lorsqu’une application appelle la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="b1769-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="b1769-608">Winsock termine un appel [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="b1769-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="b1769-609">Les paramètres suivants sont journalisés lors de l’exécution d’une opération [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="b1769-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="b1769-610">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-610">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-611">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-613">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="b1769-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-615">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="b1769-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs</span><span class="sxs-lookup"><span data-stu-id="b1769-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="b1769-617">Code d’erreur retourné pour l’opération [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="b1769-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="b1769-618">WSAEventSelect</span><span class="sxs-lookup"><span data-stu-id="b1769-618">WSAEventSelect</span></span>

<span data-ttu-id="b1769-619">ID d’événement = 32</span><span class="sxs-lookup"><span data-stu-id="b1769-619">Event ID = 32</span></span>

<span data-ttu-id="b1769-620">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-621">Les événements Winsock suivants sont suivis lorsqu’une application appelle la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :</span><span class="sxs-lookup"><span data-stu-id="b1769-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="b1769-622">Consignez le masque d’événement passé dans la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="b1769-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="b1769-623">Les paramètres suivants sont consignés pour les appels de fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :</span><span class="sxs-lookup"><span data-stu-id="b1769-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="b1769-624">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-624">Parameter</span></span>                                                                                                | <span data-ttu-id="b1769-625">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="b1769-627">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="b1769-629">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span><span class="sxs-lookup"><span data-stu-id="b1769-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="b1769-631">Valeur du masque d’événement.</span><span class="sxs-lookup"><span data-stu-id="b1769-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="b1769-632">Datagramme supprimé</span><span class="sxs-lookup"><span data-stu-id="b1769-632">Dropped Datagram</span></span>

<span data-ttu-id="b1769-633">ID d’événement = 33 (IPv4), ID d’événement = 34 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="b1769-634">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-635">Pour faciliter le diagnostic des problèmes concernant les applications de datagramme, les événements Winsock suivants sont suivis :</span><span class="sxs-lookup"><span data-stu-id="b1769-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="b1769-636">Lorsqu’un datagramme arrive et qu’il est supprimé, l’espace de mémoire tampon est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="b1769-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="b1769-637">Sur un datagramme connecté, si les données arrivent d’une source autre que la destination connectée.</span><span class="sxs-lookup"><span data-stu-id="b1769-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="b1769-638">Les paramètres suivants sont journalisés pour les datagrammes supprimés :</span><span class="sxs-lookup"><span data-stu-id="b1769-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="b1769-639">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="b1769-640">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="b1769-642">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="b1769-644">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>Taille paquet</span><span class="sxs-lookup"><span data-stu-id="b1769-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="b1769-646">Taille du paquet qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="b1769-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="b1769-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="b1769-648">Adresse IP de la source du paquet.</span><span class="sxs-lookup"><span data-stu-id="b1769-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="b1769-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="b1769-650">Numéro de port IP de la source du paquet.</span><span class="sxs-lookup"><span data-stu-id="b1769-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="b1769-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Donc</span><span class="sxs-lookup"><span data-stu-id="b1769-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="b1769-652">Code d’erreur ou raison de la suppression du paquet.</span><span class="sxs-lookup"><span data-stu-id="b1769-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="b1769-653">Connexion indiquée</span><span class="sxs-lookup"><span data-stu-id="b1769-653">Connection Indicated</span></span>

<span data-ttu-id="b1769-654">ID d’événement = 35 (IPv4), ID d’événement = 36 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="b1769-655">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-656">Les événements Winsock suivants sont suivis pour les opérations indiquées par la connexion :</span><span class="sxs-lookup"><span data-stu-id="b1769-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="b1769-657">Une application reçoit une demande de connexion.</span><span class="sxs-lookup"><span data-stu-id="b1769-657">An application receives a connection request.</span></span>

<span data-ttu-id="b1769-658">Les paramètres suivants sont consignés pour les connexions indiquées à partir d’événements de transport :</span><span class="sxs-lookup"><span data-stu-id="b1769-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="b1769-659">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-659">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-660">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-662">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-664">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="b1769-666">Adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="b1769-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="b1769-668">Numéro de port de l’adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="b1769-669">Données indiquées</span><span class="sxs-lookup"><span data-stu-id="b1769-669">Data Indicated</span></span>

<span data-ttu-id="b1769-670">ID d’événement = 37</span><span class="sxs-lookup"><span data-stu-id="b1769-670">Event ID = 37</span></span>

<span data-ttu-id="b1769-671">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-672">Les événements Winsock suivants sont suivis pour les opérations indiquées par les données :</span><span class="sxs-lookup"><span data-stu-id="b1769-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="b1769-673">Une application reçoit des données sur un socket connecté.</span><span class="sxs-lookup"><span data-stu-id="b1769-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="b1769-674">Les paramètres suivants sont enregistrés pour les données indiquées à partir des événements de transport :</span><span class="sxs-lookup"><span data-stu-id="b1769-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="b1769-675">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="b1769-676">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="b1769-678">ID du processus propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b1769-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="b1769-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="b1769-680">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Octets indiqués</span><span class="sxs-lookup"><span data-stu-id="b1769-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="b1769-682">Nombre d’octets reçus sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="b1769-683">Données indiquées à partir du transport</span><span class="sxs-lookup"><span data-stu-id="b1769-683">Data Indicated from Transport</span></span>

<span data-ttu-id="b1769-684">ID d’événement = 38 (IPv4), ID d’événement = 39 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b1769-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="b1769-685">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-686">Les événements Winsock suivants sont suivis pour les données indiquées à partir des opérations de transport :</span><span class="sxs-lookup"><span data-stu-id="b1769-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="b1769-687">Une application publie une demande de réception et reçoit des données.</span><span class="sxs-lookup"><span data-stu-id="b1769-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="b1769-688">Les paramètres suivants sont enregistrés pour les données indiquées à partir des événements de transport :</span><span class="sxs-lookup"><span data-stu-id="b1769-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="b1769-689">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="b1769-690">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="b1769-692">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="b1769-694">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="b1769-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-</span><span class="sxs-lookup"><span data-stu-id="b1769-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="b1769-696">Adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="b1769-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</span><span class="sxs-lookup"><span data-stu-id="b1769-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="b1769-698">Numéro de port de l’adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="b1769-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="b1769-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Octets indiqués</span><span class="sxs-lookup"><span data-stu-id="b1769-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="b1769-700">Nombre d’octets reçus sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="b1769-701">Déconnexion indiquée à partir du transport</span><span class="sxs-lookup"><span data-stu-id="b1769-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="b1769-702">ID d’événement = 41</span><span class="sxs-lookup"><span data-stu-id="b1769-702">Event ID = 41</span></span>

<span data-ttu-id="b1769-703">Niveau = 5 (commentaires)</span><span class="sxs-lookup"><span data-stu-id="b1769-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="b1769-704">Les événements Winsock suivants sont suivis pour les opérations de déconnexion indiquées :</span><span class="sxs-lookup"><span data-stu-id="b1769-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="b1769-705">Une application reçoit une indication de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="b1769-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="b1769-706">Les paramètres suivants sont enregistrés pour la déconnexion indiqué à partir des événements de transport :</span><span class="sxs-lookup"><span data-stu-id="b1769-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="b1769-707">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b1769-707">Parameter</span></span>                                                                                            | <span data-ttu-id="b1769-708">Description</span><span class="sxs-lookup"><span data-stu-id="b1769-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter</span><span class="sxs-lookup"><span data-stu-id="b1769-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="b1769-710">Adresse de la structure EPROCESS du noyau pour le processus.</span><span class="sxs-lookup"><span data-stu-id="b1769-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="b1769-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="b1769-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="b1769-712">Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1769-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b1769-713">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1769-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1769-714">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="b1769-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="b1769-715">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="b1769-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="b1769-716">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="b1769-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="b1769-717">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="b1769-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
