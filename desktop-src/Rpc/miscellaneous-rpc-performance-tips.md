---
title: Astuces des performances RPC diverses
description: Cette section décrit divers conseils relatifs aux performances pour le développement de serveurs RPC haute performance. Cette section fournit de nombreux conseils qui font référence au client RPC. Le développement d’un client RPC permet au serveur RPC d’effectuer moins de travail.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011413"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Astuces des performances RPC diverses

Cette section décrit divers conseils relatifs aux performances pour le développement de serveurs RPC haute performance. Cette section fournit de nombreux conseils qui font référence au client RPC. Le développement d’un client RPC permet au serveur RPC d’effectuer moins de travail.

## <a name="use-kerberos"></a>Utiliser Kerberos

Si la sécurité est utilisée, utilisez Kerberos. Côté serveur, Kerberos n’a pas besoin d’accéder au KDC. Cela déplace la charge de travail du serveur vers le client, ce qui permet d’obtenir des serveurs plus performants.

## <a name="use-static-identity-tracking"></a>Utiliser le suivi des identités statiques

Si la sécurité est utilisée, essayez d’utiliser le suivi d’identité statique. Le suivi des identités statiques est moins onéreux en termes d’utilisation des ressources que le suivi dynamique des identités. Si l’identité du client change et que le serveur ne doit pas être conscient de la modification, utilisez le suivi dynamique au lieu de créer un handle de liaison différent pour chaque identité. Toutefois, si l’identité est la même, assurez-vous que RPC est conscient de ce fait pour éviter que RPC vérifie l’identité modifiée à chaque fois.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Utiliser la fonction RpcGetAuthorizationContextForClient

si vous devez vérifier l’accès dans Windows XP, utilisez la fonction [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) . Les contextes d’autorisation qui en résultent permettent des contrôles d’accès très rapides, qui sont mis en cache efficacement par le runtime RPC.

## <a name="do-not-modify-the-token-unless-necessary"></a>Ne modifiez pas le jeton, sauf si nécessaire

Si le suivi dynamique des identités est utilisé, ne modifiez pas le jeton de thread/processus, sauf si cela est absolument nécessaire. Même s’il est modifié en paramètres précédemment, le jeton est souvent suffisamment différent du système de sécurité pour déclencher l’établissement d’un nouveau contexte de sécurité.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Prendre en compte la sérialisation en mode mixte pour les handles de contexte

Le mode de sérialisation par défaut pour le handle de contexte est sérialisé (exclusif). Envisagez d’effectuer tous les appels qui ne modifient pas l’état du handle de contexte en mode de sérialisation partagé. Pour plus d’informations, consultez [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .

 

 




