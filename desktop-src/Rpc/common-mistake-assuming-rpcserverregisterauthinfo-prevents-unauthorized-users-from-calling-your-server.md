---
title: Erreur courante en supposant que RpcServerRegisterAuthInfo empêche les utilisateurs non autorisés d’appeler votre serveur
description: Lorsque des fournisseurs de sécurité sont inscrits sur le serveur avec la fonction RpcServerRegisterAuthInfo, une option est ajoutée, et non une exigence.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675093"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Erreur courante : en supposant que RpcServerRegisterAuthInfo empêche les utilisateurs non autorisés d’appeler votre serveur

Lorsque des fournisseurs de sécurité sont inscrits sur le serveur avec la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , une option est ajoutée, et non une exigence. Cela signifie que les inscriptions précédentes avec **RpcServerRegisterAuthInfo** ne sont pas remplacées. Cela signifie également que les clients non authentifiés peuvent toujours se connecter. En appelant la fonction **RpcServerRegisterAuthInfo** , les clients non authentifiés ne sont pas autorisés à se connecter ; ils peuvent toujours se connecter, mais les appels de fonction, tels que [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) et [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , échouent. Ainsi, lorsque la fonction **RpcServerRegisterAuthInfo** est appelée, les attaquants potentiels n’ont pas été désinstallés. les clients qui devraient avoir accès ont la possibilité de prouver leur identité. Les vérifications doivent toujours être en place pour déterminer si des attaquants potentiels tentent de se connecter.

 

 




