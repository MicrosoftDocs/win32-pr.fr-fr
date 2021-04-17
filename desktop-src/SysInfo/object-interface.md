---
description: 'Windows fournit des fonctions qui effectuent les tâches suivantes :'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interface d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485248"
---
# <a name="object-interface"></a>Interface d’objet

Windows fournit des fonctions qui effectuent les tâches suivantes :

-   Créer un objet
-   Obtient un handle d’objet
-   Obtenir des informations sur l’objet
-   Définir les informations relatives à l’objet
-   Fermer le descripteur d’objet
-   Détruire l’objet

Certaines de ces tâches ne sont pas nécessaires pour chaque objet. Certaines de ces tâches sont combinées pour certains objets. Par exemple, une application peut créer un objet d’événement. D’autres applications peuvent ouvrir l’événement pour obtenir un descripteur unique de cet objet d’événement. À mesure que chaque application se termine à l’aide de l’événement, elle ferme son handle vers l’objet. Lorsqu’il n’y a aucun descripteur ouvert restant pour l’objet d’événement, le système détruit l’objet d’événement. En revanche, une application peut obtenir un handle vers un objet Window existant. Lorsque l’objet Window n’est plus nécessaire, l’application doit détruire l’objet, ce qui invalide le handle de fenêtre.

Parfois, un objet reste en mémoire après la fermeture de tous les handles d’objet. Par exemple, un thread peut créer un objet d’événement et attendre le descripteur d’événement. Pendant que le thread attend, un autre thread peut fermer le même handle d’objet d’événement. L’objet d’événement reste en mémoire, sans aucun handle d’objet d’événement, jusqu’à ce que l’objet d’événement soit défini sur l’état signalé et que l’opération d’attente soit terminée. À ce stade, le système supprime l’objet de la mémoire.

Les handles et les objets consomment de la mémoire. Par conséquent, pour préserver les performances du système, vous devez fermer les handles et supprimer les objets dès qu’ils ne sont plus nécessaires. Si vous ne le faites pas, votre application peut nuire aux performances du système, en raison d’une utilisation excessive du fichier d’échange.

Lorsqu’un processus se termine, le système ferme automatiquement les handles et supprime les objets créés par le processus. Toutefois, lorsqu’un thread se termine, le système ne ferme généralement pas les handles ou ne supprime pas les objets. Les seules exceptions sont les objets Window, Hook, position de fenêtre et conversation DDE (Dynamic Data Exchange). ces objets sont détruits lorsque le thread de création se termine.

 

 



