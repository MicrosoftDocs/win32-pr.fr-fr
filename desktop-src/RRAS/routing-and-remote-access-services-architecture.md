---
title: Architecture du Access Services du routage et du service distant
description: l’illustration suivante présente une vue architecturale générale du routeur Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- routage et accès à distance Service rras, routage et Architecture Access Services distante rras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007058"
---
# <a name="routing-and-remote-access-services-architecture"></a>Architecture du Access Services du routage et du service distant

l’illustration suivante présente une vue architecturale générale du routeur Windows 2000.

Les composants spécifiques à la famille de protocoles IP sont affichés en gris clair. Les composants spécifiques à la famille de protocoles IPX sont affichés en gris foncé. Les composants généraux de toutes les familles de protocoles ne sont pas ombrés.

Le service Routage et accès distant fournit des API pour l’administration et la configuration du service. Ces API incluent des agents SNMP pour IP et IPX.

RRAS comprend des protocoles de routage pour IP et IPX. Pour l’adresse IP, le service RRAS fournit les protocoles de routage RIP (Routing Information Protocol) et OSPF (Open Shortest Path First). Pour IPX, RRAS fournit le protocole SAP RIP et service Advertising Protocol (SAP).

RRAS utilise un gestionnaire de tables de routage (RTM) pour les protocoles IP et IPX. Toutefois, chaque famille de protocoles a son propre gestionnaire de routeurs. RRAS possède également un composant séparé pour la gestion des groupes de multidiffusion.

Interfaces DIM (Dynamic interface Manager) avec les services PPP et TAPI afin de gérer les interfaces PPP utilisées par certains itinéraires.

![vue architecturale générale du routeur Windows 2000](images/rtarch.png)

 

 




