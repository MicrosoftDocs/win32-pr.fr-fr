---
description: 'En savoir plus sur : WS-Discovery spécification de la spécification'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: Conformité de la spécification WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07794140f05a065fb770ae2d5782f24180fb7e7ef66757278d5c5c93a3fd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991409"
---
# <a name="ws-discovery-specification-compliance"></a>Conformité de la spécification WS-Discovery

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) décrit comment effectuer les tâches suivantes :

-   Annoncer la disponibilité des services sur le sous-réseau local
-   Rechercher des services sur le sous-réseau
-   Localiser un service précédemment référencé

Pour ce faire, WS-Discovery définit des messages 2 1 à sens unique, [Hello](hello-message.md) et [Bye](bye-message.md)et deux messages de recherche bidirectionnelle, de [sondage](probe-message.md) et de [résolution](resolve-message.md).

WS-Discovery fournit également des adresses et un port réservé pour la détection locale des liaisons IPv4 et IPv6. La spécification permet également de définir d’autres liaisons à d’autres endroits, telles que la sonde sur la liaison HTTP définie dans le [Profil appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).

La spécification de WS-Discovery décrit les fonctionnalités d’élection en utilisant les termes de la recommandation ou de la restriction de l’implémentation. Les fonctionnalités omises peuvent être des fonctionnalités décrites comme requises dans la spécification WS-Discovery qui n’a pas été implémentée par WSDAPI, ou il peut s’agir d’une fonctionnalité qui est implémentée par WSDAPI dans une méthode autre que celle spécifiée dans la spécification WS-Discovery.

Cette rubrique décrit comment WS-Discovery restrictions, exigences et fonctionnalités d’élection sont gérées par l’implémentation du WSDAPI. Cette rubrique est la meilleure lecture en tandem avec la spécification WS-Discovery.

## <a name="ws-discovery-and-soap-over-udp-support"></a>Prise en charge de la WS-Discovery et de SOAP sur UDP

Dans SOAP-sur-UDP, la section 3,2 spécifie que le message UDP doit tenir dans un datagramme 64 Ko. WSDAPI accepte les messages UDP 64 Ko, mais la contrainte DPWS de \_ taille maximale d’enveloppe \_ (32 Ko) limite la taille du message. Comme requis par [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), wsdapi prend en charge les modèles de message décrits dans la section 4.

WSDAPI peut être configuré pour prendre en charge le modèle de sécurité dans les sections 7 et 8. Lorsque cette configuration est configurée, WSDAPI signe les messages de WS-Discovery sortants et valide les signatures des messages entrants.

WSDAPI implémente l’algorithme de retransmission défini dans l’annexe I, tel que modifié par DPWS annexe I.

Dans WS-Discovery, WSDAPI utilise les adresses spécifiées dans la section 2,4. WSDAPI étend \_ \_ le délai maximal de l’application à partir de la section 2,4, mais pas dans l’étendue définie dans DPWS annexe I. Pour plus d’informations sur \_ le \_ délai max. d’application, voir [fonctionnalités de WS-Discovery supplémentaires](additional-ws-discovery-functionality.md).

WS-Discovery décrit la `uuid:` recommandation de format d’URI dans la section 2,6, mais wsdapi remplace cette recommandation. Au lieu de cela, WSDAPI utilise le `urn:uuid:` format d’URI décrit dans DPWS.

La section 3 de WS-Discovery décrit comment un client interagit avec un proxy de découverte. WSDAPI ne reconnaît pas cette interaction et ignore les annonces des proxys de découverte. dans Windows 7, WSDAPI implémente une extension privée dans le protocole WS-Discovery, WS-Discovery les Extensions distantes, pour permettre aux clients de découverte de rechercher des services répartis sur différents réseaux en envoyant des demandes à des proxys centralisés. Pour plus d’informations, consultez [fonctionnalités de WS-Discovery supplémentaires](additional-ws-discovery-functionality.md).

La section 4,1, paragraphe 3 de WS-Discovery requiert qu’un minuteur doive s’écouler avant l’envoi d’un message de [salutation](hello-message.md) . L’API d’hébergement n’attend pas avant l’envoi d’un message de salutation. Si un scénario nécessite un délai avant l’envoi d’un message de salutation, le développeur de l’application doit implémenter une attente.

WSDAPI implémente tous les messages décrits dans WS-Discovery sections 4, 5 et 6. WSDAPI applique également le délai de correspondance \_ décrit dans la section 7, tel que modifié par DPWS annexe I. wsdapi protège uniquement contre la « relecture » des considérations sécurisées de la section 9.

WSDAPI implémente le séquencement d’application comme décrit dans WS-Discovery annexe I.

 

 



