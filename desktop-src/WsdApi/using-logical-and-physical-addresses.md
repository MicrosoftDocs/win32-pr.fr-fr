---
description: 'WS-Discovery définit l’adressage logique à l’aide d’URI basés sur le format urn : UUID :.'
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: Utilisation d’adresses logiques et physiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516240"
---
# <a name="using-logical-and-physical-addresses"></a>Utilisation d’adresses logiques et physiques

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) définit l’adressage logique à l’aide d’URI basés sur le `urn:uuid:` format. L’objectif de ce schéma d’adressage est de différencier l’identité de l’appareil de son adresse IP actuelle. Ce schéma fournit essentiellement les fonctionnalités des noms DNS sans nécessiter de serveur de noms. [Devices Profile for Web services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) recommande que les appareils utilisent ce schéma d’adressage.

DPWS recommande également que les services utilisent des adresses physiques (également appelées transport). Cela permet aux clients qui ne prennent pas en charge de manière native WS-Discovery mécanismes d’adressage de communiquer avec les services DPWS. En outre, chaque service peut définir ses adresses, ce qui permet l’adressage au niveau du transport pour les implémentations d’appareils qui gèrent la répartition de service sur une couche inférieure. Enfin, l’utilisation d’adresses physiques optimise l’interopérabilité.

L’inconvénient de l’adressage physique est qu’il complique les implémentations d’appareils, car l’adresse IP ou de transport actuelle doit faire l’objet d’un suivi et les métadonnées de l’appareil doivent être modifiées en conséquence. Pour cette raison, DPWS ne requiert pas de services pour utiliser des adresses de transport.

Si des adresses logiques sont utilisées, il existe des scénarios dans lesquels le comportement de l’implémentation n’est pas défini. La spécification WS-Discovery ne décrit pas ce que signifie pour qu’un service réside à une adresse logique. R1001 de la spécification WS-Discovery recommande d’utiliser WS-Discovery sur les services hébergés en raison de la conversation réseau associée.

Il n’est pas recommandé que les services résident à des adresses logiques, car cela réduit l’interopérabilité. Si une implémentation doit absolument résider à une adresse logique, le service doit utiliser la même adresse logique que l’appareil. Si cela ajoute trop de complexité au modèle de répartition sur l’appareil, la solution recommandée consiste à utiliser des paramètres de référence pour différencier les services. WSDAPI enverra correctement les messages aux services s’ils utilisent la même adresse de point de terminaison que l’appareil.

 

 



