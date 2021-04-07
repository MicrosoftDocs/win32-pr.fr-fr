---
title: Implémentation du jeu de propriétés d’informations de résumé
description: Il existe des instructions à suivre lors de l’implémentation d’un jeu de propriétés d’informations de synthèse pour le stockage structuré.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implémentation du jeu de propriétés d’informations de résumé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671066"
---
# <a name="implementing-the-summary-information-property-set"></a>Implémentation du jeu de propriétés d’informations de résumé

Il existe des instructions à suivre lors de l’implémentation d’un jeu de propriétés d’informations de synthèse pour le stockage structuré.

Voici les instructions à suivre pour implémenter [le jeu de propriétés d’informations de résumé](the-summary-information-property-set.md):

-   **PID \_ Le modèle** fait référence à un document externe contenant des informations de format et de style. Le processus par lequel se trouve le modèle est défini par l’implémentation.
-   **PID \_ LASTAUTHOR** est le nom stocké dans les informations utilisateur par l’application. Par exemple, Mary crée un document sur son ordinateur et le remet à John, qui le modifie et l’enregistre. Mary est l’auteur, John est le dernier enregistré par valeur.
-   **PID \_ REVNUMBER** est le nombre de fois que la commande File/Save a été appelée sur ce document.
-   Chacune des valeurs de date/heure doit être stockée au format UTC (Universal Coordinated Time).
-   **PID \_ CREATe \_ DTM** est une propriété en lecture seule ; Cette propriété doit être définie lors de la création d’un document, mais ne doit pas être modifiée par la suite.
-   Pour **la \_ miniature PID**, les applications doivent stocker des données au format **CF \_ DIB** ou **CF \_ MetaFilePict** . **CF \_ METAFILEPICT** est recommandé.
-   **PID \_ La sécurité** est le niveau de sécurité suggéré pour le document. En notant le niveau de sécurité du document, une application autre que l’expéditeur du document peut adapter son interface utilisateur aux propriétés. Une application ne doit pas afficher d’informations sur un document protégé par mot de passe ou permettre des modifications à des documents Read-Only ou verrouillés pour les annotations. Si l’utilisateur tente de modifier des propriétés, l’application doit avertir l’utilisateur de la Read-Only État recommandé.



| Niveau de sécurité         | Valeur |
|------------------------|-------|
| Aucune                   | 0     |
| Protégé par mot de passe     | 1     |
| Lecture seule recommandée  | 2     |
| En lecture seule forcé     | 4     |
| Verrouillé pour les annotations | 8     |



 

 

 




