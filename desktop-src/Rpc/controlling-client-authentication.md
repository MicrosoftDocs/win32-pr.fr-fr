---
title: Contrôle de l’authentification du client
description: La meilleure méthode pour authentifier un client consiste à installer une fonction de rappel de sécurité à l’aide de la fonction RpcServerRegisterIf2 ou RpcServerRegisterIfEx ; accepte une fonction de rappel de sécurité en tant qu’argument.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb00a03740d99b137f97b085525e4c7232483dc15db487daf486ad51560b4427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931236"
---
# <a name="controlling-client-authentication"></a>Contrôle de l’authentification du client

La meilleure méthode pour authentifier un client consiste à installer une fonction de rappel de sécurité à l’aide de la fonction [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ; accepte une fonction de rappel de sécurité en tant qu’argument. Lorsque la fonction de rappel de sécurité est appelée, effectuez les vérifications nécessaires. Les attributs de la connexion, l’identité de l’appelant, ou les deux, peuvent être vérifiés. Pour vérifier les attributs d’une connexion, appelez la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) ou [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) . Cela permet de filtrer les clients qui ne sont pas authentifiés, les clients qui utilisent un fournisseur de sécurité spécifique ou les clients qui n’utilisent pas suffisamment de protection (par exemple, la confidentialité).

Pour autoriser l’accès à un sous-ensemble des utilisateurs authentifiés, utilisez [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Cette fonction retourne un contexte de client auth qui peut être utilisé pour effectuer des vérifications d’accès très sophistiquées. Par exemple, cette méthode peut être utilisée pour autoriser l’accès uniquement aux vice-présidents d’une organisation pendant les heures de travail normales, et au PDG pendant toute heure à l’aide des services de Active Directory pour mapper un nom d’utilisateur à son titre. L’utilisateur peut être représenté et son nom obtenu. Une fois que leur identité est connue, toute vérification souhaitée peut être effectuée.

 

 




