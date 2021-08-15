---
title: Contrôle de capture précis
description: Contrôle de capture précis
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Fonctions de rappel AVICap, contrôle de capture précis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365482f5f6309f9642aa5c8b497b58a1d9416e398e5c3624191d777e006b23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372659"
---
# <a name="precise-capture-control"></a>Contrôle de capture précis

Une fenêtre de capture peut fournir la fonction de rappel de contrôle de capture avec un contrôle précis sur les moments de début et de fin de la capture de la diffusion en continu. Le premier message envoyé à partir du pilote de capture à la procédure de rappel définit le paramètre *nState* sur le \_ préroll CONTROLCALLBACK après avoir alloué toutes les mémoires tampons et toutes les autres préparations de capture sont terminées. Ce message donne à l’application la possibilité de Prérouler les sources vidéo. (La fonction de rappel spécifie *nState* comme deuxième paramètre.) La fonction de rappel retourne alors à l’enregistrement exact du moment. La valeur de retour **true** à partir de la fonction de rappel continue la capture. La valeur de retour **false** abandonne la capture. Une fois la capture lancée, la fonction de rappel est appelée fréquemment avec *nState* défini sur la \_ capture CONTROLCALLBACK pour permettre à l’application de terminer la capture en renvoyant la **valeur false**.

 

 




