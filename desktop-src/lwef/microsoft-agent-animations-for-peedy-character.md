---
title: Animations Microsoft Agent pour le caractère Peedy
description: Animations Microsoft Agent pour le caractère Peedy
ms.assetid: 335d915c-9cae-4850-a6bf-66ad78d533ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e064063b322bc6549d91b5fce35bdbc491a5a3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727036"
---
# <a name="microsoft-agent-animations-for-peedy-character"></a>Animations Microsoft Agent pour le caractère Peedy

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le [caractère Microsoft Agent Peedy](https://www.microsoft.com/downloads/details.aspx?FamilyID=bd3c4655-79e4-4791-ab9d-abc7bbd133ef) est un travail protégé par des droits d’auteur de Microsoft Corporation.

Peedy prend en charge les animations indiquées dans le tableau ci-dessous. Reportez-vous à [la rubrique programmation de l’interface du serveur Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) et [programmation du contrôle Microsoft Agent](programming-the-microsoft-agent-control.md) pour plus d’informations sur la façon d’appeler les animations du caractère.

Si vous accédez à ces animations de caractères à l’aide du protocole HTTP et de la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) d' [**obtention**](get-method.md) ou du serveur du contrôle, réfléchissez à la façon dont vous allez les télécharger. Au lieu de télécharger toutes les animations simultanément, vous souhaiterez peut-être d’abord récupérer les animations d’état d' **émission** et de **dictée** . Cela vous permettra d’afficher rapidement le caractère et de le faire parler tout en rapprochant les autres animations de manière asynchrone. En outre, pour garantir le chargement correct des données de caractères et d’animation, utilisez l’événement [**RequestComplete**](requestcomplete-event.md) . En cas d’échec d’une demande de chargement, vous pouvez réessayer de charger les données ou afficher un message approprié.

Si l’animation de **retour** d’une animation est définie à l’aide de branches de sortie, vous n’avez pas besoin de l’appeler explicitement ; Agent lit automatiquement l’animation de **retour** avant l’animation suivante. Toutefois, si une animation de **retour** est listée, vous devez appeler l’animation à l’aide de la méthode [**Play**](play-method.md) avant une autre animation pour fournir une transition lisse. Si aucune animation de **retour** n’est indiquée, l’animation se termine normalement sans avoir besoin d’une animation de transition.

Si vous accédez à ces animations de caractères à l’aide du protocole HTTP et de la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) d' [**obtention**](get-method.md) ou du serveur du contrôle, réfléchissez à la façon dont vous allez les télécharger. Au lieu de télécharger toutes les animations simultanément, vous souhaiterez peut-être d’abord récupérer les animations d’état d' **émission** et de **dictée** . Cela vous permettra d’afficher rapidement le caractère et de le faire parler tout en rapprochant les autres animations de manière asynchrone. En outre, pour garantir le chargement correct des données de caractères et d’animation, utilisez l’événement [**RequestComplete**](requestcomplete-event.md) . En cas d’échec d’une demande de chargement, vous pouvez réessayer de charger les données ou afficher un message approprié.

Le fichier de caractères comprend des effets sonores pour certaines animations, comme indiqué dans le tableau suivant. Les effets sonores s’exécutent uniquement si cette option est activée dans la feuille de propriétés de l’agent Microsoft. Vous pouvez également désactiver les effets sonores dans votre application.



| Animation                  | Retourner l’animation         | Prend en charge la parole | Effets sonores | Affecté à l’État                            | Description                                            |
|----------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------------|
| **Reconnaître**            | Aucun                     | Non                | **Non**        | Aucun                                         | Tête nœuds                                              |
| **Alert**                  | Oui, utilisation des branches de sortie | Oui               | **Non**        | **Listen**                                | Redresser et déclencher des sourcils                        |
| **Annoncé**               | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Avion en papier et déplier                    |
| **Blink**                  | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Clignoter les yeux                                            |
| **Confus**               | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Tourner les yeux                                       |
| **Féliciter**           | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Affiche le ruban bleu                                   |
| **Refuser**                | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Secouer la tête                                            |
| **DoMagic1**               | Aucun                     | Oui               | **Oui**       | Aucun                                         | Déclenche la baguette magique                                      |
| **DoMagic2**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Baguettes de réduction, Clouds apparaissent                             |
| **DontRecognize**          | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Secoue la tête et maintient l’aile sur l’oreille                      |
| **Expliquer**                | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Étend les bras à la côte                                   |
| **GestureDown**            | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingDown**                            | Mouvements vers le dessous                                          |
| **GestureLeft**            | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingLeft**                            | Mouvements restants                                          |
| **GestureRight**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingRight**                           | Mouvements droite                                         |
| **GestureUp**              | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingUp**                              | Mouvements vers le haut                                            |
| **GetAttention**           | **GetAttentionReturn**   | Oui               | **Oui**       | Aucun                                         | Pointe vers le haut avec des ailes étirées                       |
| **GetAttentionContinued**  | **GetAttentionReturn**   | Oui               | **Oui**       | Aucun                                         | Atteint une nouvelle fois les ailes rétendues                 |
| **GetAttentionReturn**     | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **Greet**                  | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Sacs                                                   |
| **Audition \_ 1**             | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Inclinaison de l’en-tête à droite ( \* animation de bouclage)                 |
| **Audition \_ 2**             | Aucun                     | Non                | **Non**        | **Ouïe**                                  | En-tête gauche ( \* animation en boucle)                  |
| **Audition \_ 3**             | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Active la tête droite et gauche ( \* animation de bouclage)       |
| **Masquer**                   | Aucun                     | Non                | **Oui**       | **Masquage**                                   | À l’opposé                                             |
| **Idle1 \_ 1**               | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Est à l’air                                           |
| **Idle1 \_ 2**               | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble des bons et des clignotements                               |
| **Idle1 \_ 3**               | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Aperçus de gauche et de clignotement                                |
| **Idle1 \_ 4**               | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble et clignotement                                  |
| **Idle1 \_ 5**               | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble des clignotements et des clignotements                                |
| **Idle2 \_ 1**               | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel2**                             | Place sur les soleil                                     |
| **Idle2 \_ 2**               | Aucun                     | Non                | **Oui**       | **IdlingLevel2**                             | Consomme un pirate                                         |
| **Idle3 \_ 1**               | Aucun                     | Non                | **Oui**       | **IdlingLevel3**                             | Réactions                                                  |
| **Idle3 \_ 2**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | **IdlingLevel3**                             | Passe en veille ( \* animation de bouclage)                     |
| **Idle3 \_ 3**               | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel3**                             | Écoute la musique ( \* animation de boucle)                 |
| **LookDownLookDownReturn** |                          | Non                | **Non**        | Aucun                                         | Recherche vers le                                             |
| **LookDownBlink**          | **LookDownReturn**       | Non                | **Oui**       | Aucun                                         | Clignote en regardant                                    |
| **LookDownReturn**         | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **LookDownLeft**           | **LookDownLeftReturn**   | Non                | **Non**        | Aucun                                         | Recherche vers le gauche                                        |
| **LookDownLeftBlink**      | **LookDownLeftReturn**   | Non                | **Oui**       | Aucun                                         | Clignote en regardant à gauche                               |
| **LookDownLeftReturn**     | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **LookDownRight**          | **LookDownRightReturn**  | Non                | **Non**        | Aucun                                         | Recherche vers le droite                                       |
| **LookDownRightBlink**     | **LookDownRightReturn**  | Non                | **Oui**       | Aucun                                         | Clignote en regardant à droite                              |
| **LookDownRightReturn**    | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **LookLeft**               | **LookLeftReturn**       | Oui               | **Non**        | Aucun                                         | Semble à gauche                                             |
| **LookLeftBlink**          | **LookLeftReturn**       | Oui               | **Oui**       | Aucun                                         | Clignoter en regardant à gauche                                    |
| **LookLeftReturn**         | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **LookRight**              | **LookRightReturn**      | Oui               | **Non**        | Aucun                                         | Semble à droite                                            |
| **LookRightBlink**         | **LookRightReturn**      | Oui               | **Oui**       | Aucun                                         | Clignote en regardant vers la droite                                   |
| **LookRightReturn**        | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **Directes**                 | **LookUpReturn**         | Non                | **Non**        | Aucun                                         | Recherche                                               |
| **LookUpBlink**            | **LookUpReturn**         | Non                | **Oui**       | Aucun                                         | Clignotement de la recherche                                      |
| **LookUpReturn**           | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **LookUpLeft**             | **LookUpLeftReturn**     | Non                | **Non**        | Aucun                                         | Recherche vers le haut à gauche                                          |
| **LookUpLeftBlink**        | **LookUpLeftReturn**     | Non                | **Oui**       | Aucun                                         | Clignote à la recherche de gauche                                 |
| **LookUpLeftReturn**       | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **LookUpRight**            | **LookUpRightReturn**    | Non                | **Non**        | Aucun                                         | Recherche vers le haut                                         |
| **LookUpRightBlink**       | **LookUpRightReturn**    | Non                | **Oui**       | Aucun                                         | Clignote à la recherche de droite                                |
| **LookUpRightReturn**      | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **Descendre**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingDown**                               | Brusque                                             |
| **MoveLeft**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingLeft**                               | À gauche                                             |
| **MoveRight**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingRight**                              | À droite                                            |
| **MoveUp**                 | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingUp**                                 | Envole                                               |
| **Heureux**                | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Sourires                                                 |
| **Processus**                | Aucun                     | Non                | **Oui**       | Aucun                                         | Utilise la calculatrice                                        |
| **Traitement**             | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Utilise Calculator ( \* animation de bouclage)                  |
| **Lire**                   | **ReadReturn**           | Oui               | **Oui**       | Aucun                                         | Ouvre le magazine, lit et recherche                     |
| **ReadContinued**          | **ReadReturn**           | Oui               | **Oui**       | Aucun                                         | Lectures et recherches                                     |
| **ReadReturn**             | Aucun                     | Non                | **Oui**       | Aucun                                         | Retourne à la position neutre                            |
| **Lecture**                | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Lectures ( \* animation de bouclage)                            |
| **RestPose**               | Aucun                     | Oui               | **Non**        | **Parlez**                                 | Position neutre                                       |
| **Fer**                    | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Expression Sad                                         |
| **Recherche**                 | Aucun                     | Non                | **Oui**       | Aucun                                         | Révèle la télégénération et les rotations                          |
| **Dans**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Révèle la télégénération et les rotations ( \* animation de bouclage)    |
| **Afficher**                   | Aucun                     | Non                | **Oui**       | **Affichage**                                  | Rentrez dans                                               |
| **StartListening**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Place à l’oreille                                       |
| **StopListening**          | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Passe des mains aux oreilles                                     |
| **Suggérer**                | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Affiche l’ampoule                                    |
| **Étonne**              | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Semble surpris                                        |
| **Réflexion**                  | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Recherche avec aile en face                             |
| **Opération en cours**               | Aucun                     | Non                | **Non**        | Aucun                                         | Recherche avec aile on face ( \* animation en boucle)       |
| **Connaître**              | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Se penche sur Right et Shrugs                              |
| **Wave**                   | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Fréquences                                                  |
| **Écrire**                  | **WriteReturn**          | Oui               | **Oui**       | Aucun                                         | Extrait le crayon et le bloc, écrit et recherche          |
| **WriteContinued**         | **WriteReturn**          | Oui               | **Oui**       | Aucun                                         | Écritures et recherches                                    |
| **WriteReturn**            | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                            |
| **Écriture**                | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Tire un crayon et un bloc, écritures ( \* animation de bouclage) |



 

\* Si vous lisez une animation de bouclage, vous devez utiliser [**Stop**](stop-method.md) pour la supprimer avant que d’autres animations de la file d’attente du caractère ne soient lues.

 

