---
description: Recherche de l’emplacement de la bande
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Recherche de l’emplacement de la bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dca3c2b52d1501207b5b86f4e30b148a57c3881a725284a21455f7c2789c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050059"
---
# <a name="tape-location-search"></a>Recherche de l’emplacement de la bande

Bien que les périphériques DV prennent en charge une commande permettant d’effectuer des recherches par code de temps ou par le biais de la fonction ATN (Absolute Number), le pilote MSDV ne dispose pas d’une méthode standard, indépendante du périphérique pour accéder à ces fonctions. La seule option consiste à envoyer une commande AV/C brute au pilote, comme décrit dans la rubrique [émission de commandes AV/c brutes](issuing-raw-av-c-commands.md).

Le pilote UVC prend en charge un jeu de propriétés pour les recherches d’emplacement de bande. Pour envoyer une commande de recherche, utilisez l’interface **IKsControl** et définissez la \_ propriété de transport PROPSETID ext \_ . L’utilisation d’un jeu de propriétés est plus sûre que l’envoi de commandes AV/C brutes à l’appareil, car les commandes AV/C ignorent le filtre et accèdent directement au pilote de périphérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Ensemble de propriétés de transport d’appareil externe](external-device-transport-property-set.md)
</dt> </dl>

 

 



