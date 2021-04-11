---
title: Sécurité de transport
description: Bien qu’il ne s’agisse pas de la méthode recommandée, vous pouvez utiliser les paramètres de sécurité proposés par le transport de canal nommé pour ajouter des fonctionnalités de sécurité à votre application distribuée.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310778"
---
# <a name="transport-security"></a><span data-ttu-id="0658e-103">Sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="0658e-103">Transport Security</span></span>

<span data-ttu-id="0658e-104">Bien qu’il ne s’agisse pas de la méthode recommandée, vous pouvez utiliser les paramètres de sécurité proposés par le transport de canal nommé pour ajouter des fonctionnalités de sécurité à votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="0658e-104">Although this is not the preferred method, you can use the security settings that the named-pipe transport offers to add security features to your distributed application.</span></span> <span data-ttu-id="0658e-105">Ces paramètres de sécurité sont utilisés avec les fonctions Microsoft RPC qui commencent par les préfixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) et [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), ainsi que les fonctions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) et [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span><span class="sxs-lookup"><span data-stu-id="0658e-105">These security settings are used with the Microsoft RPC functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

> [!Note]  
> <span data-ttu-id="0658e-106">Si vous exécutez une application qui est un service et que vous utilisez NTLM pour la sécurité, vous devez ajouter une dépendance de service explicite pour votre application.</span><span class="sxs-lookup"><span data-stu-id="0658e-106">If you are running an application that is a service and you are using NTLM for security, you must add an explicit service dependency for your application.</span></span> <span data-ttu-id="0658e-107">Le Secur32.dll appelle le gestionnaire de contrôle des services (SCM) pour lancer le service de package de sécurité NTLM.</span><span class="sxs-lookup"><span data-stu-id="0658e-107">The Secur32.dll will call the Service Control Manager (SCM) to begin the NTLM security package service.</span></span> <span data-ttu-id="0658e-108">Toutefois, une application RPC qui est un service et qui s’exécute en tant que système doit également contacter SC, sauf si elle est connectée à un autre service sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0658e-108">However, an RPC application that is a service and is running as a system, must also contact the SC unless it is connecting to another service on the same computer.</span></span>

 

 

 




