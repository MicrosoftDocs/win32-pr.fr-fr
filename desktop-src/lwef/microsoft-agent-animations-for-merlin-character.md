---
title: Animations Microsoft Agent pour le caractère Merlin
description: Animations Microsoft Agent pour le caractère Merlin
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797002897f0e3bdb7efb309de8b73a33df8bdf399279895be8daa2b47d8ec084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247472"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Animations Microsoft Agent pour le caractère Merlin

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le [caractère Microsoft Agent Merlin](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) est un travail protégé par des droits d’auteur de Microsoft Corporation.

Merlin prend en charge les animations indiquées dans le tableau ci-dessous. Reportez-vous à [la rubrique programmation de l’interface du serveur Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) et [programmation du contrôle Microsoft Agent](programming-the-microsoft-agent-control.md) pour plus d’informations sur la façon d’appeler les animations du caractère.

Si vous accédez à ces animations de caractères à l’aide du protocole HTTP et de la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) d' [**obtention**](get-method.md) ou du serveur du contrôle, réfléchissez à la façon dont vous allez les télécharger. Au lieu de télécharger toutes les animations simultanément, vous souhaiterez peut-être d’abord récupérer les animations d’état d' **émission** et de **dictée** . Cela vous permettra d’afficher rapidement le caractère et de le faire parler tout en rapprochant les autres animations de manière asynchrone. En outre, pour garantir le chargement correct des données de caractères et d’animation, utilisez l’événement [**RequestComplete**](requestcomplete-event.md) . En cas d’échec d’une demande de chargement, vous pouvez réessayer de charger les données ou afficher un message approprié.

Si l’animation de **retour** d’une animation est définie à l’aide de branches de sortie, vous n’avez pas besoin de l’appeler explicitement ; Agent lit automatiquement l’animation de **retour** avant l’animation suivante. Toutefois, si une animation de **retour** est listée, vous devez appeler l’animation à l’aide de la méthode [**Play**](play-method.md) avant une autre animation pour fournir une transition lisse. Si aucune animation de **retour** n’est indiquée, l’animation se termine normalement sans avoir besoin d’une animation de transition.

Le fichier de caractères comprend des effets sonores pour certaines animations, comme indiqué dans le tableau suivant. Les effets sonores s’exécutent uniquement si cette option est activée dans la feuille de propriétés de l’agent Microsoft. Vous pouvez également désactiver les effets sonores dans votre application.



| Animation                 | Retourner l’animation         | Prend en charge la parole | Effets sonores | Affecté à l’État                            | Description                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Reconnaître**           | Aucun                     | Non                | **Non**        | Aucune                                         | Tête nœuds                                        |
| **Alert**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | **Listen**                                | Redresser et déclencher des sourcils                  |
| **Annoncé**              | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Déclenche une trompette et des lectures                         |
| **Blink**                 | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Clignoter les yeux                                      |
| **Confus**              | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Tête Scratch                                   |
| **Féliciter**          | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Affiche les trophées                                  |
| **Féliciter \_ 2**       | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Applauds                                         |
| **Refuser**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Soulève des mains et des secousses                     |
| **DoMagic1**              | Aucune                     | Oui               | **Non**        | Aucune                                         | Déclenche la baguette magique                                |
| **DoMagic2**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucune                                         | Baguettes de réduction, Clouds apparaissent                       |
| **DontRecognize**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Tient à l’oreille                                |
| **Expliquer**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Étend les bras à la côte                             |
| **GestureDown**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingDown**                            | Mouvements vers le dessous                                    |
| **GestureLeft**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingLeft**                            | Mouvements restants                                    |
| **GestureRight**          | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingRight**                           | Mouvements droite                                   |
| **GestureUp**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingUp**                              | Mouvements vers le haut                                      |
| **GetAttention**          | **GetAttentionReturn**   | Oui               | **Oui**       | Aucune                                         | Avances et coups                         |
| **GetAttentionContinued** | **GetAttentionReturn**   | Oui               | **Oui**       | Aucune                                         | Pour anticiper, Refrappe                    |
| **GetAttentionReturn**    | Aucun                     | Non                | **Non**        | Aucune                                         | Retourne à la position neutre                      |
| **Greet**                 | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Sacs                                             |
| **Audition \_ 1**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Ears extend ( \* animation de bouclage)                |
| **Audition \_ 2**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | En-tête gauche ( \* animation en boucle)            |
| **Audition \_ 3**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Active la tête gauche ( \* animation de boucle)            |
| **Audition \_ 4**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Active la tête à droite ( \* animation de boucle)           |
| **Masquer**                  | Aucun                     | Non                | **Oui**       | **Masquage**                                   | Disparaît sous l’extrémité                             |
| **Idle1 \_ 1**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Est à l’air                                     |
| **Idle1 \_ 2**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Aperçus de gauche et de clignotement                          |
| **Idle1 \_ 3**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Aperçus à droite                                    |
| **Idle1 \_ 4**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble de la droite et des clignotements               |
| **Idle2 \_ 1**              | Aucun                     | Non                | **Non**        | **IdlingLevel2**                             | Regarde la baguette et les clignotements                         |
| **Idle2 \_ 2**              | Aucun                     | Non                | **Non**        | **IdlingLevel2**                             | Contient des mains et des clignotements                           |
| **Idle3 \_ 1**              | Aucun                     | Non                | **Oui**       | **IdlingLevel3**                             | Réactions                                            |
| **Idle3 \_ 2**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **IdlingLevel3**                             | Passe en veille ( \* animation de bouclage)               |
| **LookDown**              | **LookDownReturn**       | Non                | **Non**        | Aucune                                         | Recherche vers le                                       |
| **LookDownBlink**         | **LookDownReturn**       | Non                | **Non**        | Aucune                                         | Clignote en regardant                              |
| **LookDownReturn**        | Aucun                     | Non                | **Non**        | Aucune                                         | Retourne à la position neutre                      |
| **LookLeft**              | **LookLeftReturn**       | Non                | **Non**        | Aucune                                         | Semble à gauche                                       |
| **LookLeftBlink**         | **LookLeftReturn**       | Non                | **Non**        | Aucune                                         | Clignoter en regardant à gauche                              |
| **LookLeftReturn**        | Aucun                     | Non                | **Non**        | Aucune                                         | Retourne à la position neutre                      |
| **LookRight**             | **LookRightReturn**      | Non                | **Non**        | Aucune                                         | Semble à droite                                      |
| **LookRightBlink**        | **LookRightReturn**      | Non                | **Non**        | Aucune                                         | Clignote en regardant vers la droite                             |
| **LookRightReturn**       | Aucun                     | Non                | **Non**        | Aucune                                         | Retourne à la position neutre                      |
| **Directes**                | **LookUpReturn**         | Non                | **Non**        | Aucune                                         | Recherche                                         |
| **LookUpBlink**           | **LookUpReturn**         | Non                | **Non**        | Aucune                                         | Clignotement de la recherche                                |
| **LookUpReturn**          | Aucun                     | Non                | **Non**        | Aucune                                         | Retourne à la position neutre                      |
| **Descendre**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingDown**                               | Brusque                                       |
| **MoveLeft**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingLeft**                               | À gauche                                       |
| **MoveRight**             | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingRight**                              | À droite                                      |
| **MoveUp**                | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingUp**                                 | Envole                                         |
| **Heureux**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Sourires et conserve les mains                  |
| **Processus**               | Non                       | Non                | **Oui**       | Aucune                                         | Agit Caldron                                    |
| **Traitement**            | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucune                                         | Agit Caldron ( \* animation de bouclage)              |
| **Lecture**                  | **ReadReturn**           | Oui               | **Oui**       | Aucune                                         | Ouvre Book, lit et recherche                   |
| **ReadContinued**         | **ReadReturn**           | Oui               | **Oui**       | Aucune                                         | Lectures et recherches                               |
| **ReadReturn**            | Aucun                     | Non                | **Oui**       | Aucune                                         | Retourne à la position neutre                      |
| **Lecture**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucune                                         | Lectures ( \* animation de bouclage)                      |
| **RestPose**              | Aucune                     | Oui               | **Non**        | **Parlez**                                 | Position neutre                                 |
| **Fer**                   | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Expression Sad                                   |
| **action**                | Non                       | Non                | **Oui**       | Aucune                                         | Recherche dans la boule de cristal                          |
| **Dans**             | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucune                                         | Recherche dans la boule de cristal ( \* animation de bouclage)    |
| **Afficher**                  | Aucun                     | Non                | **Oui**       | **Affichage**                                  | S’affiche hors Cap                               |
| **StartListening**        | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Place à l’oreille                                 |
| **StopListening**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Place les mains sur les oreilles                             |
| **Suggérer**               | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Affiche les ampoules                               |
| **Étonne**             | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucune                                         | Semble surpris                                  |
| **Réflexion**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Recherche avec la main sur le menton                       |
| **Opération en cours**              | Non                       | Non                | **Non**        | Aucune                                         | Recherche avec la main sur le menton ( \* animation de bouclage) |
| **Connaître**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Augmente la progression et déclenche un sourcil                 |
| **Wave**                  | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucune                                         | Fréquences                                            |
| **Écriture**                 | **WriteReturn**          | Oui               | **Oui**       | Aucune                                         | Ouvre Book, écrit et recherche                  |
| **WriteContinued**        | **WriteReturn**          | Oui               | **Oui**       | Aucune                                         | Écritures et recherches                              |
| **WriteReturn**           | Aucun                     | Non                | **Oui**       | Aucune                                         | Retourne à la position neutre                      |
| **Écriture**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucune                                         | Écritures ( \* animation de bouclage)                     |



 

\* Si vous lisez une animation de bouclage, vous devez utiliser [**Stop**](stop-method.md) pour la supprimer avant que d’autres animations de la file d’attente du caractère ne soient lues.

 

