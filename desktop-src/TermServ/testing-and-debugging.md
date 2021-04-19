---
title: Test et débogage
description: Il y a un \ 0034 ; Echo \ 0034 ; écouteur implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512645"
---
# <a name="testing-and-debugging"></a>Test et débogage

Il existe un écouteur « Echo » implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes. Lorsque vous écrivez le côté serveur d’un module de canal virtuel dynamique (DVC), vous pouvez ouvrir un point de terminaison nommé « ECHO » dans le cadre d’un test rapide. Toute écriture sur un canal instancié à partir de ce point de terminaison entraînera la réception des mêmes données.

Vous pouvez utiliser cette technique pour tester une implémentation d’entrée/sortie (e/s) du module côté serveur, pour mesurer le temps de réponse d’un plug-in client Connexion Bureau à distance (RDC) ou pour mesurer le délai réseau pour le client Connexion Bureau à distance (RDC). Il n’existe aucune limitation quant à la quantité de données qui peuvent être envoyées sur ce canal.

 

 




