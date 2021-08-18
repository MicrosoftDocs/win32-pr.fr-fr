---
title: Partage de connexion Internet
description: BITS peut forcer une connexion d’accès à distance pour les réseaux familiaux qui utilisent le partage de connexion Internet de Microsoft si le partage de connexion est configuré pour effectuer des appels sortants lorsque les ordinateurs sur le réseau accèdent à Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8736144b74d12666c4a364ac5b644ead35f8d1ec28aa03926bb7b691c8218f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588619"
---
# <a name="internet-connection-sharing"></a>Partage de connexion Internet

BITS peut forcer une connexion d’accès à distance pour les réseaux familiaux qui utilisent le partage de connexion Internet de Microsoft si le partage de connexion est configuré pour effectuer des appels sortants lorsque les ordinateurs sur le réseau accèdent à Internet. Pour empêcher une connexion d’accès à distance forcée, désactivez l’option **établir une connexion d’accès à distance chaque fois qu’un ordinateur de mon réseau tente d’accéder à Internet** sur l’ordinateur hôte de partage de connexion qui partage sa connexion Internet.

Les ordinateurs connectés à l’ordinateur hôte de partage de connexion partent du principe qu’ils disposent d’une connexion réseau, de sorte que le service BITS essaie de transférer les fichiers. Si l’option d’accès à distance est désactivée sur l’ordinateur hôte et que l’ordinateur hôte n’a pas de connexion active, les transferts échouent avec une erreur temporaire. Le service BITS réessaiera périodiquement les transferts.

 

 




