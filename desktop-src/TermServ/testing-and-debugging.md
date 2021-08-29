---
title: Test et débogage
description: Il y a un \ 0034 ; Echo \ 0034 ; écouteur implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cacabf8f30772fa654a1fefc24ff8059ff5e002cde8f633537ce8f2f07f068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987039"
---
# <a name="testing-and-debugging"></a>Test et débogage

Il existe un écouteur « Echo » implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes. Lorsque vous écrivez le côté serveur d’un module de canal virtuel dynamique (DVC), vous pouvez ouvrir un point de terminaison nommé « ECHO » dans le cadre d’un test rapide. Toute écriture sur un canal instancié à partir de ce point de terminaison entraînera la réception des mêmes données.

Vous pouvez utiliser cette technique pour tester une implémentation d’entrée/sortie (e/s) du module côté serveur, pour mesurer le temps de réponse d’un plug-in client Connexion Bureau à distance (RDC) ou pour mesurer le délai réseau pour le client Connexion Bureau à distance (RDC). Il n’existe aucune limitation quant à la quantité de données qui peuvent être envoyées sur ce canal.

 

 




