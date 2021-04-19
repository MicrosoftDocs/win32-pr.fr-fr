---
title: Authentification avec plusieurs en-têtes connus
description: La \_ structure http \_ avec plusieurs \_ en-têtes connus permet aux applications serveur d’envoyer plusieurs défis d’authentification au client.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8afbce3c2a41ea143003723acebc7eb83dc463d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510607"
---
# <a name="authentication-with-multiple-known-headers"></a>Authentification avec plusieurs en-têtes connus

La structure [**http avec \_ plusieurs \_ \_ en-têtes connus**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) permet aux applications serveur d’envoyer plusieurs défis d’authentification au client. Les applications peuvent défier le client avec un seul schéma d’authentification en fournissant le type d’énumération **HttpHeaderWwwAuthenticate** dans le membre **KnownHeaders** de la structure des [**\_ \_ en-têtes de réponse http**](/windows/desktop/api/Http/ns-http-http_response_headers) contenue dans la [**\_ réponse http**](http-response.md). Toutefois, lorsque le serveur rencontre plusieurs schémas d’authentification, l’application utilise la structure [**http de \_ plusieurs \_ \_ en-têtes connus**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) pour fournir les types d’authentification.

Lorsque les **\_ indicateurs d' \_ informations \_ \_ \_ de réponse HTTP** sont présents, le protocole http envoie les en-têtes d’authentification dans l’ordre spécifié. Si l’indicateur n’est pas présent, HTTP trie les schémas d’authentification de la plus forte à la plus faible, comme suit :

1.  Negotiate
2.  NTLM
3.  Digest
4.  De base

Si le schéma d’authentification n’est pas l’un de ces schémas, l’application doit spécifier l’indicateur de l' **ordre de conservation des indicateurs d' \_ informations de réponse \_ \_ \_ \_ http** .

Le membre **KnownHeader** de [**\_ plusieurs \_ \_ en-têtes connus http**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) pointe vers un tableau de structures d' [**\_ \_ en-tête connues http**](/windows/desktop/api/Http/ns-http-http_known_header) . Le membre **pRawValue** de la structure d' **\_ \_ en-tête connu http** doit pointer vers une chaîne qui spécifie le nom du schéma. HTTP analyse la chaîne pour déterminer le schéma et effectue l’une des actions suivantes :

-   Si la chaîne contient un type d’authentification inconnu ou si le type d’authentification n’est pas activé sur le groupe de configuration (le groupe d’URL ou la session serveur) associé à la demande, l’API du serveur HTTP ajoute la chaîne dans **pRawValue** à l’en-tête WWW-Authenticate. Par exemple, si l’application spécifie un schéma d’authentification non pris en charge et que **pRawValue** contient la chaîne « CustomAuthString », le texte suivant est ajouté à l’en-tête d’authentification :

    WWW-Authenticate : CustomAuthSchemeCRLF

    Si l’authentification de base n’est pas activée pour l’application et que **pRawValue** contient la chaîne « Basic Realm = "BasicRealm »», l’en-tête d’authentification contient le texte suivant :

    WWW-Authenticate : Basic Realm = "BasicRealm"

-   Si la chaîne contient un type d’authentification connu et qu’elle est présente dans le groupe de configuration (le groupe d’URL ou la session serveur) associé à la demande, l’API du serveur HTTP génère l’en-tête WWW-Authenticate. Par exemple, si la chaîne spécifiée dans **pRawValue** est « Digest » et que Digest est activé sur la session serveur, l’API du serveur http ajoute le texte suivant à l’en-tête d’authentification :

    WWW-Authenticate : condensé Realm = " testrealm@host.com "

Si le schéma dans le membre **pRawValue** de [**l' \_ \_ en-tête connu http**](/windows/desktop/api/Http/ns-http-http_known_header) est Negotiate ou NTLM, le nom du schéma d’authentification est suffisant. Si le schéma spécifié est de base, le nom du domaine est ajouté au nom du schéma ; l’application n’a pas besoin de fournir le nom de domaine dans **pRawValue**. Si le schéma spécifié est Digest, HTTP appelle [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) pour générer la stimulation qui est ajoutée au nom du schéma. Les paramètres du schéma de base (domaine) et du schéma condensé (domaine et nom de domaine) sont obtenus à partir des informations d’authentification du groupe de configuration correspondantes.

Lorsque l’application envoie plusieurs défis d’authentification au client dans des en-têtes de demande inconnus, l’API du serveur HTTP les envoie au client sans intervention. Toutefois, cette utilisation n’est pas recommandée.

 

 




