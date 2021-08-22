---
description: Initialisation du contexte client
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Initialisation du contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c0f2912de57487c1f30fdac1ef40740553947b993ef6f5179a028625f132af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141182"
---
# <a name="client-context-initialization"></a>Initialisation du contexte client

Pour établir une connexion sécurisée, le client acquiert un handle [*d’informations d’identification*](/windows/desktop/SecGloss/c-gly) sortantes avant d’envoyer une demande d’authentification au serveur. Le serveur crée un contexte de sécurité pour le client à partir de la demande d’authentification. Deux fonctions SSPI côté client sont impliquées dans la configuration de l’authentification :

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) obtient une référence aux [*informations d’identification*](/windows/desktop/SecGloss/c-gly)d’ouverture de session précédemment obtenues.
-   [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) crée les jetons de sécurité de la demande d’authentification initiale.

vous pouvez voir le Code de ce processus dans la fonction **GenClientContext** de l' [utilisation de SSPI avec un Client Windows sockets](using-sspi-with-a-windows-sockets-client.md).

Si un programme client doit utiliser des informations d’identification en plus de ses propres informations d’identification d’ouverture de session, telles qu’un nom d’utilisateur, un nom de domaine et un mot de passe différents, il les fournit dans l’appel [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) avec une structure d’identité de l' [**\_ \_ authentification \_ winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) , en spécifiant les informations d’identification supplémentaires. Pour plus d’informations sur les fonctions d’informations d’identification, consultez [gestion des informations d’identification](authentication-functions.md).

> [!Note]  
> Le membre **Flags** de la structure de l' [**\_ \_ \_ identité d’authentification Winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la sec peut être défini sur sec \_ winnt \_ \_ Identity \_ ANSI lorsque les chaînes de la structure sont ASCI ou OEM. Les chaînes ANSI peuvent être utilisées avec le membre **Flags** de la seconde structure d' **\_ \_ \_ identité d’authentification Winnt** avec la valeur s \_ winnt \_ \_ Identity \_ Unicode Unicode si elles sont d’abord converties en [*Unicode*](/windows/desktop/SecGloss/u-gly) à l’aide de la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) .

 

Pour initier la première branche de l’authentification, le client appelle [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) pour obtenir un jeton de sécurité initial à envoyer dans un message de demande de connexion au serveur.

Le client utilise les informations de jeton de sécurité reçues dans le descripteur de mémoire tampon de sortie pour générer un message à envoyer au serveur. La construction du message, en termes de positionnement de plusieurs mémoires tampons, et ainsi de suite, fait partie du [*protocole d’application*](/windows/desktop/SecGloss/a-gly) et doit être comprise par les deux parties.

Le client vérifie l’état de retour de [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) pour déterminer si l’authentification se termine en un seul appel. Un état de retour de SEC \_ je \_ continue \_ requis indique que le protocole de sécurité nécessite plusieurs messages d’authentification. Pour plus d’informations sur les fonctions de contexte, consultez [gestion du contexte](authentication-functions.md).

 

 
