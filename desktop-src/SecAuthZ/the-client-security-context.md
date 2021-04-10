---
description: Comme tous les processus, un serveur protégé a un jeton d’accès principal qui décrit son contexte de sécurité.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Contexte de sécurité du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951311"
---
# <a name="the-client-security-context"></a>Contexte de sécurité du client

Comme tous les [*processus*](/windows/desktop/SecGloss/p-gly), un serveur protégé a un [*jeton d’accès principal*](/windows/desktop/SecGloss/p-gly) qui décrit son [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly). Lorsqu’un client se connecte à un serveur protégé, le serveur peut vouloir effectuer des actions à l’aide du contexte de sécurité du client au lieu du contexte de sécurité du serveur. Par exemple, lorsqu’un client dans une conversation DDE (Dynamic Data Exchange) demande des informations à partir d’un serveur DDE, le serveur doit vérifier que le client est autorisé à accéder aux informations.

Un serveur peut agir dans le contexte de sécurité du client de deux manières :

-   Un thread du processus serveur peut emprunter l’identité du client. Dans ce cas, le thread du serveur a un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) d’emprunt d’identité qui identifie le client, les groupes du client et les [*privilèges*](/windows/desktop/SecGloss/p-gly)du client. Pour plus d’informations, consultez [emprunt d’identité du client](client-impersonation.md).
-   Le serveur peut récupérer les [*informations d’identification*](/windows/desktop/SecGloss/c-gly) du client et enregistrer le client sur l’ordinateur du serveur. Cela crée une nouvelle [*session*](/windows/desktop/SecGloss/s-gly) de connexion et produit un jeton d’accès principal pour le client. Le serveur peut ensuite utiliser le jeton d’accès du client pour emprunter l’identité du client ou démarrer un nouveau processus qui s’exécute dans le contexte de sécurité du client. Pour plus d’informations, consultez [sessions d’ouverture de session client](client-logon-sessions.md).

Dans la plupart des cas, l’emprunt d’identité du client est suffisant. L’emprunt d’identité permet au serveur de vérifier l’accès du client aux objets sécurisables, de vérifier les privilèges du client et de générer des entrées de piste d’audit qui identifient le client. En règle générale, un serveur doit démarrer une session de connexion client uniquement s’il doit utiliser le contexte de sécurité du client pour accéder aux ressources réseau.

 

 
