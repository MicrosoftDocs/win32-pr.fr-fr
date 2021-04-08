---
title: Prise en charge de l’hôte de sécurité RAS
description: Windows NT 4,0 fournit un moyen pour une DLL de sécurité RAS tierce pour améliorer les fonctionnalités de sécurité RAS intégrées. Windows 95 ne fournit pas cette prise en charge.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Prise en charge des hôtes, RAS
- Prise en charge de l’hôte de sécurité, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674026"
---
# <a name="ras-security-host-support"></a>Prise en charge de l’hôte de sécurité RAS

Windows NT 4,0 fournit un moyen pour une DLL de sécurité RAS tierce pour améliorer les fonctionnalités de sécurité RAS intégrées. Windows 95 ne fournit pas cette prise en charge.

Un serveur RAS Windows NT/Windows 2000 fournit des mécanismes de sécurité pour valider l’accès réseau des utilisateurs distants. Lorsqu’un serveur RAS reçoit un appel, il valide les informations d’identification de l’utilisateur par rapport à la base de données de comptes locaux ou de domaine. RAS prend également en charge la sécurité de rappel, dans laquelle le serveur RAS se bloque, puis rappelle à l’utilisateur distant pour établir la connexion. Pour les réseaux dans lesquels ce niveau de sécurité n’est pas suffisant, vous pouvez installer une DLL de sécurité RAS tierce. La DLL de sécurité peut ensuite authentifier un utilisateur distant en lisant les informations de sécurité dans une base de données autre que la base de données de compte d’utilisateur standard.

Lorsque le serveur RAS reçoit un appel, il appelle la DLL de sécurité pour authentifier l’utilisateur distant. La prise en charge de l’hôte de sécurité RAS fournit un mécanisme permettant à la DLL de sécurité de communiquer avec l’utilisateur distant par le biais d’une fenêtre de terminal sur l’ordinateur distant. Dans un scénario classique, la DLL de sécurité demande le nom d’ouverture de session de l’utilisateur distant. La DLL utilise ensuite sa base de données de sécurité privée pour formuler un défi à envoyer au terminal distant. Par exemple, le défi peut être un code que l’utilisateur doit fournir comme entrée à un lecteur Cardkey. Le lecteur Cardkey affiche ensuite une réponse que l’utilisateur distant tape dans la fenêtre de terminal. La DLL de sécurité valide ensuite la réponse par rapport aux informations de l’utilisateur dans la base de données de sécurité privée.

Si la DLL de sécurité authentifie l’utilisateur distant, le serveur RAS effectue sa propre authentification. Cela garantit que la sécurité RAS authentifie toujours un utilisateur distant, même si une DLL de sécurité qui accorde l’accès à tous les utilisateurs est installée.

> [!Note]  
> Windows NT/Windows 2000 fournit actuellement la prise en charge de l’hôte de sécurité RAS uniquement pour les connexions de modem asynchrones. les autres types de connexions, comme Ethernet (qui n’est pas une connexion par modem), VPN (qui n’est pas non plus une connexion par modem) ou RNIS (qui est synchrone), ne sont pas pris en charge.

 

 

 




