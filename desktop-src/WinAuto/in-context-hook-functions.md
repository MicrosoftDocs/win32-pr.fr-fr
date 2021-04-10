---
title: Fonctions de raccordement In-Context
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'En savoir plus sur : fonctions de raccordement In-Context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210741"
---
# <a name="in-context-hook-functions"></a>Fonctions de raccordement In-Context

La liste suivante présente les aspects clés des fonctions de raccordement dans le contexte :

-   Les fonctions de raccordement dans le contexte doivent se trouver dans une bibliothèque de liens dynamiques (DLL) que le système mappe à l’espace d’adressage du serveur.
-   Les fonctions de raccordement dans le contexte partagent l’espace d’adressage avec le serveur.
-   Lorsque le serveur déclenche un événement, le système appelle une fonction de raccordement sans marshaling (empaquetage et envoi de paramètres d’interface entre les limites de processus).
-   Les fonctions de raccordement dans le contexte ont tendance à être très rapides et à recevoir des notifications d’événements de façon synchrone, car il n’existe aucun marshaling.
-   Certains événements peuvent être remis hors processus, même si vous demandez qu’ils soient remis en cours (à l’aide de l' \_ indicateur INCONTEXT WINEVENT). Vous pouvez voir cette situation avec des problèmes d’interopérabilité des applications 64 bits et 32 bits et avec les événements de la console Windows.

 

 




