---
description: L’objet capteur représente un capteur particulier.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Objet capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ad666153be31958bb758ca4b504e10591ccbe29c9d37355499c9d22c5aae2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666409"
---
# <a name="the-sensor-object"></a>Objet capteur

L’objet capteur représente un capteur particulier.

L’API de capteur représente chaque capteur sous la forme d’un objet de capteur. Vous pouvez utiliser un objet de capteur particulier par le biais de son interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) . Cette interface vous permet d’effectuer les opérations suivantes :

-   Récupérez les métadonnées relatives au capteur, telles que son ID, son type ou son nom convivial.
-   Récupérez des informations sur les données spécifiques que le capteur peut fournir.
-   Récupérez les données, de façon synchrone.
-   Récupérez les informations d’État, par exemple si le capteur est prêt.
-   Spécifiez les événements que votre programme recevra.
-   Spécifiez l’interface de rappel que l’API de capteur peut utiliser pour fournir à votre programme des notifications d’événements.

 

 



