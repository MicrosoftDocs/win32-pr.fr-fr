---
description: Schannel prend en charge les versions 1,0, 1,1 et 1,2 du protocole TLS (Transport Layer Security).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocole TLS (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532140"
---
# <a name="transport-layer-security-protocol"></a>Protocole TLS (Transport Layer Security)

Schannel prend en charge les versions 1,0, 1,1 et 1,2 du [*protocole TLS (Transport Layer Security)*](../secgloss/t-gly.md). Ce protocole est une norme de l’industrie conçue pour protéger la confidentialité des informations communiquées sur Internet. TLS suppose qu’un transport orienté connexion, généralement TCP, est en cours d’utilisation. Le protocole TLS permet aux applications client/serveur de détecter les risques de sécurité suivants :

-   Falsification des messages
-   Interception des messages
-   Falsification de message

La spécification complète du protocole TLS est disponible sur le site Web IETF : [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organisation du protocole TLS

Les étapes suivantes sont impliquées dans l’utilisation du protocole TLS pour la communication client/serveur :

 **Pour utiliser TLS pour la communication client/serveur**

1.  Négociation de la suite de négociation et de la suite de chiffrement
2.  Authentification des tiers
3.  Échange d’informations relatives aux clés
4.  Échange de données d’application

Les étapes qui composent TLS sont divisées en deux protocoles qui, ensemble, assurent la sécurité de la connexion :

-   [Protocole de négociation TLS](tls-handshake-protocol.md)— (étapes 1 à 3)
-   [Protocole d’enregistrement TLS](tls-record-protocol.md)— (étape 4)

## <a name="sspi-with-tls-implementations"></a>Implémentations SSPI avec TLS

Dans la mesure où TLS n’a pas de spécification GSSAPI, les implémenteurs TLS ne sont peut-être pas familiers avec les fonctions SSPI. Les applications appellent les fonctions SSPI pour énumérer les packages disponibles, créer et utiliser des handles pour les informations d’identification, créer des contextes de sécurité et garantir la confidentialité de l’intégrité des messages.

Pour prendre en charge les fonctions SSPI utilisées par les applications en mode utilisateur, les fonctions listées dans les [fonctions implémentées par SSP/APS en mode utilisateur](/windows/desktop/SecAuthN/authentication-functions) doivent être prises en charge par les implémentations TLS, telles que schannel.dll.

Pour plus d’informations sur les fonctions SSPI et les fonctions SSP, consultez [fonctions d’authentification](authentication-functions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Suites de chiffrement TLS](tls-cipher-suites.md)
</dt> <dt>

[TLS et SSL](tls-versus-ssl.md)
</dt> </dl>

 

 
