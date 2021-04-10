---
title: Nettoyage de l’entrée du service de noms
description: Une entrée de service de nom doit contenir des informations qui ne changent pas fréquemment.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029543"
---
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="f7e11-103">Nettoyage de l’entrée du service de noms</span><span class="sxs-lookup"><span data-stu-id="f7e11-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="f7e11-104">Une entrée de service de nom doit contenir des informations qui ne changent pas fréquemment.</span><span class="sxs-lookup"><span data-stu-id="f7e11-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="f7e11-105">Pour cette raison, n’incluez pas de points de terminaison dynamiques dans vos descripteurs de liaison exportés, car ils seront modifiés à chaque appel du serveur et encombreront votre entrée de service de noms.</span><span class="sxs-lookup"><span data-stu-id="f7e11-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="f7e11-106">Pour supprimer ces descripteurs de liaison, utilisez [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span><span class="sxs-lookup"><span data-stu-id="f7e11-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="f7e11-107">Par exemple, une séquence raisonnable d’opérations de serveur serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="f7e11-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="f7e11-108">Pour plusieurs transports :</span><span class="sxs-lookup"><span data-stu-id="f7e11-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="f7e11-109">Pour placer des liaisons dans le mappeur de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="f7e11-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="f7e11-110">Pour supprimer des points de terminaison des liaisons :</span><span class="sxs-lookup"><span data-stu-id="f7e11-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="f7e11-111">Pour ajouter des liaisons au service de noms :</span><span class="sxs-lookup"><span data-stu-id="f7e11-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




