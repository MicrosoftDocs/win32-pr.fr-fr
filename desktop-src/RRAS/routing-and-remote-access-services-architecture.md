---
title: Architecture des services de routage et d’accès à distance
description: L’illustration suivante présente une vue architecturale générale du routeur Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- Routage et accès à distance service RRAS, architecture des services de routage et d’accès à distance RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462343"
---
# <a name="routing-and-remote-access-services-architecture"></a>Architecture des services de routage et d’accès à distance

L’illustration suivante présente une vue architecturale générale du routeur Windows 2000.

Les composants spécifiques à la famille de protocoles IP sont affichés en gris clair. Les composants spécifiques à la famille de protocoles IPX sont affichés en gris foncé. Les composants généraux de toutes les familles de protocoles ne sont pas ombrés.

Le service Routage et accès distant fournit des API pour l’administration et la configuration du service. Ces API incluent des agents SNMP pour IP et IPX.

RRAS comprend des protocoles de routage pour IP et IPX. Pour l’adresse IP, le service RRAS fournit les protocoles de routage RIP (Routing Information Protocol) et OSPF (Open Shortest Path First). Pour IPX, RRAS fournit le protocole SAP RIP et service Advertising Protocol (SAP).

RRAS utilise un gestionnaire de tables de routage (RTM) pour les protocoles IP et IPX. Toutefois, chaque famille de protocoles a son propre gestionnaire de routeurs. RRAS possède également un composant séparé pour la gestion des groupes de multidiffusion.

Interfaces DIM (Dynamic interface Manager) avec les services PPP et TAPI afin de gérer les interfaces PPP utilisées par certains itinéraires.

![vue architecturale générale du routeur Windows 2000](images/rtarch.png)

 

 




