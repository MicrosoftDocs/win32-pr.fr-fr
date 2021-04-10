---
title: Interface (RRAS)
description: Une interface est une connexion logique à un réseau. Chaque interface est identifiée par un index unique. Les protocoles de routage de multidiffusion (tels que MOSPF) traitent tous les types d’interfaces de la même façon.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103941566"
---
# <a name="interface-rras"></a>Interface (RRAS)

Une interface est une connexion logique à un réseau. Chaque interface est identifiée par un index unique. Les protocoles de routage de multidiffusion (tels que MOSPF) traitent tous les types d’interfaces de la même façon.

Dans le cas d’une interface LAN, l’interface correspond à un appareil physique réel de l’ordinateur (la carte LAN). Dans le cas d’une interface de réseau étendu (WAN), l’interface est mappée à un port lorsqu’une connexion est établie. Les interfaces WAN peuvent être basées sur des tunnels et le port peut être un port de réseau privé virtuel (VPN).

Les systèmes d’exploitation Windows 2000 et versions ultérieures prennent en charge une interface point-à-multipoint. Ce type d’interface peut être affiché sous la forme d’une collection de liens point à point qui partagent un point de terminaison unique.

Pour identifier de façon unique un lien exact dans une interface point à multipoint, l’API MGM utilise l’adresse de tronçon suivant de l’ID d’interface. Pour prendre en charge cette identification, l’API MGM utilise un ID d’interface étendu, qui comprend une adresse de [tronçon suivant](next-hop.md) .

 

 




