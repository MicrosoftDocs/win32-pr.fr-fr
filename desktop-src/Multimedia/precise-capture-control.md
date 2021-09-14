---
title: Contrôle de capture précis
description: Contrôle de capture précis
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Fonctions de rappel AVICap, contrôle de capture précis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119525"
---
# <a name="precise-capture-control"></a>Contrôle de capture précis

Une fenêtre de capture peut fournir la fonction de rappel de contrôle de capture avec un contrôle précis sur les moments de début et de fin de la capture de la diffusion en continu. Le premier message envoyé à partir du pilote de capture à la procédure de rappel définit le paramètre *nState* sur le \_ préroll CONTROLCALLBACK après avoir alloué toutes les mémoires tampons et toutes les autres préparations de capture sont terminées. Ce message donne à l’application la possibilité de Prérouler les sources vidéo. (La fonction de rappel spécifie *nState* comme deuxième paramètre.) La fonction de rappel retourne alors à l’enregistrement exact du moment. La valeur de retour **true** à partir de la fonction de rappel continue la capture. La valeur de retour **false** abandonne la capture. Une fois la capture lancée, la fonction de rappel est appelée fréquemment avec *nState* défini sur la \_ capture CONTROLCALLBACK pour permettre à l’application de terminer la capture en renvoyant la **valeur false**.

 

 




