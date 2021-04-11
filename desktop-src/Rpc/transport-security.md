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
# <a name="transport-security"></a>Sécurité de transport

Bien qu’il ne s’agisse pas de la méthode recommandée, vous pouvez utiliser les paramètres de sécurité proposés par le transport de canal nommé pour ajouter des fonctionnalités de sécurité à votre application distribuée. Ces paramètres de sécurité sont utilisés avec les fonctions Microsoft RPC qui commencent par les préfixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) et [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), ainsi que les fonctions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) et [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Si vous exécutez une application qui est un service et que vous utilisez NTLM pour la sécurité, vous devez ajouter une dépendance de service explicite pour votre application. Le Secur32.dll appelle le gestionnaire de contrôle des services (SCM) pour lancer le service de package de sécurité NTLM. Toutefois, une application RPC qui est un service et qui s’exécute en tant que système doit également contacter SC, sauf si elle est connectée à un autre service sur le même ordinateur.

 

 

 




