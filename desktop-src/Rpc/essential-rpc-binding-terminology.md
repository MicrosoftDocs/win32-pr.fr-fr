---
title: Terminologie des liaisons RPC essentielles
description: Pour mieux vous aider dans une discussion sur le processus de connexion client/serveur, il est utile de connaître les termes suivants.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Appel de procédure distante RPC, description, liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031690"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="9a6d5-104">Terminologie des liaisons RPC essentielles</span><span class="sxs-lookup"><span data-stu-id="9a6d5-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="9a6d5-105">Pour mieux vous aider dans une discussion sur le processus de connexion client/serveur, il est utile de connaître les termes suivants.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a6d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a6d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a6d5-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Séquence de protocole</span><span class="sxs-lookup"><span data-stu-id="9a6d5-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="9a6d5-108">Lorsque les systèmes d’exploitation réseau communiquent entre eux, ils doivent écouter et prononcer la même langue.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="9a6d5-109">Ces langages sont appelés *séquences de protocole*.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="9a6d5-110">Les programmes client et serveur doivent utiliser des séquences de protocole que le réseau qui les connecte prend en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="9a6d5-111">Microsoft RPC prend en charge différentes séquences de protocole.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="9a6d5-112">Pour plus d’informations, consultez [sélection d’une séquence de protocole](selecting-a-protocol-sequence.md), [spécification de séquences de protocole](specifying-protocol-sequences.md)et [**point de terminaison**](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="9a6d5-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="9a6d5-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Ordinateur hôte serveur ou système hôte serveur</span><span class="sxs-lookup"><span data-stu-id="9a6d5-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="9a6d5-114">Le programme serveur s’exécute sur l’ordinateur hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="9a6d5-115">Toutefois, une grande partie de la documentation sur l’informatique client/serveur fait référence au programme serveur et à l’ordinateur hôte du serveur en tant que « serveur ».</span><span class="sxs-lookup"><span data-stu-id="9a6d5-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="9a6d5-116">Le résultat est qu’il n’est pas toujours évident de savoir ce qui est abordé.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="9a6d5-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="9a6d5-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="9a6d5-118">Les programmes serveur écoutent un port ou un groupe de ports sur l’ordinateur hôte du serveur pour les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="9a6d5-119">Les systèmes hôtes de serveur maintiennent une base de données de ces ports, appelés points de terminaison dans RPC.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="9a6d5-120">La base de données est appelée mappage de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="9a6d5-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Liant</span><span class="sxs-lookup"><span data-stu-id="9a6d5-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="9a6d5-122">Les programmes clients créent une liaison avec le serveur pour établir une session de communication.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="9a6d5-123">Une liaison contient toutes les informations dont l’application cliente a besoin pour créer la session.</span><span class="sxs-lookup"><span data-stu-id="9a6d5-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 