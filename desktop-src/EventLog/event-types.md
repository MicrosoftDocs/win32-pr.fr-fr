---
description: Il existe cinq types d’événements qui peuvent être journalisés. Toutes ces données comportent des données communes bien définies et peuvent éventuellement inclure des données spécifiques à l’événement.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Types d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864245"
---
# <a name="event-types"></a>Types d’événements

Il existe cinq types d’événements qui peuvent être journalisés. Toutes ces données comportent des données communes bien définies et peuvent éventuellement inclure des données spécifiques à l’événement.

L’application indique le type d’événement lorsqu’il signale un événement. Chaque événement doit être d’un type unique. L’observateur d’événements affiche une icône différente pour chaque type dans le mode liste du journal des événements.

Le tableau suivant décrit les cinq types d’événements utilisés dans la journalisation des événements.



| Type d'événement        | Description                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Error**         | Événement qui indique un problème grave tel qu’une perte de données ou une perte de fonctionnalités. Par exemple, si un service ne parvient pas à se charger au démarrage, un événement d’erreur est consigné.                                                                                                                           |
| **Avertissement**       | Événement qui n’est pas nécessairement significatif, mais qui peut indiquer un éventuel problème futur. Par exemple, lorsque l’espace disque est faible, un événement d’avertissement est enregistré. Si une application peut effectuer une récupération à partir d’un événement sans perte de fonctionnalités ou de données, elle peut généralement classer l’événement comme un événement d’avertissement.     |
| **Informations**   | Événement qui décrit la réussite de l’opération d’une application, d’un pilote ou d’un service. Par exemple, lorsqu’un pilote réseau est chargé avec succès, il peut être approprié d’enregistrer un événement d’information. Notez qu’il n’est généralement pas approprié pour une application de bureau de consigner un événement à chaque fois qu’elle démarre. |
| **Audit des succès** | Événement qui enregistre une tentative d’accès de sécurité auditée réussie. Par exemple, la tentative réussie d’un utilisateur pour se connecter au système est consignée comme un événement d’audit de réussite.                                                                                                                        |
| **Audit des échecs** | Événement qui enregistre une tentative d’accès de sécurité auditée qui échoue. Par exemple, si un utilisateur tente d’accéder à un lecteur réseau et échoue, la tentative est consignée comme un événement d’audit d’échec.                                                                                                                   |



 

Les activités sélectionnées des utilisateurs peuvent être suivies en auditant les événements de sécurité, puis en plaçant des entrées dans le journal de sécurité d’un ordinateur.

 

 



