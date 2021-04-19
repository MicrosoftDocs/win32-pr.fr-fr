---
description: Application WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Application WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525068"
---
# <a name="wpdservicesapisample-application"></a>Application WpdServicesApiSample

Un service d’appareil est une extension d’un objet fonctionnel : outre le regroupement logique des fonctionnalités de l’appareil, un service d’appareil fournit aux applications la possibilité de découvrir ces fonctionnalités par programmation.

L’exemple d’application WpdServicesApiSample est une application de bureau en ligne de commande que vous pouvez utiliser pour explorer les services de contacts sur les appareils connectés à votre ordinateur. Vous pouvez explorer ces services en répertoriant les formats, les événements, les méthodes et les services abstraits pris en charge. Vous pouvez également utiliser cette application pour récupérer les propriétés sur un service de contact donné et appeler les méthodes prises en charge par ce service.

Si vous n’avez pas encore un appareil qui prend en charge les services de contacts, vous pouvez toujours exécuter le WpdServicesApiSample si vous installez pour la première fois le WpdServiceSampleDriver inclus dans le kit de pilotes Windows.

L’exemple d’application WpdServicesApiSample comprend les fichiers suivants :



| **File**                | **Description**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp  | Contient des méthodes qui énumèrent le contenu d’un service de contacts donné.                                                                                                                                  |
| ContentProperties. cpp   | Contient des méthodes qui lisent et écrivent des propriétés sur un service de contacts donné.                                                                                                                              |
| ServiceCapabilities. cpp | Contient les méthodes qui récupèrent les formats, événements et services abstraits pris en charge par un service de contacts donné.                                                                   |
| ServiceEnumeration. cpp  | Contient les fonctions d’assistance qui récupèrent des informations sur l’appareil, telles que le nom convivial du périphérique ou les services de contacts pris en charge.                                                                       |
| ServiceMethods. cpp      | Contient les méthodes qui récupèrent et appellent les méthodes prises en charge par un service de contacts donné.                                                                                                              |
| stdafx.cpp              | Comprend les fichiers standard.                                                                                                                                                                              |
| WpdServiceApiSample. cpp | Héberge la fonction de démarrage **\_ tmain** , qui appelle la fonction de **menu contextuel** locale, qui affiche une liste des périphériques et des tâches disponibles et appelle la fonction appropriée pour la sélection de menu de l’utilisateur. |



 


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples](sample.md)
</dt> </dl>

 

 



