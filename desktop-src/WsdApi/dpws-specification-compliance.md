---
description: Cette rubrique décrit comment WSDAPI implémente les fonctionnalités d’élection dans la spécification de profil de périphériques pour les services Web (DPWS). Elle décrit également les fonctionnalités DPWS qui ont été omises de l’implémentation du WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Conformité de la spécification DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed26e57a0f7a94069e802f96f346a3a5eca67b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517912"
---
# <a name="dpws-specification-compliance"></a>Conformité de la spécification DPWS

Cette rubrique décrit comment WSDAPI implémente les fonctionnalités d’élection dans la spécification de [profil de périphériques pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). Elle décrit également les fonctionnalités DPWS qui ont été omises de l’implémentation du WSDAPI.

La spécification DPWS fournit un moyen cohérent de message avec les appareils. Il ajoute également des restrictions et des recommandations spécifiques qui simplifient le processus de prise en charge des services Web sur du matériel intégré.

La spécification DPWS décrit les fonctionnalités d’élection en utilisant les termes de la recommandation ou de la restriction de l’implémentation. Les fonctionnalités omises peuvent être des fonctionnalités décrites comme requises dans la spécification DPWS qui n’a pas été implémentée par WSDAPI, ou il peut s’agir d’une fonctionnalité qui est implémentée par WSDAPI dans une méthode autre que celle spécifiée dans la spécification DPWS.

Cette rubrique suit la disposition de la section DPWS par section. Chaque section décrit comment des restrictions, exigences et fonctionnalités optionnelles spécifiques sont gérées par l’implémentation du WSDAPI. Cette rubrique est la meilleure lecture en tandem avec la spécification DPWS.

## <a name="dpws-30-messaging"></a>Messagerie DPWS 3,0

### <a name="dpws-31-uri-formats"></a>Formats d’URI DPWS 3,1

Restrictions R0025 et R0027 contraignent les URI sur la taille maximale des \_ \_ octets URI. WSDAPI applique ces deux restrictions comme spécifié.

### <a name="dpws-32-udp-messaging"></a>Messagerie UDP DPWS 3,2

La recommandation R0029 suggère que les paquets UDP plus volumineux que l’unité de transfert maximale (MTU) pour UDP ne doivent pas être envoyés. WSDAPI n’implémente pas cette recommandation et permet aux implémentations d’envoyer et de recevoir des messages de découverte plus volumineux que l’unité MTU.

### <a name="dpws-33-http-messaging"></a>Messagerie HTTP DPWS 3,3

R0001 requiert que les services prennent en charge le transfert en bloc. WSDAPI accepte les données mémorisées en bloc dans les messages de demande et envoie les données mémorisées en bloc dans les messages de requête.

R0012 et R0013 décrivent les parties requises de la liaison HTTP SOAP. Pour R0012, WSDAPI implémente la liaison HTTP SOAP, mais ne commence pas la lecture de la réponse HTTP tant que WSDAPI n’a pas terminé l’envoi de la requête HTTP. WSDAPI implémente le modèle d’échange de messages requis dans R0013, implémente le nœud SOAP répondeur facultatif dans R0014, et n’implémente pas la fonctionnalité de méthode Web facultative dans R0015. WSDAPI prend également en charge les spécifications dans R0030 et R0017.

### <a name="dpws-34-soap-envelope"></a>Enveloppe SOAP DPWS 3,4

WSDAPI prend en charge R0034 et applique R0003 et R0026 par défaut. Plus précisément, conformément à R0003 et R0026, si WSDAPI reçoit une enveloppe SOAP supérieure à la \_ taille d’enveloppe maximale \_ sur http, il est rejeté et la connexion est fermée.

### <a name="dpws-35-ws-addressing"></a>DPWS 3,5 WS-Addressing

R0004 reflète l’utilisation recommandée de l’API d’appareil dans WSDAPI et est prise en charge par l’API cliente dans WSDAPI. Étant donné qu’il s’agit d’une recommandation, WSDAPI permet aux clients et aux appareils d’utiliser des URI autres que `urn:uuid` des URI pour leurs points de terminaison de périphérique afin de garantir une compatibilité maximale. Étant donné que l’API d’appareil dans WSDAPI ne conserve pas l’état entre les initialisations, il revient aux développeurs d’applications qui utilisent l’API d’appareil dans WSDAPI de s’assurer que R0005 et R0006 sont correctement pris en charge. L’API cliente dans WSDAPI suppose que les identités des appareils sont uniques et conservées, et que la fonctionnalité basée sur l’API cliente dans WSDAPI (comme PnP-X) en a besoin pour reconnaître correctement l’appareil lors des redémarrages de l’appareil.

R0007 recommande l’utilisation de propriétés de référence dans les références de point de terminaison. WSDAPI va toujours reconnaître et accepter les points de terminaison avec des propriétés de référence, et les développeurs peuvent choisir de les utiliser, mais par défaut, WSDAPI ne les remplit pas dans les points de terminaison qu’il crée. De même, avec R0042, lorsque WSDAPI crée des points de terminaison de service, il utilise une adresse de transport HTTP ou HTTPs, mais n’exige pas que les appareils utilisent des adresses de transport http ou https dans leurs points de terminaison de service. Le comportement du client lors de la tentative de communication avec un service qui n’utilise pas HTTP ou HTTPs n’est pas défini.

En cas d’erreurs, R0031 limite le point de terminaison de réponse et décrit l’erreur à envoyer si l’erreur n’est pas anonyme. WSDAPI force le point de terminaison de réponse à utiliser la valeur correcte lors de l’envoi des messages, et fonctionne correctement si WSDAPI reçoit un message de demande avec le point de terminaison de réponse incorrect. R0041 permet aux implémentations de supprimer une erreur si le point de terminaison de réponse n’est pas valide. Au lieu de supprimer l’erreur, WSDAPI renvoie la faute sur le canal de demande, adressé au point de terminaison anonyme, en tant que « meilleur effort » pour communiquer avec le client.

Enfin, il existe deux restrictions sur les en-têtes SOAP, R0019 et R0040, qui sont tous les deux conformes à et s’appliquent aux messages reçus.

### <a name="dpws-36-attachments"></a>DPWS 3,6 pièces jointes

WSDAPI prend en charge les pièces jointes et est conforme à R0022. WSDAPI est également conforme à R0037. Lors de l’envoi de pièces jointes, WSDAPI définit toujours l’encodage de transfert de contenu à « binaire » pour toutes les parties MIME. Toutefois, WSDAPI n’applique pas R0036. Le comportement de WSDAPI lors de la réception d’une partie MIME avec un encodage de transfert de contenu non défini sur « Binary » n’est pas défini.

DPWS définit également les clauses de tri des parties MIME. Pour R0038, WSDAPI applique le classement des parties et rejette un message MIME si l’enveloppe SOAP n’est pas la première partie MIME. Pour R0039, WSDAPI enverra toujours l’enveloppe SOAP comme première partie MIME.

## <a name="dpws-40-discovery"></a>Découverte de DPWS 4,0

R1013 et R1001 différencient la découverte des appareils et la découverte du service. WSDAPI est conforme à R1013. L’implémentation de l’hébergement est conforme à R1001, mais WSDAPI n’applique pas cette recommandation sur le client.

DPWS fournit également des conseils sur les types et les règles de correspondance de portée. WSDAPI prend en charge toutes les règles de correspondance d’étendue définies dans [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) , à l’exception de LDAP. WSDAPI fournit également un modèle extensible permettant de définir des règles de correspondance d’étendue personnalisée, ce qui se conforme à R1019. L’API d’hébergement fournira toujours le `wsdp:Device` type dans Discovery par R1020, mais l’API cliente ne requiert pas qu’elle soit présente. D’autres applications basées sur WSDAPI, telles que PnP-X, ont une exigence matérielle pour que le `wsdp:Device` type soit présent dans la découverte.

Pour faciliter la découverte et la liaison, WSDAPI prend en charge R1009 et R1016. Par R1018, WSDAPI ignore le protocole UDP multidiffusion non envoyé à l’adresse anonyme. R1015, R1021 et R1022 définissent une liaison HTTP pour le message de sondage, que WSDAPI prend en charge comme décrit.

## <a name="dpws-50-description"></a>Description de DPWS 5,0

WSDAPI applique R2044 sur le client. Côté hébergement, WSDAPI ne fournira jamais l' `wsx:Metadata` élément dans le corps de l’enveloppe SOAP. R2045 permet aux appareils de prendre en charge un sous-ensemble de la fonctionnalité [WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) . L’API d’hébergement générera toujours l' `wsa:ActionNotSupported` erreur.

### <a name="dpws-51-characteristics"></a>Caractéristiques de DPWS 5,1

DPWS décrit les caractéristiques de base de l’appareil. Outre les restrictions décrites dans cette rubrique, les limites de longueur sont définies pour des chaînes et des URI spécifiques. WSDAPI applique les limites de longueur dans la section 5,1 de la DPWS avant l’envoi du message ou après l’analyse de son contenu.

DPWS décrit également les sections de métadonnées requises et le cycle de la version des métadonnées. L’implémentation du client impose la présence de métadonnées ThisModel et ThisDevice. L’implémentation de l’hébergement gère également correctement la version des métadonnées et fournit toujours ces sections, conformes à R2038, R2012, R2001, R2039, R2014 et R2002.

### <a name="dpws-52-hosting"></a>Hébergement DPWS 5,2

Cette section décrit la hiérarchie des services et les métadonnées de relation. WSDAPI n’impose pas l’unicité du ServiceId comme décrit dans cette section sur le client ou le côté de l’appareil.

WSDAPI est conforme à R2040, et il est possible que l’implémentation d’hébergement envoie une réponse de métadonnées sans section de relation s’il n’y a pas de services hébergés. L’implémentation du client accepte correctement la réponse des métadonnées.

R2029 autorise plusieurs sections de relation dans une réponse de métadonnées, que WSDAPI acceptera correctement. R2030 et R2042 décrivent la gestion de la version des métadonnées, qui est implémentée correctement dans l’API d’hébergement.

### <a name="dpws-53-wsdl"></a>DPWS 5,3 WSDL

Si un service fournit des données Web Services Description Language (WSDL), les implémentations clientes peuvent obtenir la définition du service et manipuler le service à la volée. Utilisé par les clients à liaison tardive. L’implémentation du client WSDAPI accepte le WSDL fourni par un service, mais le client ne le valide pas et le client ne fournit pas de modèle de programmation à liaison tardive. L’implémentation d’hébergement peut être utilisée pour fournir WSDL, mais l’hôte n’est pas obligé de le faire, car les métadonnées de niveau de service ne sont pas gérées par l’hôte lui-même.

### <a name="dpws-54-ws-policy"></a>DPWS 5,4 WS-Policy

DPWS décrit les assertions de stratégie à utiliser pour les appareils. Comme WSDAPI ne fournit pas et n’interprète pas WSDL, il ne peut pas reconnaître et appliquer la stratégie incorporée dans les données WSDL.

## <a name="dpws-60-eventing"></a>Événements DPWS 6,0

### <a name="dpws-61-subscription"></a>Abonnement DPWS 6,1

DPWS requiert la prise en charge de la remise push. WSDAPI implémente la remise Push côté service, qui est conforme à R3009 et R3010, et accepte uniquement le mode de distribution Push côté client. R3017 et R3018 requièrent des erreurs spécifiques du service s’il ne reconnaît pas `NotifyTo` les `EndTo` adresses ou. WSDAPI ne valide pas ces adresses avant et ne génère pas ces erreurs. Toutefois, l’implémentation cliente reconnaîtra ces erreurs correctement. De même, R3019 est facultatif et WSDAPI n’implémente pas cette recommandation, mais l’implémentation du client reconnaît correctement le `SubscriptionEnd` message et notifie l’application d’un échec de remise.

### <a name="dpws-611-filtering"></a>Filtrage DPWS 6.1.1

WSDAPI est conforme à R3008 et implémente le `Action` filtre. En conformité avec R3011 et R3012, WSDAPI ne génère pas les erreurs dans les conditions indiquées. WSDAPI implémente également l’erreur décrite R3020 s’il ne reconnaît pas les actions sur lesquelles il est demandé de filtrer.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Durée et renouvellement de l’abonnement DPWS 6,2

WSDAPI est conforme à R3005, R3006 et R3016. WSDAPI utilisera toujours `xs:duration` , mais acceptera s’il est `xs:dateTime` fourni, et n’émettra donc pas l’erreur facultative dans R3013. WSDAPI prend en charge `GetStatus` et n’émet pas l' `wsa:ActionNotSupported` erreur par R3015. WSDAPI accepte l' `wsa:ActionNotSupported` erreur si un service répond à une `GetStatus` demande.

## <a name="dpws-70-security"></a>DPWS 7,0 sécurité

DPWS décrit un modèle de sécurité recommandé pour les appareils. WSDAPI n’implémente pas ces recommandations comme décrit et n’applique pas les restrictions de cette section comme décrit.

## <a name="dpws-appendix-i"></a>DPWS annexe I

DPWS modifie les constantes globales d’autres spécifications pour les adapter aux appareils. WSDAPI utilise les constantes de cette section et remplace les constantes par défaut de l’implémentation [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) par ces constantes. Les applications qui utilisent WSDAPI pour WS-Discovery sont liées aux constantes définies dans DPWS, et non aux constantes définies dans [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

 

 



