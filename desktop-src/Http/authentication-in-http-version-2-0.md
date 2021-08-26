---
title: Authentification (API du serveur HTTP)
description: À partir de la version 2,0, l’API du serveur HTTP effectue l’authentification côté serveur pour l’application.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4e3c35dc4e244fd51af42bb3c52d225d233364f61fc79a8127ef450e84016fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078359"
---
# <a name="authentication-http-server-api"></a>Authentification (API du serveur HTTP)

Certaines applications serveur requièrent l’authentification du client pour accéder aux ressources et traiter les requêtes HTTP. À partir de la version 2,0, l’API du serveur HTTP effectue l’authentification côté serveur pour l’application. Dans la version 1,0 de l’API du serveur HTTP, l’application serveur devait implémenter sa propre authentification. Les avantages de l’authentification effectuée par l’API du serveur HTTP sont les suivants :

-   Les applications peuvent s’exécuter sous des privilèges faibles, réduisant ainsi les risques de sécurité.
-   L’authentification est effectuée en mode noyau, ce qui réduit les transitions du mode utilisateur au mode noyau lors de l’authentification.
-   L’authentification effectuée en mode noyau permet aux applications serveur de s’exécuter sur différents comptes d’utilisateur. Dans la version 1,0, toutes les applications de l’ordinateur doivent s’exécuter sous le même compte d’utilisateur pour s’authentifier sur le nom de principal du service (SPN).
-   La négociation d’authentification NTLM n’est pas réinitialisée si un processus de travail est recyclé alors que le protocole de transfert est en cours.

Pour tirer parti de l’authentification 2,0 de la version, l’application active les schémas d’authentification que l’API du serveur HTTP applique aux URL pour lesquelles l’application s’est inscrite. L’authentification peut être activée sur la session ou le groupe d’URL du serveur. Le groupe d’URL hérite des schémas d’authentification activés par la session serveur si aucun n’est défini sur le groupe d’URL. L’API du serveur HTTP prend en charge les schémas suivants :

-   Negotiate
-   NTLM
-   Digest
-   De base

L’application serveur peut également implémenter des schémas d’authentification non pris en charge par l’API du serveur HTTP. L’API du serveur HTTP envoie des demandes à l’application pour les schémas d’authentification qui ne sont pas pris en charge, ou pour les schémas qui n’ont pas été activés par l’application.

### <a name="enabling-authentication"></a>Activation de l'authentification

L’application serveur Active et configure l’authentification sur la session serveur ou le groupe d’URL avec les fonctions [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) comme suit :

1.  L’application active l’authentification en spécifiant **HttpServerAuthenticationProperty** dans le paramètre *Property* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  L’application spécifie les paramètres de configuration dans la structure des [**\_ \_ \_ informations d’authentification du serveur http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) dans le paramètre *pPropertyInformation* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). L’application spécifie les schémas d’authentification activés, si la mise en cache des informations d’identification NTLM est désactivée et fournit les paramètres de base et Digest dans la structure des **\_ \_ \_ informations d’authentification du serveur http** .

### <a name="authentication-procedure"></a>Procédure d’authentification

Pour lancer l’authentification du serveur HTTP, l’application active la propriété d’authentification avant l’arrivée de la première requête dans la file d’attente des demandes. Les étapes suivantes sont le processus de traitement courant pour l’authentification d’une demande.

1.  L’application active l’authentification. Consultez la section « activation de l’authentification » précédente.
    > [!Note]  
    > Le client envoie une demande non authentifiée. L’API du serveur HTTP transmet la requête à l’application serveur et lui permet de générer le défi initial 401. L’API du serveur HTTP comprend la structure d’informations d’authentification de la [**\_ requête \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) incorporée avec la structure de la [**\_ requête http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) . Le membre **AuthStatus** indique **HttpAuthStatusNotAuthenticated**

     

2.  L’application examine le membre **AuthStatus** de la structure [**d' \_ \_ \_ informations d’authentification de la requête http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) pour déterminer si la requête a été authentifiée. Si la demande n’a pas été authentifiée, l’application peut traiter la demande comme anonyme ou envoyer une demande d’authentification initiale 401.
3.  Si l’application traite la demande comme anonyme, elle gère la requête et envoie la réponse finale à l’application cliente, comme si l’authentification n’était pas impliquée.
4.  Si, à la place, l’application requiert une authentification, elle envoie le défi initial 401 avec un ou plusieurs en-têtes WWW-Authenticate indiquant les schémas disponibles au client. L’application doit utiliser la structure [**http de \_ plusieurs \_ \_ en-têtes connus**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) pour générer le jeu d’en-têtes requis lorsque plusieurs en-têtes d’authentification sont envoyés dans la réponse.
    > [!Note]
    >
    > Le client renvoie la demande avec l’en-tête Authorization pour un schéma sélectionné à partir de l’ensemble de schémas disponibles indiqué par l’application serveur dans la réponse initiale 401.
    >
    > L’API du serveur HTTP examine l’en-tête d’autorisation de demande d’autorisation pour déterminer si le schéma est activé. Si c’est le cas, l’API du serveur HTTP effectue l’authentification et gère tous les échanges de demande/401-Response intermédiaires, jusqu’à ce que le protocole de transfert d’authentification soit finalisé.
    >
    > Lorsque l’API du serveur HTTP termine la tentative d’authentification, elle envoie la demande à l’application avec les résultats de la tentative d’authentification dans la structure d' [**\_ \_ \_ informations**](/windows/desktop/api/Http/ns-http-http_request_auth_info) d’authentification de la requête HTTP qui est retournée avec la requête. Si la tentative d’authentification échoue pour l’une des raisons suivantes, l’API du serveur HTTP ne transmet pas la demande à l’application :
    >
    > -   Si la négociation d’authentification échoue en raison d’une erreur de l’API du serveur HTTP interne, telle qu’un échec d’allocation de mémoire, l’API du serveur HTTP génère une réponse 503 (service non disponible) et renvoie au client.
    > -   Si un en-tête d’autorisation incorrect, tel qu’un en-tête sans nom de schéma, ou un encodage en base64 incorrect des informations d’identification du client, est généré, l’API du serveur HTTP génère une réponse 400 (requête incorrecte) et renvoie au client.

     

5.  L’application serveur examine le membre **AuthStatus** de la structure [**d' \_ \_ \_ informations d’authentification de la requête http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) pour déterminer si l’authentification a réussi. En cas d’échec de l’authentification, l’API du serveur HTTP comprend l’erreur retournée par [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) dans le membre **SecStatus** de la structure d’informations d’authentification de la **\_ requête \_ \_ http** . Si la tentative d’authentification échoue en raison d’informations d’identification incorrectes, l’application peut générer un autre défi 401 avec l’en-tête de WWW-Authenticate souhaité, ou peut décider de traiter la demande comme anonyme.
6.  Si l’authentification a réussi, l’application utilise le jeton fourni dans la structure des informations d’authentification de la [**\_ requête \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) pour emprunter l’identité du client et pour accéder aux ressources. Le handle de jeton d’accès retourné à l’application est valide tant que l’ID de demande est valide, ce qui est généralement jusqu’à ce que l’application termine la réponse à la demande. Toutefois, le jeton peut expirer pendant cette période et l’application peut être amenée à envoyer une autre demande 401 au client.
7.  L’application envoie la réponse finale 200 OK et doit fermer le descripteur du jeton d’accès.
    > [!Note]  
    > L’API du serveur HTTP ajoute les données d’authentification mutuelle à la réponse finale 200 OK, si une réponse a été générée lors de la négociation d’authentification.

     

### <a name="ntlm-null-sessions"></a>Sessions NTLM NULL

Notez qu’une session NTLM NULL indiquée dans le contexte de sécurité final n’est pas traitée comme authentifiée. Dans ce cas, la demande est envoyée à l’application avec une erreur HttpAuthStatusFailure dans la structure des informations d’authentification de la [**\_ requête \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) et l’application peut envoyer une autre demande 401.

### <a name="preemptive-authentication"></a>Authentification préemptive

D’après le protocole HTTP, une fois que le client a établi l’authentification pour une ressource, il peut, de manière préventive, envoyer l’en-tête d’autorisation correspondant avec les demandes consécutives ultérieures pour la ressource sans attendre un défi 401 du serveur. Si le schéma indiqué dans l’en-tête d’autorisation est toujours activé par l’application et pris en charge par l’API du serveur HTTP, le serveur HTTP tente une authentification sans envoyer la demande à l’application. Lorsque ce type de demande authentifiée est reçu par l’application, il peut choisir d’ignorer la demande et de régénérer le défi initial 401 ou de traiter la demande comme étant authentifiée.

### <a name="mutual-authentication"></a>Authentification mutuelle

Les données d’authentification mutuelle sont générées lorsque le schéma Negotiate est utilisé pendant le protocole de transfert et qu’il est résolu en Kerberos et que le client a demandé une authentification mutuelle. Les données d’authentification mutuelle sont insérées automatiquement par l’API du serveur HTTP dans la dernière réponse 200 OK envoyée par l’application serveur. Par défaut, l’API du serveur HTTP ne transmet pas les données d’authentification mutuelle à l’application serveur, car elle gère automatiquement l’envoi de celle-ci. Toutefois, si l’application serveur Active l’indicateur ReceiveMutualAuth dans la structure des [**\_ \_ \_ informations d’authentification du serveur http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) dans la configuration, les données d’authentification mutuelle sont transmises à l’application dans la structure des informations d’authentification de la [**\_ requête \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) incorporée à la [**\_ requête http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))authentifiée. Dans ce cas, l’application doit envoyer les données d’authentification mutuelle avec la réponse 200 OK finale. Dans le cas où plusieurs sites sont pris en charge par un seul ordinateur, tous les sites sur l’ordinateur utilisent les informations d’identification du compte de l’ordinateur local dans le domaine pour l’authentification mutuelle.

 

 
