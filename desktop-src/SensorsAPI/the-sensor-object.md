---
description: L’objet capteur représente un capteur particulier.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Objet capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526152"
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

 

 



