---
title: attribut ncacn_http
description: Le \_ mot clé http ncacn identifie Microsoft Internet Information Server (IIS) comme famille de protocoles pour le point de terminaison.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726340"
---
# <a name="ncacn_http-attribute"></a><span data-ttu-id="81e73-104">\_attribut http ncacn</span><span class="sxs-lookup"><span data-stu-id="81e73-104">ncacn\_http attribute</span></span>

<span data-ttu-id="81e73-105">Le mot clé **\_ http ncacn** identifie Microsoft Internet Information Server (IIS) comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="81e73-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="81e73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81e73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e73-107">*\_serveur RPC*</span><span class="sxs-lookup"><span data-stu-id="81e73-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="81e73-108">Adresse Internet ou nom de l’ordinateur sur lequel s’exécute le processus du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="81e73-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="81e73-109">*endpoint*</span><span class="sxs-lookup"><span data-stu-id="81e73-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="81e73-110">Port TCP/IP connu (statique) sur lequel le processus serveur RPC est à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="81e73-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81e73-111">Notes</span><span class="sxs-lookup"><span data-stu-id="81e73-111">Remarks</span></span>

<span data-ttu-id="81e73-112">L’identification de Microsoft Internet Information Server (IIS) comme famille de protocole permet aux applications client et serveur de communiquer sur Internet à l’aide de Microsoft Internet Information Server (IIS) en tant que proxy.</span><span class="sxs-lookup"><span data-stu-id="81e73-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="81e73-113">Étant donné que les appels sont acheminés via un port HTTP établi, ils peuvent traverser les pare-feu.</span><span class="sxs-lookup"><span data-stu-id="81e73-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="81e73-114">Toutes les applications clientes et serveur RPC peuvent prendre en charge le protocole **\_ http ncacn** tant qu’elles sont en réseau sur un serveur Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="81e73-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="81e73-115">IIS contacte le serveur RPC et établit un socket TCP/IP, qu’il gère pour le client.</span><span class="sxs-lookup"><span data-stu-id="81e73-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="81e73-116">IIS négocie une connexion TCP/IP avec le serveur RPC et, une fois la négociation terminée, agit comme un proxy RPC, en transférant les données entre le socket TCP/IP côté client et le socket TCP/IP côté serveur.</span><span class="sxs-lookup"><span data-stu-id="81e73-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="81e73-117">Lorsque le proxy RPC IIS détecte une fermeture de session sur le côté client ou côté serveur, il ferme le socket restant.</span><span class="sxs-lookup"><span data-stu-id="81e73-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="81e73-118">L’application cliente utilise implicitement la liaison statique aux services Internet (IIS), mais le serveur peut utiliser des points de terminaison dynamiques, avec le mappeur de point de terminaison (RPCSS) du serveur qui résout le port du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="81e73-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="81e73-119">Si IIS se trouve sur un autre ordinateur que le serveur RPC, IIS reçoit l’appel distant, contacte le service RPCSS sur l’ordinateur serveur RPC pour obtenir le point de terminaison du processus serveur, puis transfère l’appel au serveur RPC approprié.</span><span class="sxs-lookup"><span data-stu-id="81e73-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="81e73-120">Si Internet Explorer est installé, le transport vérifie le registre pour déterminer s’il existe une configuration pour un proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="81e73-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="81e73-121">Si un proxy existe, le transport l’utilise.</span><span class="sxs-lookup"><span data-stu-id="81e73-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="81e73-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="81e73-122">Examples</span></span>

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a><span data-ttu-id="81e73-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81e73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e73-124">**poste**</span><span class="sxs-lookup"><span data-stu-id="81e73-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="81e73-125">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="81e73-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="81e73-126">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="81e73-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 