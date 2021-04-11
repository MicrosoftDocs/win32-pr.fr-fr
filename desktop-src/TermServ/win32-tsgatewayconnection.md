---
title: Classe Win32_TSGatewayConnection
description: Représente une connexion entre un ordinateur client et un serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection de la classe Services Bureau à distance
- Win32_TSGatewayConnection de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105832"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="7f6a5-105">\_Classe TSGatewayConnection Win32</span><span class="sxs-lookup"><span data-stu-id="7f6a5-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="7f6a5-106">Représente une connexion entre un ordinateur client et un serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="7f6a5-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6a5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f6a5-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="7f6a5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7f6a5-108">Members</span></span>

<span data-ttu-id="7f6a5-109">La classe **Win32 \_ TSGatewayConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7f6a5-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="7f6a5-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f6a5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f6a5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f6a5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f6a5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f6a5-112">Methods</span></span>

<span data-ttu-id="7f6a5-113">La classe **Win32 \_ TSGatewayConnection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="7f6a5-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="7f6a5-114">Method</span></span>                                                                     | <span data-ttu-id="7f6a5-115">Description</span><span class="sxs-lookup"><span data-stu-id="7f6a5-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f6a5-116">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="7f6a5-117">Vérifie l’état d’une connexion au serveur de passerelle Bureau à distance et si le serveur cible est configuré pour l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="7f6a5-118">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="7f6a5-119">Met fin à la connexion.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="7f6a5-120">**DisconnectProtocol**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="7f6a5-121">Met fin à toutes les connexions qui utilisent le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="7f6a5-122">**DisconnectUser**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="7f6a5-123">Met fin à toutes les connexions de l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="7f6a5-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f6a5-124">Properties</span></span>

<span data-ttu-id="7f6a5-125">La classe **Win32 \_ TSGatewayConnection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f6a5-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-127">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-129">Identificateur du canal.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-130">**ClientAddress**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-133">Adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-134">**ConnectedPort**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-137">Port sur la ressource connectée à laquelle l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-138">**ConnectedResource**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-141">Nom de l’ordinateur (ou du cluster) auquel le client est connecté.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-142">**ConnectedTime**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-145">Horodatage du moment où la connexion a été établie.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="7f6a5-146">Cette heure est réinitialisée lorsque la connexion est réinitialisée, même si elle est reconnectée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-147">**ConnectionDuration**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-150">Temps écoulé depuis l’heure de la connexion.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-151">**ConnectionKey**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-154">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f6a5-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-155">Identificateur de connexion au format « tunnelId : channelID ».</span><span class="sxs-lookup"><span data-stu-id="7f6a5-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-156">**FullUserName**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-159">Nom d’utilisateur complet de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-160">**IdleTime**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-163">Durée d’inactivité de la connexion.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-164">**NumberOfKilobytesReceived**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-165">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-167">Nombre de kilo-octets reçus à partir de l’ordinateur client par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-168">**NumberOfKilobytesSent**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-169">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-171">Nombre de kilo-octets envoyés à l’ordinateur client par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-175">Protocole utilisé pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="7f6a5-176">RDP</span><span class="sxs-lookup"><span data-stu-id="7f6a5-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="7f6a5-177">Protocole du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f6a5-178">**TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-179">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-181">Spécifie le type de transport pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="7f6a5-182">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="7f6a5-183">0</span><span class="sxs-lookup"><span data-stu-id="7f6a5-183">0</span></span>
</dt> <dd>

<span data-ttu-id="7f6a5-184">Transport RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-185">1</span><span class="sxs-lookup"><span data-stu-id="7f6a5-185">1</span></span>
</dt> <dd>

<span data-ttu-id="7f6a5-186">Transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-187">2</span><span class="sxs-lookup"><span data-stu-id="7f6a5-187">2</span></span>
</dt> <dd>

<span data-ttu-id="7f6a5-188">Transport UDP.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f6a5-189">**TunnelId**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-190">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-192">Identificateur du tunnel.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a5-193">**UserName**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6a5-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f6a5-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f6a5-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6a5-196">Nom d’utilisateur connecté au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f6a5-197">Notes</span><span class="sxs-lookup"><span data-stu-id="7f6a5-197">Remarks</span></span>

<span data-ttu-id="7f6a5-198">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="7f6a5-199">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7f6a5-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7f6a5-200">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7f6a5-201">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7f6a5-202">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7f6a5-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6a5-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f6a5-203">Requirements</span></span>



| <span data-ttu-id="7f6a5-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f6a5-204">Requirement</span></span> | <span data-ttu-id="7f6a5-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f6a5-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6a5-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f6a5-206">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6a5-207">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f6a5-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7f6a5-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f6a5-208">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6a5-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f6a5-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7f6a5-210">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f6a5-210">Namespace</span></span><br/>                | <span data-ttu-id="7f6a5-211">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7f6a5-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7f6a5-212">MOF</span><span class="sxs-lookup"><span data-stu-id="7f6a5-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f6a5-213"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f6a5-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f6a5-214">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6a5-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f6a5-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6a5-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7f6a5-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f6a5-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6a5-217">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="7f6a5-218">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="7f6a5-219">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="7f6a5-220">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="7f6a5-221">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="7f6a5-222">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="7f6a5-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

