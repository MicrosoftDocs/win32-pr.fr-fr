---
title: Interface (RRAS)
description: Une interface est une connexion logique à un réseau. Chaque interface est identifiée par un index unique. Les protocoles de routage de multidiffusion (tels que MOSPF) traitent tous les types d’interfaces de la même façon.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1347f1a8d9afd049dd8283e7199c6da7d8a9dce6990a1e7ea674943f32811f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030159"
---
# <a name="interface-rras"></a>Interface (RRAS)

Une interface est une connexion logique à un réseau. Chaque interface est identifiée par un index unique. Les protocoles de routage de multidiffusion (tels que MOSPF) traitent tous les types d’interfaces de la même façon.

Dans le cas d’une interface LAN, l’interface correspond à un appareil physique réel de l’ordinateur (la carte LAN). Dans le cas d’une interface de réseau étendu (WAN), l’interface est mappée à un port lorsqu’une connexion est établie. Les interfaces WAN peuvent être basées sur des tunnels et le port peut être un port de réseau privé virtuel (VPN).

les systèmes d’exploitation Windows 2000 et versions ultérieures prennent en charge une interface point-à-multipoint. Ce type d’interface peut être affiché sous la forme d’une collection de liens point à point qui partagent un point de terminaison unique.

Pour identifier de façon unique un lien exact dans une interface point à multipoint, l’API MGM utilise l’adresse de tronçon suivant de l’ID d’interface. Pour prendre en charge cette identification, l’API MGM utilise un ID d’interface étendu, qui comprend une adresse de [tronçon suivant](next-hop.md) .

 

 




