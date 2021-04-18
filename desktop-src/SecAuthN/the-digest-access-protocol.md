---
description: Protocole d’accès Digest
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: Protocole d’accès Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569768"
---
# <a name="the-digest-access-protocol"></a>Protocole d’accès Digest

Le protocole d’accès Digest spécifié par [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) est implémenté par le [*fournisseur SSP (Security support Provider*](../secgloss/s-gly.md) ) Microsoft Digest. L’implémentation se compose d’un ensemble de fonctions de contexte de sécurité SSPI ( [Microsoft Security Support Provider Interface](sspi.md) ) que les applications client/serveur appellent pour :

-   Établissez un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages.
-   Obtenir les objets de données requis par le SSP Digest, tels que les [*informations d’identification*](../secgloss/c-gly.md) et les handles de contexte.
-   Accédez aux mécanismes d' [*intégrité*](../secgloss/i-gly.md) et de confidentialité des messages.

L’authentification d’accès Digest a lieu dans les transactions de demande/réponse jumelées, avec les demandes provenant du client et les réponses provenant du serveur. Une authentification Digest Access réussie requiert deux paires demande/réponse.

Lorsque le SSP Digest est utilisé pour l’authentification HTTP, aucune connexion n’est maintenue entre la première et la deuxième paire demande/réponse. En d’autres termes, le serveur n’attend pas la deuxième demande après l’envoi de la première réponse.

L’illustration suivante montre les étapes effectuées sur le chemin d’accès HTTP par un client et un serveur pour effectuer une authentification à l’aide du SSP Digest. Le mécanisme SASL utilise l’authentification mutuelle, de sorte que les données d’authentification sont renvoyées au dernier appel du serveur ASC au client, qui vérifie que le client communique avec le serveur approprié.

![protocole d’accès Digest](images/digest1.png)

Le processus commence par le client qui demande une ressource protégée par l’accès au serveur en envoyant la requête HTTP 1.

Le serveur reçoit la requête HTTP 1 et détermine que la ressource requiert des informations d’authentification qui n’étaient pas incluses dans la demande. Le serveur génère une demande de test pour le client comme suit :

1.  Le serveur obtient ses [*informations d’identification*](../secgloss/c-gly.md) en appelant la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .
2.  Le serveur génère la stimulation Digest en appelant la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
3.  Le serveur envoie un en-tête de WWW-Authenticate en tant que réponse à la demande du client (indiqué en tant que réponse HTTP 1). L’en-tête contient la stimulation Digest et une directive opaque qui contient une référence à un [*contexte de sécurité*](../secgloss/s-gly.md) partiel établi pour le client. L’en-tête est envoyé avec un code d’état 401 qui indique que la demande du client a généré une erreur d’accès non autorisé. Pour plus d’informations sur la demande de résumé, consultez le [contenu d’une demande de résumé](contents-of-a-digest-challenge.md) et [la génération de la demande de résumé](generating-the-digest-challenge.md).
4.  Le client reçoit une réponse HTTP 1, extrait la stimulation de synthèse envoyée par le serveur et génère une réponse de demande de résumé comme suit :
    1.  Les informations d’identification de l’utilisateur sont obtenues en appelant la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) ou en invitant l’utilisateur à entrer des informations d’identification de manière interactive.
    2.  Les informations sur les informations d’identification et les informations d’identification sont transmises à la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , qui génère la réponse de la stimulation de synthèse.
5.  Le client envoie un en-tête d’autorisation qui contient la réponse de stimulation au serveur (indiqué sous la forme HTTP request 2). Pour plus d’informations sur la réponse à la demande de synthèse, consultez le [contenu d’une réponse de stimulation Digest](contents-of-a-digest-challenge-response.md) et [la génération de la réponse à la stimulation de synthèse](generating-the-digest-challenge-response.md).
6.  Le serveur reçoit la requête HTTP 2, extrait la réponse de stimulation envoyée par le client et authentifie les informations en appelant la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Pour plus d’informations sur le processus d’authentification, consultez [authentification initiale à l’aide de Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  Le serveur envoie la réponse HTTP 2 au client en tant que deuxième et dernière réponse requise par le protocole d’accès Digest. Si l’authentification réussit, cette réponse contient la ressource demandée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contenu d’une réponse de stimulation Digest](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
