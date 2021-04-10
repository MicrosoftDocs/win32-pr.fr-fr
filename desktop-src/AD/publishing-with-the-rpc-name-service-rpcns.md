---
title: Publication avec le service de noms RPC
description: Les services RPC peuvent publier leurs identificateurs dans un espace de noms à l’aide des API RpcNs (RPC Name Service).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publication avec la publicité service de noms RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030992"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="9cb29-104">Publication avec le service de noms RPC</span><span class="sxs-lookup"><span data-stu-id="9cb29-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="9cb29-105">Les services RPC peuvent publier leurs identificateurs dans un espace de noms à l’aide des API RpcNs (RPC Name Service).</span><span class="sxs-lookup"><span data-stu-id="9cb29-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="9cb29-106">Les API RpcNs dans Windows 2000 publient les entrées RPC dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9cb29-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="9cb29-107">Les services créent des liaisons RPC et les publient dans l’espace de noms en tant qu’entrées de serveur RPC nommées avec des attributs, y compris l’ID d’interface unique, un GUID qui est reconnu par les clients.</span><span class="sxs-lookup"><span data-stu-id="9cb29-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="9cb29-108">Un client peut ensuite rechercher les serveurs RPC qui offrent l’interface souhaitée, importer la liaison et se connecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="9cb29-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="9cb29-109">Pour plus d’informations sur la publication d’un service RPC, consultez [liaison côté serveur](/windows/desktop/Rpc/server-side-binding).</span><span class="sxs-lookup"><span data-stu-id="9cb29-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 