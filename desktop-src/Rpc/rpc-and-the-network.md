---
title: RPC et le réseau
description: Cette section explique comment gérer la non-fiabilité du réseau lors de l’utilisation d’un appel de procédure distante, et explique comment les API de niveau RPC traduisent en activité réseau. La section fait référence uniquement aux \_ \_ séquences de protocole http ncacn IP TCP et ncacn \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Appel de procédure distante RPC, meilleures pratiques, RPC et le réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413617"
---
# <a name="rpc-and-the-network"></a>RPC et le réseau

Cette section explique comment gérer la non-fiabilité du réseau lors de l’utilisation d’un appel de procédure distante, et explique comment les API de niveau RPC traduisent en activité réseau. La section fait référence uniquement aux séquences de protocole [**\_ http**](/windows/desktop/Midl/ncacn-http) [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) et ncacn.

Cette section est composée des rubriques suivantes :

-   [Développement et déploiement sur le réseau](development-versus-deployment-in-the-network.md)
-   [Prévention des blocages de Client-Side](preventing-client-side-hangs.md)
-   [Gestion des groupes de connexions réseau (associations)](managing-network-connection-sets-associations-.md)
-   [Nettoyage des connexions inactives](idle-connection-cleanup.md)
-   [Gestion de la perte de connectivité](dealing-with-loss-of-connectivity.md)
-   [Nettoyage côté serveur](server-side-cleanup.md)

 

 