---
title: Informations d’identification d’authentification du client
description: Chaque client authentifié doit fournir des informations d’authentification au serveur.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029787"
---
# <a name="client-authentication-credentials"></a>Informations d’identification d’authentification du client

Chaque client authentifié doit fournir des informations d’authentification au serveur. Sous RPC, le client stocke ses informations d’authentification dans la liaison entre le client et le serveur. Pour ce faire, le client appelle [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).

Il existe deux types d’informations d’identification : implicite et explicite :

-   Des informations d’identification explicites existent lorsque le client fournit le nom d’utilisateur, le mot de passe et le domaine.
-   Des informations d’identification implicites existent lorsque le client utilise des informations d’identification du thread ou du jeton de processus appelant les fonctions **RpcBindingSetAuthInfo** ou **RpcBindingSetAuthInfoEx** .

Les clients doivent s’abstenir de fournir des informations d’identification explicites, car le stockage, la manipulation et la récupération d’un mot de passe utilisateur peuvent introduire une faille de sécurité dans un système distribué si des informations d’identification explicites sont utilisées.

Pour utiliser des informations d’identification implicites, le client appelle **RpcBindingSetAuthInfo**(*ex*). Le système de sécurité et RPC obtiennent les informations d’identification à partir du thread ou du jeton de processus pour une utilisation dans la session d’authentification.

Si le client utilise des informations d’identification explicites, le cinquième paramètre de ces deux fonctions est de type [**RPC \_ auth \_ Identity \_ handle**](rpc-auth-identity-handle.md). Il s’agit d’un type flexible qui est un pointeur vers une structure de données. Le contenu de la structure de données peut être différent avec chaque service d’authentification. À l’heure actuelle, les fournisseurs de sécurité partagés pris en charge par RPC requièrent que votre application définisse le **\_ handle d' \_ identité \_ RPC auth** pour pointer vers une structure d' [**\_ \_ \_ identité Winnt auth**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . La structure de l' **\_ \_ \_ identité d’authentification Winnt** de la sec contient des champs pour un nom d’utilisateur, un domaine et un mot de passe.

 

 




