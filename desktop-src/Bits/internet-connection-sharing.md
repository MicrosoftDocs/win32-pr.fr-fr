---
title: Partage de connexion Internet
description: BITS peut forcer une connexion d’accès à distance pour les réseaux familiaux qui utilisent le partage de connexion Internet de Microsoft si le partage de connexion est configuré pour effectuer des appels sortants lorsque les ordinateurs sur le réseau accèdent à Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671426"
---
# <a name="internet-connection-sharing"></a>Partage de connexion Internet

BITS peut forcer une connexion d’accès à distance pour les réseaux familiaux qui utilisent le partage de connexion Internet de Microsoft si le partage de connexion est configuré pour effectuer des appels sortants lorsque les ordinateurs sur le réseau accèdent à Internet. Pour empêcher une connexion d’accès à distance forcée, désactivez l’option **établir une connexion d’accès à distance chaque fois qu’un ordinateur de mon réseau tente d’accéder à Internet** sur l’ordinateur hôte de partage de connexion qui partage sa connexion Internet.

Les ordinateurs connectés à l’ordinateur hôte de partage de connexion partent du principe qu’ils disposent d’une connexion réseau, de sorte que le service BITS essaie de transférer les fichiers. Si l’option d’accès à distance est désactivée sur l’ordinateur hôte et que l’ordinateur hôte n’a pas de connexion active, les transferts échouent avec une erreur temporaire. Le service BITS réessaiera périodiquement les transferts.

 

 




