---
title: Redirecteur
description: Le redirecteur est le composant en mode noyau du routeur qui est responsable du transfert des données d’une interface de routeur vers les autres.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029258"
---
# <a name="forwarder"></a>Redirecteur

Le redirecteur est le composant en mode noyau du routeur qui est responsable du transfert des données d’une interface de routeur vers les autres. Le redirecteur décide également si un paquet est destiné à une remise locale, s’il est destiné à être transféré hors d’une autre interface, ou les deux à la fois.

Il existe deux redirecteurs en mode noyau : monodiffusion et multidiffusion.

Le gestionnaire de routeur obtient les meilleurs itinéraires vers toutes les destinations du gestionnaire de tables de routage. Ces itinéraires sont passés au redirecteur de monodiffusion. Le redirecteur de monodiffusion utilise ces itinéraires pour effectuer le transfert réel des données de monodiffusion. De cette façon, le redirecteur de monodiffusion gère un cache des meilleurs itinéraires dans la vue de monodiffusion de la table de routage.

Le gestionnaire de groupe de multidiffusion utilise les informations de la vue multidiffusion de la table de routage pour ajouter des entrées de transfert de multidiffusion au redirecteur de multidiffusion.

 

 




