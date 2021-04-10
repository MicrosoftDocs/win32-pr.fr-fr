---
title: Nouveautés de l’API du serveur HTTP version 2,0
description: Les fonctionnalités suivantes sont disponibles dans l’API du serveur HTTP version 2,0.
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- Nouveautés de l’API du serveur HTTP version 2,0
- API de la version 2,0 du serveur HTTP, nouveautés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028827"
---
# <a name="whats-new-for-http-server-version-20-api"></a>Nouveautés de l’API du serveur HTTP version 2,0

L’API du serveur HTTP version 2,0 ajoute des objets de configuration des propriétés et une gestion avancée des files d’attente des requêtes. Pour plus d’informations et pour obtenir une liste complète des fonctions, consultez la rubrique de référence sur le [serveur http Version 2,0](http-server-api-version-2-0-reference.md) . Les fonctionnalités suivantes sont disponibles dans l’API du serveur HTTP version 2,0.

## <a name="configuration-objects"></a>Objets de configuration

Les objets de configuration de session et de groupe d’URL du serveur permettent aux applications de configurer le service HTTP. La session serveur est l’objet de configuration de niveau supérieur qui remplace les paramètres par défaut de l’API du serveur HTTP pour tous les groupes d’URL créés dans le cadre de la session. Le groupe d’URL, créé dans le cadre d’une session de serveur, gère un ensemble d’URL qui reçoivent les paramètres de configuration du groupe. Pour plus d’informations, consultez la rubrique relative à l' [architecture http Version 2,0](http-version-2-0-architecture.md) .

## <a name="property-configuration-in-version-20"></a>Configuration de la propriété dans la version 2,0

La configuration est effectuée sur la session serveur, ou sur les objets de groupe d’URL. Les configurations à l’ensemble du serveur sont définies sur l’objet de configuration de session du serveur. Les groupes d’URL, créés dans le cadre de la session serveur, héritent des configurations de session du serveur. Les configurations définies sur le groupe d’URL remplacent les configurations de session du serveur. Les configurations qui peuvent être définies par l’application incluent les délais d’attente de connexion, les limites de connexion, l’authentification et la journalisation. Pour plus d’informations, consultez la rubrique [Configuration des propriétés dans la version HTTP 2,0](configuring-properties-in-http-version-2-0.md) .

## <a name="process-isolation-on-request-queues"></a>Isolation des processus sur les files d’attente des requêtes

La file d’attente de demandes de la version 2,0 prend en charge l’isolation des processus, ce qui permet à plusieurs processus de travail d’effectuer des e/s sur la file Les propriétés de configuration définies sur la file d’attente des demandes permettent aux applications d’avoir davantage de contrôle sur le service. La fonctionnalité de file d’attente des demandes nommée permet aux applications de créer des files d’attente de requêtes et de les sécuriser avec des listes de Access Control. Les applications fonctionnant sous des comptes d’utilisateurs autres que le compte qui a créé la file d’attente des demandes peuvent ouvrir la file d’attente des demandes, recevoir des demandes et envoyer des réponses. Pour plus d’informations, consultez la rubrique [isolation des processus](process-isolation.md) .

## <a name="full-kernel-mode-ssl"></a>SSL en mode noyau complet

La sécurité SSL en mode noyau est activée par défaut. les certificats clients pour l’authentification mutuelle sont également pris en charge. Les performances sont augmentées en effectuant des opérations SSL en mode noyau, ce qui réduit les transitions entre le noyau et le mode utilisateur. Pour plus d’informations, consultez la rubrique [SSL en mode noyau](kernel-mode-ssl.md) .

## <a name="kernel-mode-response-cache"></a>Cache de réponse en mode noyau

Les réponses avec un contenu statique peuvent être mises en cache en mode noyau, ce qui améliore les performances par rapport au cache du mode utilisateur. La structure de la stratégie de cache est envoyée avec la réponse. Pour plus d’informations, consultez la rubrique [cache en mode noyau dans HTTP 2,0](kernel-mode-cache-in-http-2-0.md) .

## <a name="authentication"></a>Authentification

La \_ réponse http et les \_ structures de requête HTTP sont mises à jour pour inclure les informations d’authentification. L’authentification côté serveur est prise en charge pour les schémas suivants : Negotiate, NTLM, Basic et Digest. Les applications peuvent spécifier les schémas d’authentification pris en charge et définir l’ordre de préférence pour ces schémas.

## <a name="object-scoped-versioning"></a>Contrôle de version avec étendue des objets

L’API du serveur HTTP version 1,0 a passé les informations sur la version dans l’appel à HTTPInitialize. La version a été définie globalement pour toutes les applications dans le même processus. Dans l’API du serveur HTTP version 2,0, les informations de version sont fournies lors de la création de l’objet. Pour plus d’informations, consultez contrôle [de version dans l’API du serveur http version 2,0](versioning-in-http-2-0.md).

## <a name="logging"></a>Journalisation

À partir de la version 2,0, la journalisation peut être configurée via l’API du serveur HTTP. La journalisation activée sur une session serveur sert de forme centralisée de journalisation pour le service. La journalisation peut également être activée sur un groupe d’URL pour les fichiers journaux individualisés. L’application spécifie le format des fichiers journaux, ainsi que les champs consignés pour les erreurs et les transactions réussies.

## <a name="graceful-request-queue-shutdown"></a>Arrêt normal de la file d’attente des demandes

Les applications peuvent arrêter la file d’attente de demandes et gérer gracieusement les demandes en suspens dans la file d’attente avant de mettre fin au processus de la file d’attente des demandes. Lorsque la file d’attente des demandes est arrêtée, l’API du serveur HTTP arrête la mise en file d’attente des demandes et réachemine les demandes en suspens dans la file d’attente des demandes.

## <a name="demand-start-on-a-request-queue"></a>Démarrage à la demande dans une file d’attente de demandes

La fonctionnalité de démarrage à la demande dans la file d’attente de demandes permet à l’application de contrôleur de retarder l’instanciation du processus de travail jusqu’à ce que la première requête arrive dans la file d’attente Ainsi, les applications peuvent éviter de consommer des ressources jusqu’à ce qu’elles soient nécessaires. Pour plus d’informations, voir la rubrique [Demand Start on Version 2,0 Request queues](demand-start-on-version-2-0-request-queues.md) .

## <a name="port-sharing"></a>Partage de port

Les applications basées sur l’API du serveur HTTP partagent automatiquement l’espace d’écoute IP avec d’autres applications basées sur l’API serveur non-HTTP sur l’ordinateur. la liste d’écoutes IP n’est plus nécessaire. Lorsque l’application enregistre une URL, l’API du serveur HTTP écoute uniquement l’adresse IP et la paire de ports spécifiées.

## <a name="etw-support"></a>Prise en charge ETW

Le suivi avancé à l’aide du Suivi d’v nements pour Windows (ETW) permet aux applications de plus grandes capacités de diagnostic. Le suivi d’événements est disponible pour les inscriptions et réservations d’URL, la configuration de propriété, les événements de cache, l’authentification et la journalisation pour n’en nommer que quelques-uns.

## <a name="performance-counters"></a>Compteurs de performance

L’outil compteur de performances permet aux applications de récupérer des compteurs de service et de diagnostiquer les performances du service. Les compteurs globaux suivent les performances du service, les compteurs de site suivent les performances du groupe d’URL et les compteurs de la file d’attente des demandes pour suivre les performances de la file d’attente des demandes.

## <a name="international-domain-names-idn"></a>Noms de domaine internationaux (IDN)

Les portions d’hôte et de chemin d’accès internationalisées de l’URL autorisent l’inscription des chemins d’accès et des noms de domaine non-ASCII. L’API du serveur HTTP traite les URL Unicode pour se conformer aux normes IDN.

## <a name="netsh-extensions"></a>Extensions NetSH

L’utilitaire netsh remplace l’outil HttpCfg.exe disponible dans Windows Server 2003 et Windows XP Service Pack 2 (SP2). L’extension netsh fournit un moyen de gérer, de diagnostiquer et de configurer le service HTTP. Les administrateurs peuvent interroger et configurer des paramètres au niveau du serveur, tels que les inscriptions d’espaces de noms et les certificats SSL.

 

 




