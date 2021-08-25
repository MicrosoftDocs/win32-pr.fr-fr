---
description: notions de base sur les protocoles de WSPListen, WSPAccept et WSPConnect pour l’établissement d’une connexion de sockets avec Windows sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'notions de base sur les protocoles : écouter, Connecter, accepter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db73ea4bca5a709ff6d030fcbb44661c6181e552955d02b67d8eb2bcf680bf92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857919"
---
# <a name="protocol-basics-listen-connect-accept"></a>notions de base sur les protocoles : écouter, Connecter, accepter

Les opérations de base nécessaires à l’établissement d’une connexion de socket peuvent être expliquées plus facilement en termes de paradigme client-serveur.

Le côté serveur crée tout d’abord un socket, le lie à une adresse locale connue (afin que le client puisse le trouver) et met le socket en mode d’écoute, par le biais de [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)), afin de se préparer aux demandes de connexion entrantes et de spécifier la longueur de la file d’attente de la connexion. Les fournisseurs de services conservent les demandes de connexion en attente dans une file d’attente de travaux en souffrance jusqu’à ce qu’ils soient traités par le serveur ou soient retirés (en raison d’un délai d’expiration) par le client. Un fournisseur de services peut ignorer silencieusement les demandes d’extension de la taille de la file d’attente des travaux en souffrance au-delà d’une limite supérieure définie par le fournisseur.

À ce stade, si un socket bloquant est utilisé, le côté serveur peut appeler immédiatement [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) , qui se bloque jusqu’à ce qu’une demande de connexion soit en attente. Inversement, le serveur peut également utiliser l’un des mécanismes d’indication d’événement réseau abordé précédemment pour organiser la notification des demandes de connexion entrantes. selon le mécanisme de notification sélectionné, le fournisseur émet un message Windows ou signale un objet d’événement lorsque les demandes de connexion arrivent. Consultez [notification des événements réseau](notification-of-network-events-2.md) pour savoir comment s’inscrire à l' \_ événement réseau d’acceptation FD.

Le côté client crée un socket approprié et initie la connexion en appelant [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)), en spécifiant l’adresse de serveur connue. Les clients n’exécutent généralement pas d’opération de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) explicite avant d’initialiser une connexion, ce qui permet au fournisseur de services d’effectuer une liaison implicite en son nom. Si le socket est en mode blocage, **WSPConnect** se bloque jusqu’à ce que le serveur ait reçu et agi sur la demande de connexion (ou jusqu’à ce qu’un délai d’attente se produise). Dans le cas contraire, le client doit utiliser l’un des mécanismes d’indication d’événement réseau abordé précédemment pour organiser la notification d’une nouvelle connexion établie. selon le mécanisme de notification sélectionné, le fournisseur l’indique à l’aide d’un message de Windows ou en signalant un objet d’événement.

Lorsque le côté serveur appelle [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept), le fournisseur de services appelle la fonction de condition fournie par l’application, à l’aide des paramètres de fonction pour transmettre les informations du serveur à partir de l’entrée supérieure de la file d’attente des demandes de connexion. Ces informations comprennent notamment l’adresse de connexion de l’hôte, les données utilisateur disponibles et les informations de QoS disponibles. À l’aide de ces informations, la fonction condition du serveur détermine s’il faut accepter la demande, rejeter la demande ou retarder la prise d’une décision jusqu’à une date ultérieure. Cette décision est indiquée par la valeur de retour de la fonction condition. Consultez [notification des événements réseau](notification-of-network-events-2.md) pour savoir comment s’inscrire à l' \_ événement réseau FD Connect.

Si le serveur décide d’accepter la demande, le fournisseur doit créer un nouveau socket avec les mêmes attributs et inscriptions d’événements que le socket d’écoute. Le socket d’origine reste à l’état d’écoute afin que les demandes de connexion suivantes puissent être reçues. Grâce aux paramètres de sortie de la fonction condition, le serveur peut également fournir des données utilisateur de réponse et affecter des paramètres de qualité de service (en supposant que ces opérations sont prises en charge par le fournisseur de services).

 

 
