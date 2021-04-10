---
title: Intégrité et confidentialité
description: Les communications client/service qui requièrent une authentification mutuelle doivent protéger le trafic qu’ils échangent après une authentification réussie.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- Intégrité et confidentialité AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ed167c3796aec2b0717b1207ff56565ec94afa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940811"
---
# <a name="integrity-and-privacy"></a>Intégrité et confidentialité

Les communications client/service qui requièrent une authentification mutuelle doivent protéger le trafic qu’ils échangent après une authentification réussie. Il est déconseillé de s’authentifier mutuellement au moment de la connexion initiale au service si le trafic est ultérieurement susceptible d’être modifié par un utilisateur non autorisé. SSPI, RPC et COM fournissent tous des utilitaires pour la signature numérique et le chiffrement des messages. L’application de signatures numériques empêche le trafic modifié de passer inaperçus et décourage les écoutes clandestines. Le trafic peut être intercepté bien sûr, mais le déchiffrement du trafic est suffisamment difficile pour dissuader la plupart des utilisateurs non autorisés.

À moins que les exigences de performances ne soient sévères, l’utilisation de la signature et du chiffrement est recommandée, en particulier pour les fonctions administratives. Même si les performances constituent un problème, certains clients choisissent une sécurité plus étroite pour de meilleures performances. Dans ce cas, rendez les options d’intégrité et de confidentialité configurables avec un niveau de sécurité plus élevé, ce qui est l’option par défaut.

Les clients RPC peuvent spécifier le niveau d’intégrité et de confidentialité lorsqu’ils appellent la fonction [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) pour définir les données d’authentification de la liaison RPC. Utilisez **\_ \_ \_ \_ \_ l’intégrité PKT du niveau d’authentification RPC c** pour la signature et la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification c RPC** pour le chiffrement. Pour plus d’informations, consultez [authentification mutuelle dans les applications RPC](mutual-authentication-in-rpc-applications.md).

Les services qui utilisent un package SSPI pour l’authentification mutuelle peuvent interroger le package pour déterminer s’il prend en charge les fonctions [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)et [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) pour la signature et le chiffrement des messages. Pour plus d’informations et pour obtenir un exemple de code, consultez [garantie de l’intégrité des communications pendant l’échange de messages](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 