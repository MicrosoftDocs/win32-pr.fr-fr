---
title: Composants de l’architecture du routeur
description: La documentation d’administration de routeur fait souvent référence aux composants suivants du routeur.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- routeurs RRAS, composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f39f104e001db99076dcd29d9d5b603d5cf9f3c526d54cd16e1ed0e4d10c575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791593"
---
# <a name="components-of-the-router-architecture"></a>Composants de l’architecture du routeur

La documentation d’administration de routeur fait souvent référence aux composants suivants du routeur.

Gestionnaire d’interface dynamique (DIM)

Toutes les fonctions d’administration de routeur passent par DIM. Selon la nature de la fonction, DIM peut passer l’appel à l’un des gestionnaires de routeur. Les fonctions qui traitent uniquement les interfaces sont gérées par DIM. Si la fonction affecte les protocoles de routage, DIM appelle le gestionnaire de routeur pour le transport correspondant à ce protocole. Par exemple, si la fonction affecte le protocole OSPF (Open Shortest Path First), DIM appellera dans le gestionnaire de routeur IP, puisque OSPF est un protocole de routage IP.

Gestionnaires de routeur

Chaque transport routable qui s’adapte à l’architecture du routeur a son propre gestionnaire de routeur. Actuellement, les gestionnaires de routeur existent pour les transports IP et IPX. Les gestionnaires de routeur gèrent les protocoles de routeur et d’autres types de clients de routage qui s’exécutent sur les interfaces sur l’ordinateur local.

Protocoles de routage et autres clients

Les clients sont des fournisseurs de services qui fonctionnent dans le cadre de l’architecture du routeur. Les protocoles de routage sont un type de client pris en charge par le routeur.

Les clients sont spécifiques à un transport routable particulier : IP ou IPX. Les protocoles de routage pour le transport IP incluent le protocole OSPF (Open Shortest Path First) et le protocole RIP (Routing Information Protocol). Les protocoles SAP (Service Advertising Protocol) et RIP pour IPX sont des exemples de protocoles de routage IPX. Par exemple, un client qui n’est pas un protocole de routage est la traduction d’adresses réseau (NAT) pour l’adresse IP.

L’interface entre le gestionnaire de routeur et un client est décrite dans la section [interface de protocole de routage](about-routing-protocol-interface.md). Tous les clients sont conformes à cette interface. À l’aide de cette interface, les fournisseurs peuvent implémenter leurs propres clients qui sont compatibles avec le routeur.

[Interfaces](interfaces.md)

Une interface est une connexion à un réseau externe. Chaque interface est identifiée par un *index* d’interface unique. Les interfaces sont des entités logiques ; les clients de routeur tels que NAT ou OSPF traitent tous les types d’interfaces de la même façon. Toutefois, en termes d’implémentation, une interface peut représenter une connexion dédiée (par exemple, à un réseau local (LAN)) ou une connexion d’accès à distance non dédiée (par exemple, une connexion PPP à un réseau étendu).

Dans le cas d’une interface LAN, l’interface correspond à un appareil physique réel de l’ordinateur, une carte réseau. Dans le cas d’une interface de réseau étendu (WAN), l’interface est mappée à un port au moment où une connexion est établie. Il peut s’agir d’un port COM, d’un port parallèle ou d’un port virtuel (pour les tunnels tels que PPTP et L2TP).

Les interfaces de réseau étendu ont une qualité supplémentaire qu’elles reçoivent généralement une adresse réseau uniquement au moment où une connexion est établie. Par exemple, une interface WAN utilisant PPP reçoit son adresse de couche réseau de l’homologue distant pendant le processus de connexion. La réception d’une adresse réseau dans le cadre du processus de connexion est parfois appelée *liaison tardive*.

 

 




