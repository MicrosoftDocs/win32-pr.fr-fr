---
title: Sécurité de transport
description: Bien qu’il ne s’agisse pas de la méthode recommandée, vous pouvez utiliser les paramètres de sécurité proposés par le transport de canal nommé pour ajouter des fonctionnalités de sécurité à votre application distribuée.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d92a0c9f0b31392d265c1c60bd201d088af8e8ff0b10ac4e09e274da92d2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011207"
---
# <a name="transport-security"></a>Sécurité de transport

Bien qu’il ne s’agisse pas de la méthode recommandée, vous pouvez utiliser les paramètres de sécurité proposés par le transport de canal nommé pour ajouter des fonctionnalités de sécurité à votre application distribuée. Ces paramètres de sécurité sont utilisés avec les fonctions Microsoft RPC qui commencent par les préfixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) et [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), ainsi que les fonctions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) et [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Si vous exécutez une application qui est un service et que vous utilisez NTLM pour la sécurité, vous devez ajouter une dépendance de service explicite pour votre application. Le Secur32.dll appelle le gestionnaire de contrôle des services (SCM) pour lancer le service de package de sécurité NTLM. Toutefois, une application RPC qui est un service et qui s’exécute en tant que système doit également contacter SC, sauf si elle est connectée à un autre service sur le même ordinateur.

 

 

 




